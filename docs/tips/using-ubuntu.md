# Using Ubuntu instead of Debian

Drifter uses Debian Jessie boxes by default. But you can also use Ubuntu Trusty (which is tested by us), or any other box.

Add the following to `virtualization/parameters.yml` and rebuild the box (`vagrant destroy -f && vagrant up`)

```
lxc_box_name: "fgrehm/trusty64-lxc"
lxc_box_url: 
vbox_box_name: "ubuntu/trusty64"
vbox_box_url:
```

