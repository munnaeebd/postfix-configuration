# postfix-configuration

hostnamectl set-hostname test-bed.brilliant.com.bd

vi /etc/postfix/sasl_passwd
~~~
[mta.brilliant.com.bd]:25  monitor@brilliant.com.bd:password
~~~

~~~
postmap /etc/postfix/sasl_passwd
chown root:root /etc/postfix/sasl_passwd*
chmod 600 /etc/postfix/sasl_passwd*
yum install cyrus-sasl cyrus-sasl-plain
systemctl restart postfix
~~~


crontab: 
0 */12 * * * /root/clamav.sh
