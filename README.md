XP Framework Build System
=========================

Installation
------------
If all prerequisited are met, you can run the following command to install
the build system:

```
INST=`tempfile` && \
 wget --no-check-certificate \
 https://github.com/kiesel/xp-build-system/raw/master/installer.xml \
 -O $INST && \
 ant -f $INST && \
 rm $INST
```

This will install the system in

```
$HOME/
 ^- .ant/
   ^- lib/
   ^- xp-build/
```

For developers
--------------
To use the checked out version of this system, make sure you have
a regular version installed, then set environment variable
```XPBUILD_HOME``` to the ```src/``` folder.
