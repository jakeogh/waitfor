**waitfor - Run command over until it exits 0.**

https://github.com/jakeogh/waitfor

**Use:**

simple example (wait for the net to be available, then do something):
```
$ waitfor
waitfor interval command [exit_status]

$ waitfor 2 "ping -c1 1.1.1.1" && wget http://www.wrh.noaa.gov/images/twc/granalyst/kemx_cr_0.jpg
```

**Theory:**

 1. Run command, if command exits 0, then exit 0. If it does not, wait the specified interval (in seconds) and try again.

**General Install:**

Place in $PATH

```
    git clone https://github.com/jakeogh/waitfor
    sudo cp waitfor/waitfor /usr/bin/waitfor
```

**Gentoo Install:**
```
   su
   layman -o https://raw.githubusercontent.com/jakeogh/jakeogh/master/jakeogh.xml -f -a jakeogh
   echo "source /var/lib/layman/make.conf" >> /etc/portage/make.conf
   layman -S
   emerge waitfor
```


