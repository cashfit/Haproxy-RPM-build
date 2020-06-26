# HAProxy RPM build

$ sudo yum install -y rpm-build rpmdevtools pcre-devel openssl-devel zlib-devel redhat-rpm-config gcc gcc-c++ make libstdc++-devel  
$ rpmdev-setuptree   
$ cp haproxy.spec ~/rpmbuild/SPECS/  
$ rpmbuild -ba ~/rpmbuild/SPECS/haproxy.spec  
$ cd ~/rpmbuild/RPMS/x86_64/  
$ sudo yum install haproxy-1.5-devX.x86_64.rpm 

# Keepalived RPM build

$ yum install rpm-build rpmdevtools rpm-sign gcc pcre-devel expect  
$ ./configure -prefix=/usr/local/keepalived  
$ make rpm  

#comments lines below in keepalived.spec file, if make error  
#CONFIG_OPTS="$CONFIG_OPTS --disable-iptables"  
#CONFIG_OPTS="$CONFIG_OPTS --disable-libiptc”  
#CONFIG_OPTS="$CONFIG_OPTS --disable-libipset”  


