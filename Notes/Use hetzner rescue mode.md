1. Connect to [[Hetzner]] dashboard
2. Goto the Rescue Section of your server, but click on the "Enable Rescue & Power Cycle" button instead of the (reset root password) button.
3. After that your server will boot into a rescue system.
4. Connect to your server via SSH with the rescue login using `ssh root@IP`
5. Run the following commands in Rescue:
    
```bash
mount /dev/sda1 /mnt
chroot-prepare /mnt
chroot /mnt

# do the things

Ctrl-D
reboot
```
