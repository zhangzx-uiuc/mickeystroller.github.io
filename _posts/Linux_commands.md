### Decompress

```
tar -zxvf backup.tar.gz 
```

### Compress
```
tar -cxvf file.txt
```

### Alias
```
$ vim ~/.bash_profile
add one line: alias l='ls -lah'
$ source ~/.bash_profile
```

### PDFcrop
```
pdfcrop --margins '5 10 20 30' input.pdf output.pdf
```
* the left, top, right, bottom order.


### Tmux
```
tmux new -s myname # create new session
tmux ls # list all existing seesion
tmux a -t myname # attach to existing session
```
[tmux cheatsheet](https://gist.github.com/MohamedAlaa/2961058)

### Swith modules on Server
```
module avail # see all available modules
module load # load module
```

### Download git repo with username
```
git clone https://username@github.com/username/repository.git
```




