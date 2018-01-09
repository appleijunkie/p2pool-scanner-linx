Mooncoin Peer to Peer mining network public node scanner
===============================================

A simple NodeJS scanner that runs beside p2pool node and scans all IPs stored in addrs file. If IP has a public interface, then it is added to the list.  Users can connect to these nodes to mine on p2pool network without having to setup their own p2pool node.

You need to setup separate instances of this process with different config files to run on different crypto networks.

If HTTP port is provided in the configuration file, this application will publish the list on the given HTTP port.  Alternatively, it can be configured to upload page rendering to a destination FTP address to copy it to another host via SCP.

This project can be adapted to any cryptocurrency supported by p2pool by customizing:

These values in scanner.cfg:

p2pool_port <<< should be the default port used for the particular currency's p2pool
<br />currency
<br />addr_file
<br />init_file
<br />store_file

& these files:

p2pool-(currency)-init.txt <<< include a few peers currently available in the p2pool network
<br />resources/(currency).png <<< find a high quality png with alpha similiar to dimensions of mooncoin.png

To install & run:
<br />cd ~
<br />npm install https://github.com/appleijunkie/p2pool-scanner-mooncoin.git
<br />cd node_modules
<br />cd p2pool-scanner-mooncoin
<br />node scanner.js
