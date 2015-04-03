google-hosts
============

[**What**](#what) | [**How**](#how) | [**Must**](#must) | [**Contributing**](#contributing) | [**License**](#license) | [**Donate**](#donate)

What
---

This projects can help you visit google service. (Only for research and study)

How
---

**`find.sh` find ip detail from CIDR**

```
$ cd google-hosts/scripts

# find ip from 192.168.1.1/24
$ ./find.sh 192.168.1.1/24
```

**`filter.sh`filter IP from output directory(generate by find.sh)for some domain**

```
$ cd google-hosts/scripts

# filter IP for *.google.com
$ ./filter.sh *.google.com

# filter IP for mail.google.com
$ ./filter.sh mail.google.com
```

**`use.sh` use IP for some domain and update hosts.all**

```
$ cd google-hosts/scripts

# use 192.168.1.1 for *.google.com 
$ ./use.sh *.google.com 192.168.1.1

# use 192.168.1.1 for mail.google.com 
$ ./use.sh mail.google.com 192.168.1.1
```

**`select.sh` run filter.sh, use.sh, use the best IP for domains in hosts.all**

```
$ cd google-hosts/scripts
$ ./select.sh
```

**`apply.sh` use hosts.all to update ../hosts**

```
$ cd google-hosts/scripts
$ ./apply.sh
```

**`auto.sh` find CIDR and run find.sh, select.sh, apply.sh**

```
$ cd google-hosts/scripts
$ ./auto.sh
```

Explanation for output 

| IP | LOSS | TIME | SSL |
| --- | --- | --- | --- |
| IP | packet loss | ping time | ssl domain |

Must
---

* Uuse regular DNS. e.g: google dns + opendns
* Use international google. Make google no country redirect: <https://www.google.com/ncr>
* Use `https`

Contributing
---

* vim:ts=4:sw=4:expandtab:ff=unix:encoding=utf8
* Please create your pull request on `develop` branch

License
---

Licensed under The [MIT][MIT] License

Donate
---

* Alipay/Paypal: `cloud@txthinking.com`
* Bitcoin: `17PCWDxxJ1wmNb9YmRrTJTXd4dvcJvWPVN`
* [Donors][Donors]

[hosts]: http://freedom.txthinking.com/hosts
[fuckGFW-64.exe]: http://freedom.txthinking.com/fuckGFW-64.exe
[fuckGFW-32.exe]: http://freedom.txthinking.com/fuckGFW-32.exe
[MIT]: https://github.com/txthinking/google-hosts/blob/master/LICENSE
[Donors]: https://github.com/txthinking/google-hosts/blob/master/DONORS.md
