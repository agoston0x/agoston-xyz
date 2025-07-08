Walrus Sites Showcase
---------------------

This Project contains 3 examples of what is possible with static sites when served decentrally on Walrus, using cloudless compute by Fluence.

For deployment, walrus site-builder binary was used locally along with a sui client. 

In order to resolve a SuiNS domain (eg. agoston.sui to agoston.xyz), a portal is needed.

This portal is run on a cloudless compute instance provided by Fluence. The following steps are necessary to run the portal:

- set up and start VM on Fluence, with ports 443 and 80 open
- set up SSH in local environment and SSH into the instance
- set DNS records in domain provider's interface (eg. Godaddy, namecheap, etc.)
- run package manager update (eg. sudo apt update) on instance
- install docker using the official docker install guide
- clone the git repo of the walrus portal by mysten labs (https://github.com/MystenLabs/walrus-sites.git), build docker image
- install and set up nginx to accept connections on port 443, get ssl certificate according to official guide
- enable and set up ufw according to official guides
- point suiNS domain to own domain
- run docker container
- if content has been published o.k. to walrus sites, simply enjoy the decentralized permissionless web!

