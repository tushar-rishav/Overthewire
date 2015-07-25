## [Leviathan](http://www.overthewire.org/wargames/leviathan/)

## Level 0
```sh
ls -al
cd .backup
ls -al
cat bookmarks.html|grep password
```

Leviathan1 password is ```rioGegei8m```

## Level 1
```
ls -al
file check
strings check ### to read the non text files
./check
### enter sex as password, because sex = secret love
cd /
ls -al
cat README.txt  ### Says PASSWORDS for each level are stored in /etc/somegame_pass/
ls -al|grep leviathan
cd leviathan_pass
ls -al
file leviathan2     ### ASCII text
cat leviathan2
```
Leviathan2 password is ```ougahZi8Ta``` 

