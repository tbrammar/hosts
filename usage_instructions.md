# Steps
1. Ensure all the dependancies have been installed: `pip3 install --user -r requirements.txt`
2. Review the `whitelist` file to ensure all domains you want to whitelist are present
3. Run the following command: `python3 updateHostsFile.py --replace --skipstatichosts --extensions porn --whitelist whitelist`
4. Upload to `tmp/hosts` in the router