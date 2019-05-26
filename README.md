# hellohs (Hello Homestead)

hellohs is a sample project that uses Homestead to run a simple php project in a popular stack, some of the pre-installed software includes:

* Ubuntu
* Git
* PHP
* Nginx
* MySQL
* ...

Full list and versions https://laravel.com/docs/5.8/homestead

hellohs in my setup on MacOS uses virtualbox.

If you want to run this setup on Windows you will need to fix a few paths in Homestead.yaml and change / to \ etc

A few notes on network and ports in this setup:

the /etc/hosts has a mapping from 192.168.10.10 to hellohs.local, so that you can use the friendly name to open the site in the browser

```
##
# Host Database
#
# localhost is used to configure the loopback interface
# when the system is booting.  Do not change this entry.
##
192.168.10.10   hellohs.local
```

Also, inside the vm the /etc/hosts has changed the mapping of localhost to 

```
0.0.0.0.0   localhost
```

As for source control, the structure is 

```
/           (root of git project hellohs)
/webroot    (root of web site)
/host       (various host files in the host OS)
```

The drawback of this git structure is that (with git clone) you get host files on the guest which can be deleted.



