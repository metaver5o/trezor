# how to use it: 
` git clone ` <br>
` cd offline-wallet ` <br>
` docker build -t trezor:local . ` <br>
` docker run -ti --rm --privileged -v /dev/bus/usb:/dev/bus/usb -p 8000:8000 trezor:local ` <br>
* access https://localhost:8000

 <br><br><br>
 -  don't forget to download the trezor wallet source file, or <br>
    just uncomment the wget command in dockerfile