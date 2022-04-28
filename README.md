Zabbix-NUT-Template
===================

Zabbix Template for NUT(Network UPS Tools) for current Zabbix Versions.

Supported UPS: http://www.networkupstools.org/stable-hcl.html

Due to changes how Zabbix handles Value mappings the old Template was broken, i was able to fix it with some work for my new 6.0 installation, hope this will help others getting up and running quick :)


# Installation

```
git clone https://github.com/delin/Zabbix-NUT-Template.git
cd Zabbix-NUT-Template
sudo cp -r sh/ /etc/zabbix/
sudo cp zabbix_agentd.d/userparameter_nut.conf /etc/zabbix/zabbix_agentd.conf.d/
sudo service zabbix-agent restart
sudo service zabbix-server restart
```

After that login to Zabbix, go to Config->Templates and import the Templatefile.

Then you just add the Template to the Host that have a NUT installation running on them.
