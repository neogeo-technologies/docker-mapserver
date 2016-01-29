# docker-mapserver

MapServer is build from Github source on the top of a Debian:latest base.
MapServer is build with fcgi support
Port 80 is open and MapServer is located at host/cgi-bin/mapserv.fcgi
There is a rewrite rule making /maps/map_name points to /cgi-bin/mapserv.fcgi?map=/var/maps/map_name.map
For easy mapfile edition, run the container with -v /some/place/on/your/host:/var/maps and put your own mapfile in /some/place/on/your/host, making the mapfiles available for the container through the volume sharing.
