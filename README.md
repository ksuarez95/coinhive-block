# CoinHive-Block

To block the Malware domains of CoinHive or related JS bitcoin miners.

This does not block AuthedMine.com because they ask for permission. This is only for the rogue implementations of it.

## Why block (rogue) JS Crypto Miners?
We believe that using a JavaScript Bitcoin miner on your site without end-users explicit permission is **Malware**.

Fortunately, CoinHive realized how webmasters were implementing their miners without ever asking the end-user. They concluded:

>We're a bit saddened to see that some of our customers integrate CoinHive into their pages without disclosing to their users what's going on, let alone asking for their permission. We believe there's so much more potential for our solution, but we have to be respectful to our end users.
>
>We hope we can convince website owners to integrate the miner in a way that is more meaningful and honest to their users. ...

[source][4]

In September 2017, The PirateBay secretly added the JS miner without any user disclosure. Adding secret miners makes your site behave as a malware. 

While it may seem like a great solution for the dying ads market, it's sad that the webmasters implemented it like a malware, without considering the end-user.

## How to use:

* Program's that supports hostfile format such as `adaway`, `ublock orgin`, `DNS66` you can use: `https://raw.githubusercontent.com/Marfjeh/coinhive-block/master/hostfile.txt`
* Or you prefer to use a adblock-filter list: `https://raw.githubusercontent.com/Marfjeh/coinhive-block/master/adblock.txt`

Those lists gets updated on every commit, so you dont need to change them anymore after release.

## My domain is in this list. What now?
If you believe this is a false-positive which can happen, please make an `issue` about this.
and we will resolve this ASAP.

Make also sure that your webhost isnt compromised.


## I'm using CoinHive on my site. What now?
We suggest asking the end-user for opt-in before operation. It's the user's choice whether they wish to participate. 
If they don't, please respect their decision.

[AuthedMine.com][3] adds a pop-up asking for permission to authorize it. That's why we won't block AuthedMine.

AntiMalwareBytes has also taken steps to block JS Miners stating:
>Why are we blocking it?
>
>We do not claim that CoinHive is malicious, or even necessarily a bad idea. The concept of allowing folks to opt-in for an alternative to advertising, which has been plagued by everything from fake news to malvertising, is a noble one. The execution of it is another story.
>
>The reason we block CoinHive is because there are site owners who do not ask for their users’ permission to start running CPU-gorging applications on their systems. A regular Bitcoin miner could be incredibly simple or a powerhouse, depending on how much computing the user running the miner wants to use. The JavaScript version of a miner allows customization of how much mining to do, per user system, but leaves that up to the site owner, who may want to slow down your computer experience to a crawl.

[source][1]

## Credits

Some of the domains in this repo are from [gitlab.com/ZeroDot1/CoinBlockerLists](https://zerodot1.gitlab.io/CoinBlockerListsWeb/index.html)
Big shoutout to these guys. They're not just blocking JS miners, but every crypto-pool to make mining inside your network impossible. Very neat stuff for SysAdmins!


# Compiling
To compile the files yourself: Several ways are listed below:

### How to compile (Linux)
```BASH
git clone https://github.com/Marfjeh/coinhive-block.git
cd coinhive-block
sudo make
sudo make install
```

### How to install (Windows Python) (as admin)
```BASH
git clone https://github.com/Marfjeh/coinhive-block.git
cd coinhive-block/compilers/src
python make.py
cd ../../
copy /b %windir%/drivers/etc/hosts + hostfile %windir%/drivers/etc/hosts 
```

### How to install (Windows Binary) (as admin)
```BASH
git clone https://github.com/Marfjeh/coinhive-block.git or git clone git@github.com:Marfjeh/coinhive-block.git
cd coinhive-block/compilers/bin
compile.exe
cd ../../
copy /b %windir%/drivers/etc/hosts + hostfile %windir%/drivers/etc/hosts 
```

### Contributing
1. Clone the repository `git@github.com:Marfjeh/coinhive-block.git`
2. Change directory to the coin-hice block folder `cd coinhive-block`
3. Add new domains to the `domains` and start contributing!
4. Make a pull-request.


## License

This project is released under the [MIT License][2]

[1]: https://blog.malwarebytes.com/security-world/2017/10/why-is-malwarebytes-blocking-coinhive/
[2]: https://github.com/Marfjeh/coinhive-block/blob/master/LICENSE.md
[3]: https://www.authedmine.com
[4]: https://coinhive.com/blog/status-report
[7]: https://github.com/Marfjeh/coinhive-block/wiki/Installation-on-windows-Linux-Mac-OSX
[8]: https://zerodot1.gitlab.io/CoinBlockerListsWeb/index.html
