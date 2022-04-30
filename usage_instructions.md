# Steps
1. Ensure all the dependancies have been installed: `pip3 install --user -r requirements.txt`
2. Review the `whitelist` file to ensure all domains you want to whitelist are present
3. Run the following command: `python3 updateHostsFile.py --replace --skipstatichosts --extensions porn --whitelist whitelist`
4. Upload outputted `hosts` file to `tmp/hosts/` in the router e.g. `scp hosts root@192.168.1.1:/tmp/hosts/porn`
5. Then run `/etc/init.d/dnsmasq restart`
6. Check in the logs to see that its loaded it ok by running `logread` and checking for a line like `Sat Apr 30 08:50:43 2022 daemon.info dnsmasq[7703]: read /tmp/hosts/porn - 142886 addresses`