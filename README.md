# The RPM-416 configuration for prometheus modbus_exporter

![rpm-416.jpg](rpm-416.jpg)

The [RPM-416](https://novatek-electro.com/en/products/recorder-of-electric-process/data-logger-rpm-416.html) can be connected to a facility network via ethernet (modbus/tcp) and send data to the prometheus, for example.

This project contain the modbus.yml file for [modbus_exporter](https://github.com/RichiH/modbus_exporter)
Also i've written simple systemd unit for node exporter. 

Enjoy :)

### Add systemd unit

Copy `modbus-exporter.service` to `/etc/systemd/system/`
```
sudo cp modbus-exporter.service /etc/systemd/system
```
Then reload the daemon config 
```
sudo systemctl daemon-reload
```
And run your service
```
sudo systemctl start modbus-exporter
```