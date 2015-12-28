# ddig

[![Current tag](http://img.shields.io/github/tag/frdmn/ddig.svg)](https://github.com/frdmn/ddig/tags) [![Repository issues](http://issuestats.com/github/frdmn/ddig/badge/issue)](http://issuestats.com/github/frdmn/ddig) [![Flattr this repository](http://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=frdmn&url=https://github.com/frdmn/ddig)

Simple bash script to query each actual responsible DNS server directly for a specific domain/hostname.

## Installation

    brew tap frdmn/homebrew-formulas
    brew install ddig

## Usage

    $ ddig frd.mn
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

---

    $ dig +short frd.mn @dns3.iwelt-ag.de.
    82.196.7.61

---

    $ dig +short frd.mn @dns2.iwelt-ag.net.
    82.196.7.61

---
    
    $ dig +short frd.mn @dns.iwelt-ag.net.
    82.196.7.61

## Contributing

1. Fork it
2. Create your feature branch: `git checkout -b feature/my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin feature/my-new-feature`
5. Submit a pull request

## Version

1.2.0

## License

[MIT](LICENSE)
