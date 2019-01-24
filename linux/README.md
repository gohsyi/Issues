# Issues on Linux

**_E: Could not get lock /var/cache/apt/archives/lock - open (11: Resource temporarily unavailable)_**

**_E: Unable to lock directory /var/cache/apt/archives/_**

[solution] https://itsfoss.com/fix-ubuntu-install-error/

```
sudo rm /var/lib/apt/lists/lock
sudo rm /var/cache/apt/archives/lock
sudo rm /var/lib/dpkg/lock
sudo dpkg --configure -a
```

> While you are trying to install some package with apt command, some other package manager is running or an update is going on.
It is possible that you have Software Center open or another terminal is using the apt or apt-get commands.

------
