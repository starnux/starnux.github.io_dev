+++
Categories = ["Development", "ip"]
Description = ""
Tags = ["Development", "ipv4", "ipv6"]
date = "2016-03-01T09:49:01+01:00"
title = "IP Address discovery service"

+++
Starnux.net offer a very simple service :

http://ip.starnux.net
<!--more-->

That prints the current IP address you are using :

````
Votre adresse IP est 91.64.244.31

Vous accedez a ce serveur en IPv4

JSON output : here
````

You can also get a JSON output at :


http://ip.starnux.net/json.php


```
{ "ip": "91.64.244.31", "protocol": "IPv4" }
```

And even force the IPv6 address at :

http://ip6.starnux.net

and get :
````
Votre adresse IP est 2001:41d1:b:5390::

Vous accedez a ce serveur en IPv6

JSON output : here
````

Same for JSON :

http://ip6.starnux.net/json.php


```
{ "ip": "2001:41d1:b:5390::", "protocol": "IPv6" }
```

And you can automate it from the terminal by running :
```
$ wget -q http://ip6.starnux.net/json.php -O - | json_pp
{
	   "protocol" : "IPv6",
           "ip" : "2001:42d0:b:5291::"
}
```

And interpret the JSON in python, ruby, go, ... whatever !
