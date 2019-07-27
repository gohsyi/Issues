### error: command 'gcc' failed with exit status 1 when installing mujoco

```
sudo apt-get install python3-dev
```
> https://stackoverflow.com/questions/11094718/error-command-gcc-failed-with-exit-status-1-while-installing-eventlet


### "ipcluster nbextension enable" crashes on a permission error

PermissionError: [Errno 13] Permission denied: '/usr/local/share/jupyter'

Solve: 
```
jupyter serverextension enable --py ipyparallel --user
jupyter nbextension install --py ipyparallel --user 
jupyter nbextension enable --py ipyparallel --user
```

> https://github.com/ipython/ipyparallel/issues/170
