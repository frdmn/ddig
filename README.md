Direct dig (ddig)
===================

Simple bash script to query each actual responsible DNS server for a specific domain/hostname.

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

instead of

    $ dig +short ns frd.mn
    dns3.iwelt-ag.de.
    dns2.iwelt-ag.net.
    dns.iwelt-ag.net.

    $ dig +short frd.mn @dns3.iwelt-ag.de.
    82.196.7.61

    $ dig +short frd.mn @dns2.iwelt-ag.net.
    82.196.7.61
    
    $ dig +short frd.mn @dns.iwelt-ag.net.
    82.196.7.61