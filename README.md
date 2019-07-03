# Docs
1	Download 
	https://downloads.raspberrypi.org/raspbian_lite_latest
	
2	write img to sd card
	
3	if running headless put a text file on the root of the sd card with the name : ssh
	
4	insert the sd card and plug in to power and ethernet , power it on
	
5	find the ip address in your dhcp server / router
	
6	log in to the pi via ssh pi@192.168.1.xxx  with the password of : raspberry
	
	
7	sudo  raspi-config
	
8	curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
	sudo apt-get install -y nodejs
	
9	passwd pi ; when promted enter the password : pi-racer
	
10	apt install vim -y
	
11	vim /etc/hostname ; replace contents with : pi-racer
	
12	follow this tutorial to turn the wireless access point on. The SSID and the password should be pi-racer
	https://learn.sparkfun.com/tutorials/setting-up-a-raspberry-pi-3-as-an-access-point/all
	
13	exit ; to exit out of root
	
14	install nodejs & node-red
	bash <(curl -sL https://raw.githubusercontent.com/node-red/raspbian-deb-package/master/resources/update-nodejs-and-nodered)
	
15	node-red-start ; to make the setings.js file
	
16	press : control + c  ; to stop node red
	
17	vim .node-red/settings.js
	lines to chenge
	
	change the port to 80
	"module.exports = {
    // the tcp port that the Node-RED web server is listening on
    uiPort: process.env.PORT || 1880,"
	
	// When httpAdminRoot is used to move the UI to a different root path, the
	    // following property can be used to identify a directory of static content
	    // that should be served at http://localhost:1880/.
	    //httpStatic: '/home/nol/node-red-static/',
