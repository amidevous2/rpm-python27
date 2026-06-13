rpm-python27
============

An RPM spec file build and alt-install Python 2.7 on RHEL.

To Build:


`sudo dnf -y install rpmdevtools && rpmdev-setuptree`

`wget https://github.com/amidevous2/rpm-python27/raw/refs/heads/master/python27.spec -O $(rpm --eval '%{_specdir}')/python27.spec`

`sudo dnf -y build-dep ~/rpmbuild/SPECS/python27.spec`

`spectool --get-files --sourcedir $(rpm --eval '%{_specdir}')/python27.spec`

`rpmbuild -ba $(rpm --eval '%{_specdir}')/python27.spec`
