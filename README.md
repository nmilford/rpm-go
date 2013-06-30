rpm-go
======

An RPM spec file to build and install the Go programming language.

This was spec was tweaked to skip tests that failed on RHEL/EL/CentOS 5. *shrug*

See: https://groups.google.com/forum/?fromgroups=#!topic/golang-nuts/QnjpPVc3V-g

To build:
 
`sudo yum -y install rpmdevtools ed bison mercurial && rpmdev-setuptree`
 
`wget https://raw.github.com/nmilford/rpm-go/master/go.spec -O ~/rpmbuild/SPECS/go.spec`

`wget https://go.googlecode.com/files/go1.1.1.src.tar.gz -O ~/rpmbuild/SOURCES/go1.1.1.src.tar.gz`
 
`rpmbuild -bb ~/rpmbuild/SPECS/go.spec`