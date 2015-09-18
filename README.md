# Rippled RPM package builder

## Setup
On a fresh instance of Red Hat Enterprise Linux 7 install the following
packages to be able to build RPMs:

```
sudo yum install -y rpm-build
```

## Usage

First copy the rippled source code into `~/rpmbuild/SOURCES`

```
cp /tmp/rippled.gz /home/$USER/rpmbuild/SOURCES/
```

Next copy the spec file into `~/rpmbuild/SPECS`

```
cd /tmp
git clone https://github.com/stevenzeiler/rippled-rpm-builder.git
cp rippled.spec ~/rpmbuild/SPECS/
```

Then run the `rpmbuild` command to build rippled from the RPM spec file

```
cd ~/rpmbuild/SPECS/ && rpmbuild rippled.spec
```

