# Install Rotor
.PHONY: extract install uninstall


install: /var/log/rotor extract
	sudo install -m 0644 _libnss/libnss_rotor.so.2 /lib
	sudo /sbin/ldconfig /lib

/var/log/rotor:
	sudo mkdir /var/log/rotor

extract:
	sudo mkdir /opt/rotor && sudo tar --no-same-owner -xvf _rotor/rotor-0.3.0.tar.gz -C /opt/rotor

uninstall:
	sudo rm -rf /opt/rotor
	sudo rm /lib/libnss_rotor.so.2
	sudo /sbin/ldconfig /lib
