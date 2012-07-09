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

You need to supply a `$HOME/.ivy2/ivysettings-repositories.xml` file:

```xml
<?xml version="1.0"?>
<ivysettings>
        <resolvers>
                <chain name="xp-shared-snapshots">
                        <resolver ref="xp-public-snapshots"/>
                </chain>
                <chain name="xp-shared-milestones">
                        <resolver ref="xp-public-milestones"/>
                </chain>
                <chain name="xp-shared-releases">
                        <resolver ref="xp-public-releases"/>
                </chain>
        </resolvers>
</ivysettings>
```

This file can later be adjusted to enable use of a local shared team repository.


For developers
--------------
To use the checked out version of this system, make sure you have
a regular version installed, then set environment variable
```XPBUILD_HOME``` to the ```src/``` folder.
