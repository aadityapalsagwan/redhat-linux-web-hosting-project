# Website Hosting on Red Hat Linux 10

## Project Overview
Hosted a static website on Red Hat Linux 10 using Apache in VMware.

## Technologies Used
- Red Hat Linux 10
- VMware
- Apache HTTP Server
- systemctl
- journalctl
- firewalld
- SELinux

## Commands Used

dnf install httpd -y
systemctl start httpd
systemctl enable httpd
firewall-cmd --permanent --add-service=http
firewall-cmd --reload
getenforce
setenforce 0
restorecon -Rv /var/www/html
journalctl -u httpd
ip a
curl http://192.168.16.144  | Completed.

## Issues Resolved
- Apache startup issue
- SELinux blocking HTTP access
- VMware adapter conflict

## Author
Aaditya Pal