Q: nginx error log:***failed (13: Permission denied)
A:
  1、gpasswd -a www-data path-owner
  2、nginx -s reload
