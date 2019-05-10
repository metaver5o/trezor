# how to use it: 
` git clone ` <br>
` cd offline-wallet ` <br>
` docker build -t trezor:local . ` <br>
` docker run -ti --rm --privileged -v /dev/bus/usb:/dev/bus/usb -p 8000:8000 trezor:local ` <br>
* access https://localhost:8000

 <br><br><br>
 -  don't forget to download the trezor wallet source file, or <br>
    just uncomment the wget command in dockerfile
 <br><br><br>

# not working for OSX
you must user docker-machine instead: <br>
` docker-machine create --driver virtualbox default ` <br>
<br><br>

* Add the USB device to the new VM <br>
Stop the default VM first so that you can change its settings in VirtualBox: <br> `docker-machine stop` <br>
From VirtualBox settings for `default` VM, enable USB Controller and add the connected USB device.<br>
Start the VM again: `docker-machine start` <br><br>

* Tell Docker to talk to the VM <br>
We need to set a few environment variables to tell Docker to use the new VM instead of <br> the native mode. docker-machine env commands tells us how to do that:<br><br>

`$ docker-machine env default` <br>
`export DOCKER_TLS_VERIFY="1"` <br>
`export DOCKER_HOST="tcp://192.168.99.100:2376"` <br>
`export DOCKER_CERT_PATH="/Users/milad/.docker/machine/machines/default"` <br>
`export DOCKER_MACHINE_NAME="default"` <br>
`# Run this command to configure your shell:` <br>
`# eval $(docker-machine env default)` <br><br>

So all we need to do is: eval "$(docker-machine env default)"


