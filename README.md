# EndeavourOS-ISO

[![Maintenance](https://img.shields.io/maintenance/yes/2024.svg)]()

This ISO is based on hugely modified Arch-ISO to provide Installation Environment for EndeavourOS.  
More info at [EndeavourOS-GitHub-Development](https://endeavouros-team.github.io/EndeavourOS-Development/)

### Development source

- [EndeavourOS-ISO source](https://github.com/endeavouros-team/EndeavourOS-ISO) (Live environment with KDE-Desktop)
- [Calamares {EndeavourOS fork}](https://github.com/endeavouros-team/calamares) (installer framework)


### Base source

- [Arch-ISO](https://gitlab.archlinux.org/archlinux/archiso)
- [Calamares](https://github.com/calamares/calamares)



# Boot options

Systemd-boot for UEFI systems:  
<img src="https://raw.githubusercontent.com/endeavouros-team/screenshots/master/Apollo/apollo-systemdboot.png" alt="drawing" width="600"/>

Bios-boot (syslinux) for legacy systems:  
<img src="https://raw.githubusercontent.com/endeavouros-team/screenshots/master/Apollo/apollo-syslinux.png" alt="drawing" width="600"/>


##### Build

```
./prepare.sh
```

~~~
sudo ./mkarchiso -v "."
~~~

**or with log:**

~~~
sudo ./mkarchiso -v "." 2>&1 | tee "eosiso_$(date -u +'%Y.%m.%d-%H:%M').log"
~~~

##### The .iso file appears in the `out` directory...

to reset build structure:

```
sudo ./reset.sh
```


## Advanced

To install locally built packages on ISO, put the packages inside the following directory:

~~~
airootfs/root/packages
~~~

Packages will be installed and the directory will be cleaned up after that.
