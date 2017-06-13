# GitHub Tutorials:

- https://www.youtube.com/watch?v=0fKg7e37bQE&t=24s
- https://www.youtube.com/watch?v=oFYyTZwMyAg

# Python 3 with virtual environment setup guide
- http://www.marinamele.com/2014/07/install-python3-on-mac-os-x-and-use-virtualenv-and-virtualenvwrapper.html

# Pip install: There was a problem confirming the ssl certificate: [SSL: CERTIFICATE_VERIFY_FAILED]
pip install puresnmp --trusted-host pypi.python.org

# Bridged network in VirtualBox - mac OSX host and Ubuntu Client
- https://superuser.com/questions/152043/configuring-virtualbox-host-only-networking-osx-host-ubuntu-guest?rq=1
➜  ~ cat /etc/network/interfaces
#interfaces(5) file used by ifup(8) and ifdown(8)
auto lo
iface lo inet loopback

auto enp0s3
iface enp0s3 inet static
	address 172.17.1.25
	netmask 255.255.255.0
	broadcast 172.17.1.255
	network 172.17.1.0

auto enp0s8
iface enp0s8 inet dhcp

MacOSX: ifconfig information:
en0: flags=8863<UP,BROADCAST,SMART,RUNNING,SIMPLEX,MULTICAST> mtu 1500
	ether a0:99:9b:09:dc:39
	inet6 fe80::4c4:9f9b:c65b:a88b%en0 prefixlen 64 secured scopeid 0x4
	inet 172.17.1.120 netmask 0xfffffc00 broadcast 172.17.3.255
	nd6 options=201<PERFORMNUD,DAD>
	media: autoselect
	status: active
  
  Ubuntu ifConfig Information:
  enp0s3    Link encap:Ethernet  HWaddr 08:00:27:00:10:0d  
          inet addr:172.17.1.25  Bcast:172.17.1.255  Mask:255.255.255.0
          inet6 addr: fe80::a00:27ff:fe00:100d/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:6 errors:0 dropped:0 overruns:0 frame:0
          TX packets:41 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000 
          RX bytes:379 (379.0 B)  TX bytes:4661 (4.6 KB)
          Interrupt:19 Base address:0xd020 

# Host-only networks:
- https://www.youtube.com/watch?v=Jk5Kfm2-Muk
- https://superuser.com/questions/152043/configuring-virtualbox-host-only-networking-osx-host-ubuntu-guest?rq=1
- http://christophermaier.name/2010/09/01/host-only-networking-with-virtualbox/
- https://forums.virtualbox.org/viewtopic.php?f=8&t=34396
- https://superuser.com/questions/429405/how-can-i-get-virtualbox-to-run-with-a-hosts-only-adapter
- https://superuser.com/questions/119732/how-to-do-networking-between-virtual-machines-in-virtualbox
