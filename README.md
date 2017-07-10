# GitHub Tutorials:

- https://www.youtube.com/watch?v=0fKg7e37bQE&t=24s
- https://www.youtube.com/watch?v=oFYyTZwMyAg

# Python 3 with virtual environment setup guide
- http://www.marinamele.com/2014/07/install-python3-on-mac-os-x-and-use-virtualenv-and-virtualenvwrapper.html
- http://python-guide-pt-br.readthedocs.io/en/latest/dev/virtualenvs/
- https://stackoverflow.com/questions/12647266/where-is-virtualenvwrapper-sh-after-pip-install
- https://stackoverflow.com/questions/33216679/usr-bin-python3-error-while-finding-spec-for-virtualenvwrapper-hook-loader

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

# Change password in SNMP client using snmpusm:
- http://www.net-snmp.org/docs/man/snmpusm.html

# SNMP commands tutorial
- https://docs.oracle.com/cd/E19201-01/820-6413-13/SNMP_commands_reference_appendix.html
- http://snmpsim.sourceforge.net/public-snmp-simulator.html
snmpwalk -v 2c -c public 192.168.1.78 system

snmpget -v 2c -c public 192.168.56.103 sysUpTime.0

snmpget -u demo -l authPriv -a MD5 -x DES -A 12345678 -X 12345678 192.168.56.103 sysUpTime.0


# SNMP setup tutorial:
- https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-an-snmp-daemon-and-client-on-ubuntu-14-04#install-the-snmp-daemon-and-utilities
- http://xmodulo.com/configure-snmpv3-ubuntu-centos-cisco.html
- http://ghost-armsultan.rhcloud.com/install-and-configure-snmp-on-ubuntu-and-debian/
- https://www.fineconnection.com/how_to_install_and_enable_snmpv3_on_a_linux_system_for_authentication_en_encryption_testing-2/
- http://www.bauer-power.net/2012/10/how-to-configure-snmp-for-ubuntu-in-5.html#.WUAmRRPyvBJ
- http://www.it-slav.net/blogs/2009/02/05/install-and-configure-snmp-on-ubuntu/


# SNMP create/modify users
- http://www.net-snmp.org/docs/man/snmpusm.html
snmpusm -u demo -l authPriv -a MD5 -x DES -A temp_password -X temp_password 192.168.56.103 passwd temp_password 12345678
snmpusm -u bootstrap -l authPriv -a MD5 -x DES -A temp_password -X temp_password 192.168.56.101 create demo bootstrap
snmpusm -u demo -l authPriv -a MD5 -x DES -A 12345678 -X 12345678 192.168.56.103 delete bootstrap

# vim python support
- https://askubuntu.com/questions/775059/vim-python-support-on-ubuntu-16-04
- https://github.com/python-mode/python-mode/issues/687
- https://realpython.com/blog/python/vim-and-python-a-match-made-in-heaven/#vim-extensions
- https://github.com/amix/vimrc
- https://github.com/amix/vimrc
- https://github.com/j1z0/vim-config/blob/master/vimrc
- https://github.com/python-mode/python-mode/issues/687

# Vim tutorials
- https://stackoverflow.com/questions/5400806/what-are-the-most-used-vim-commands-keypresses/5400978#5400978
- https://github.com/Valloric/YouCompleteMe
- http://www.openvim.com/
- https://vim-adventures.com/

# SNMP Agent start and stop
- https://www.ibm.com/support/knowledgecenter/en/ST9MBR_1.2.1/ltfs_ee_start_stop_snmp.html

# Writing an SNMP Agent With a Custom MIB Using Pysnmp
- http://www.nealc.com/blog/blog/2013/02/23/writing-an-snmp-agent-with-a-custom-mib-using-pysnmp/

# Make SNMP Scapy Flooding:
- http://alibay.com.tr/approaching-danger-snmp-amplification-attacks/
- http://www.nothink.org/misc/snmp_reflected.php
- http://www.packetlevel.ch/html/scapy/scapychw.html
- http://www.secdev.org/projects/scapy/doc/advanced_usage.html
- http://www.nothink.org/misc/snmp_reflected.php

# Tcpdump filters
- http://biot.com/capstats/bpf.html
- http://alumni.cs.ucr.edu/~marios/ethereal-tcpdump.pdf

# Logstash Grok
- http://grokdebug.herokuapp.com/
- http://grokconstructor.appspot.com/do/automatic
- https://github.com/kkos/oniguruma/blob/master/doc/RE

# Login to AWS instance
sudo ssh -i ~/.ssh/vishnu_honeyot_key_pair.pem ubuntu@34.212.187.81

