
# For virtualbox

* Start your vagrant project and let the provisioning run
* Shut it down
* Do `vagrant package --output 'mybox_0.1.0.box'`
* Upload it to your webserver
* Create a whatever.json with the following content
```
 {
    "name": "project/mybox",
    "description": "This box does something",
    "versions": [{
        "version": "0.1.0",
        "providers": [{
                "name": "virtualbox",
                "url": "https://boxes.example.com/path/to/mybox_0.1.0.box",
                "checksum_type": "sha1",
                "checksum": "b58676b903c78aa275da3117d5cb31d4217aaa23"
        }]
    },
    {
        "version": "0.2.0",
        "providers": [{
                "name": "virtualbox",
                "url": "https://boxes.example.com/path/to/mybox_0.2.0.box",
                "checksum_type": "sha1",
                "checksum": "72a0a24d285728aed455f366321a29f50096c421"
        }]           
    }
]
}
```
* (create the checksum whith the sha1sum command line tool)
* Set the URL in your Vagrantfile to https://boxes.example.com/whatever.json and the name to "project/mybox"
* done

# For lxc

* do the same as above, just with `name: lxc`




