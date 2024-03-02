# qubes-plymouth-themes
Plymouth themes for Qubes OS

The themes needs to be installed in dom0.
The themes only allows you to use the luks password, if you are using any other type of authentication like AEM don't expect it to work.

![qubes-ani-01](https://github.com/renehoj/qubes-plymouth-themes/assets/108547507/8b44e898-54ea-40b5-8cdc-43e3bf2d60c8)

qubes-theme-ani-01

![qubes-ani-02](https://github.com/renehoj/qubes-plymouth-themes/assets/108547507/04fc0949-d6d3-4e40-853e-f92d041cce41)

qubes-theme-ani-02


![qubes-ani-03](https://github.com/renehoj/qubes-plymouth-themes/assets/108547507/b88fa612-3e25-4b11-9557-37c1c93eef52)

qubes-theme-ani-03

![qubes-ani-04](https://github.com/renehoj/qubes-plymouth-themes/assets/108547507/0f4f881e-d589-4f1d-8ec2-b545a748fcc9)

qubes-theme-ani-04

# Install
Clone the repo in a domU and copy it to dom0, and in dom0 copy qubes-theme to /usr/share/plymouth/themes

```
$ sudo cp -r qubes-theme-ani-XX /usr/share/plymouth/themes
```

Check if the theme is avaiable, qubes-theme-ani-XX should be in the theme list
```
$ plymouth-set-default-theme -l
```
Set the theme active
```
$ sudo plymouth-set-default-theme -R qubes-theme-ani-XX
```

# Reinstall default theme
```
$ sudo plymouth-set-default-theme -R qubes-dark
```
# Disaster recovery
If your system doesn't boot you need to disable plymouth, and and enable the default theme.

At the grub boot prompt use e to edit the boot config, add the following to the boot parameters

```
rd.plymouth=0 plymouth.enable=0
```
