# Local networks

Your company, Machibuya, just open a new office in Bach Khoa. You are charged to set up the required servers so that :

 - DHCP is resolved
 - DNS is resolved
 - A DNS zone is managed for this new office
 - A NFS server is available to share files
 - A LDAP server is available with the registered users

## Question 1 Warming up

*2 points*

Create three virtual machines with these names on virtualbox :

 - eval1-client
 - eval1-nfs-server
 - eval1-server

Add them an interface on a private network.

## Question 2 DHCP stuff

*6 points*

 1. Configure eval1-server to have 192.168.102.5/24 static IP (1 point)
 2. Install DHCPD on eval1-server (1 point)
 3. Configure dhcpd to allocate IPs from 192.168.102.100 to 192.168.102.200 (2 point)
 4. Configure eval1-client to obtain an IP from eval1-server (1 point)
 5. Configure eval1-nfs-server to obtain an IP address. eval1-server should always return it the same IP address. (1 point)

## Question 3 DNS stuff

*6 points*

 1. Install a DNS server on eval1-server. Configure both eval1-nfs-server and eval1-client to use it (2 point)
 2. The main office of the company delegate you the management of bachkhoa.machibuya.com. They asked you to create the entries server.bachkhoa.machibuya.com for eval1-server and nfs.backkhoa.machibuya.com for eval1-nfs-server. (2 point)
 3. Create also the reverse entries (2 point)

## Question 4 NFS share

*3 points*

 1. Install a NFS server on eval1-nfs-server. This server should export the /data folder. (1 point)
 2. eval1-client should mount this share in /mnt/nfs folder upon startup. (2 point)

## Question 5 LDAP server

*5 points*

 1. Install a LDAP server on eval1-server. Manage dc=bachkhoa,dc=machibuya,dc=com. Edit the configuration accordingly. You should be able to start it. (2 points)
 2. Create dcObject, and organization named dc=bachkhoa,dc=machibuya,dc=com (1 point)
 3. Add an organizationalUnit to it : ou=devservices,dc=bachkhoa,dc=machibuya,dc=com (1 point)
 4. Add a inetOrgPerson to it : cn=worker1,ou=devservices,dc=bachkhoa,dc=machibuya,dc=com (1 point)
