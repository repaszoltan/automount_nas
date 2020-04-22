# automount_nas
Help to mount NAS drive at reboot

How to use:

1. edit the .smbcredentials file, 
2. <code>chmod 600 .smbcredential</code>
3. <code>chown root .smbcredential</code>
4. edit upnas scrypt
5. edit the root crontab (normal user can-t mount that)<br>
  <code>sudo crontab -e</code><br>
  Then insert this line the end of crontab:<br>
  <code>@reboot sleep 60 && /home/user/upnas</code><br>
