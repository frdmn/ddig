Direct dig (ddig)
===================

Simple bash script to query the actual responsible DNS server of a specific domain/hostname.

# Installation

    cd /tmp
    git clone https://github.com/frdmn/direect-dig.git
    sudo mv direct-dig/bin/ddig /usr/bin/ddig
    sudo chmod +x /usr/bin/ddig

# Usage

    $ bin/ddig frd.mn
    1. responsible DNS:   dns2.iwelt-ag.net.
       resolved hostname: 82.196.7.61
    2. responsible DNS:   dns.iwelt-ag.net.
       resolved hostname: 82.196.7.61
    3. responsible DNS:   dns3.iwelt-ag.de.
       resolved hostname: 82.196.7.61    