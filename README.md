# Firebird2.5.9-ClearLinux
This repository contains compiled binarys to Clear Linux (latest gcc, with clearlinux cflags optimizations).
The default install dir is on /usr/local/firebird. So, attached is 3 zips from this compilation. 
To execute Super Classic Server, do: /usr/local/firebird/bin/fbguard -daemon -forever -pidfile /var/run/fb.pid
For Classic, depends on xinited and socket systemd unit file is not working. 
User: SYSDBA
Password: sysdba
Inside bin you have the scripts to change de password.
Error: If you got dependency error, install devpkg-icu4c and devpkg-libedit. 

If you want compile (i recommend 50GB disc):
git the firebird version from github. 
In clear linux do: 
swupd bundle-add R-extras-dev dev-utils-dev devpkg-icu4c devpkg-libedit devpkg-newt perl-extras
In firebird folder do:
./configure  --with-system-icu --with-system-editline
make
make install
make clean (to clean sources after installation wizard). 

See configure to see options. 
