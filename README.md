# A simple guide
to help automount a NAS drive at startup

How to use:

1. edit the .smbcredentials file, 
2. <code>chmod 600 .smbcredential</code>
3. <code>chown root .smbcredential</code>
4. edit upnas script
5. edit the root crontab (normal user can-t mount that)<br>
  <code>sudo crontab -e</code><br>
  Then insert this line the end of crontab:<br>
  <code>@reboot sleep 60 && /home/user/upnas</code><br>
