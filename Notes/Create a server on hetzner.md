- Type: shared vCPU CX22
- Networking: IPv6 only
- Set your [[SSH Keys]] as default
- Use this cloud init, note that I set `AllowTcpForwarding yes` compared to the cloud-init proposed by Hetzner
```yaml
#cloud-config
users:
  - name: simone
    groups: users, admin
    sudo: ALL=(ALL) ALL
    shell: /bin/bash
    ssh_authorized_keys:
      - ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIJD6a6cUp2MsZDYn3OcujzHm9QwgR+tNr9nBuYzEZXqP simone@dragonfly (personal)
packages:
  - fail2ban
  - ufw
package_update: true
package_upgrade: true
write_files:
  - path: /etc/ssh/sshd_config.d/ssh-hardening.conf
    content: |
      PermitRootLogin no
      PasswordAuthentication no
      Port 9934
      KbdInteractiveAuthentication no
      ChallengeResponseAuthentication no
      MaxAuthTries 2
      AllowTcpForwarding yes
      X11Forwarding no
      AllowAgentForwarding no
      AuthorizedKeysFile .ssh/authorized_keys
      AllowUsers simone
runcmd:
  - printf "[sshd]\nenabled = true\nport = 9934, 9934\nbanaction = iptables-multiport" > /etc/fail2ban/jail.local
  - systemctl enable fail2ban
  - ufw allow 9934/tcp
  - ufw enable
  - reboot
```

## Things to figure out
How to set the sudo password for simone? For now I used [[Use hetzner rescue mode]]