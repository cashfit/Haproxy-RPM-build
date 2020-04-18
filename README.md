# HAProxy RPM build
HAProxy RPM build

$ sudo yum install -y rpm-build rpmdevtools pcre-devel openssl-devel zlib-devel redhat-rpm-config gcc gcc-c++ make libstdc++-devel
$ rpmdev-setuptree

$ git clone https://github.com/kevholmes/haproxy-rpm.git

$ spectool -R -g haproxy.spec

$ cp haproxy-rpm/haproxy.spec ~/rpmbuild/SPECS/

$ rpmbuild -ba ~/rpmbuild/SPECS/haproxy.spec

$ cd ~/rpmbuild/RPMS/x86_64/

$ sudo yum install haproxy-1.5-devX.x86_64.rpm



