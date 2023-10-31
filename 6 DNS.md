# At basic level what is DNS used for ?

resolve ip of a domain name

# On a Linux based system, which of the following file can be used to point domains/hostnames to IPs locally?

Run: `cat /etc/hosts` and see the domains/hostnames.


# On a Linux based system, which of the following file contains information about dns server i.e nameserver?
Run: `cat /etc/resolv.conf` and see the details about dns server.


# On host01, if we have an entry for app01 in /etc/hosts file like 172.168.238.12 app01 and the DNS server which is used by host01 has 172.168.239.10 as app01's IP then which IP host01 will pick for app01 as per priority.

Check hosts order in /etc/nsswitch.conf file on host01.

# On host01, point www.google.com to 127.0.0.1 IP address locally.
Add 127.0.0.1 www.google.com entry in /etc/hosts file.

```sudo vi /etc/hosts```

# On host01, add Google public DNS i.e 8.8.8.8 as a nameserver.

Add nameserver 8.8.8.8 entry in /etc/resolv.conf file.

Open VI editor as shown below :-

```ruby
thor@host01 ~$ sudo vi /etc/resolv.conf
```
![image](https://github.com/Althaf-official/DevOps/assets/105126131/4fba8d7e-9bd5-438a-8b67-eab3de56774c)

press i to insert and add given details to the file then press ESC and use :wq to save and exit from the editor.

# In www.google.com, which is the top level domain?
.com

# On host01 we want to resolve name news to news.yahoo.com automatically without hard coding its entry in /etc/hosts file. Add the required changes on host01.
Add `search yahoo.com` entry in `/etc/resolv.conf` file.

# Which of the following command is used to query a hostname from a DNS server?
nslookup

