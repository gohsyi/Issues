### "ipcluster nbextension enable" crashes on a permission error

PermissionError: [Errno 13] Permission denied: '/usr/local/share/jupyter'

Solve: 
```
jupyter serverextension enable --py ipyparallel --user
jupyter nbextension install --py ipyparallel --user 
jupyter nbextension enable --py ipyparallel --user
```

> https://github.com/ipython/ipyparallel/issues/170
