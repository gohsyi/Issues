# Issues on Linux

## Process still exists after I use kill \<pid\>_

Processes can ignore some signals. If you send SIGKILL it will not be able to ignore it (and neither catch it to do cleanups). Try:

kill -9 {PID}


## Passwordless login on Mac OS

First, add this in `~/.ssh/config`
```
Host <alias>
     Hostname <address>
     User <your login username>
     Port <port number>
```

Then, run this on localhost
```
ssh-copy-id -i ~/.ssh/id_rsa.pub <alias>
```

Now, you can login your server with:
```
ssh <alias>
```

------

## Change apt-get sources

First, check which version of Ubuntu you are using.
```
lsb_release -c
```

| Codename |   version   |
|----------|-------------|
|  bionic  | 18.04 (LTS) |
|  xenial  | 16.04 (LTS) |
|  trusty  | 14.04 (LTS) |
|  precise | 12.04 (LTS) |

Take Ubuntu 16.04 (LTS) for example, replace `etc/apt/sources.list` with following content:

```
deb http://mirrors.aliyun.com/ubuntu/ xenial main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ xenial main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ xenial-proposed main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-proposed main restricted universe multiverse
```

------

## Add new SSH key to github

```
ls -al ~/.ssh  # Lists the files in your .ssh directory, if they exist
ssh-keygen -t rsa -b 4096 -C "guohongyi@sjtu.edu.cn"
eval "$(ssh-agent -s)"
ssh-add -k ~/.ssh/id_rsa
```

Copy SSH key stored in `~/.ssh/id_rsa.pub` to github account

------

## E: Could not get lock /var/cache/apt/archives/lock - open (11: Resource temporarily unavailable)

## E: Unable to lock directory /var/cache/apt/archives/

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
