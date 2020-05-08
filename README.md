# docker-commands

Fikse DNS- og HTTP-trøbbel en gang for alle:
Sjekke nettverk og DNS på Ubuntu:
Bra bloggpost om temaet: https://development.robinwinslow.uk/2016/06/23/fix-docker-networking-dns/
	* nmcli device -> Lister devices
	* nmcli device show <name> -> Lister info om device. Se etter DNS-info.
Evt: nmcli device show | grep -i dns
	* sudo vim /etc/docker/daemon.json
	* {"dns":["<ipaddr1>", "<ipaddr2>"],"insecure-registries":["old-dockerhub.spk.no:5000"]}
	* sudo service docker restart
