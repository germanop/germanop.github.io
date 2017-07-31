# Using Git with Socks

Say a socks has been created on port 5555 using ```ssh``` with the following
```
ssh -f -N somehost -D 5555
```
adding the following to your git configuration file will make ```git``` aware
if the socks.
```
[http]
       proxy = socks5h://localhost:5555
```

The above configuration works for both ```http``` and ```https```.

Note the ```h``` at the end of ```socks5h```: this will make git
use the socks for DNS queries, too.
