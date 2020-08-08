# How-to-create-an-Access-Point-from-the-current-WiFi-connection-
How to create an Access Point from the current WiFi connection?


# How do I share the Internet of the currently connected network over a hotspot in Linux?

You should use `create_ap`


### Install the dependencies :

`sudo apt-get install dnsmasq haveged hostapd build-essential`

To install `create_ap` run:

`git clone https://github.com/oblique/create_ap`
`cd create_ap`
`sudo make install`

### enable/start the service:

`service create_ap start`


### To check the status run:

`service create_ap status`

### Using the `systemd` features (it is not available on Ubuntu 14.04):

`sudo systemctl start create_ap.service`
`sudo systemctl enable create_ap.service`

### Create the AP
To create your access point run:

`sudo create_ap wlan0 wlan0 MyAccessPoint MyPassPhrase`



`











