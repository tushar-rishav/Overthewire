##[Bandit](http://www.overthewire.org/wargames/bandit/)

### Level 0
```sh
  ls -al
  cat readme
```
Level 1 password is ```boJ9jbbUNNfktd78OOpsqOltutMc3MY1```

### Level 1
```sh
ls -al
cat ./-
```
Level 2 password is ```CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9```

### Level 2
```sh
ls -al
cat 'spaces in this filename'
```
Level 3 passowrd is ```UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK```

### Level 3
```sh
ls -al
cd inhere
ls -al
cat ./.hidden
```
Level 4 password is ```pIwrPrtPN36QITSp3EQaw936yaFoFgAB```

### Level 4
```sh
ls -al
cd inhere
file ./-file07    ### ASCII text-> Human readable
cat ./-file07
```
Level 5 password is ```koReBOKuIDDepwhWk7jZC0RTdopnAYKh```

### Level 5
```sh
  ls -al
  cd inhere
  find -readable -size 1033c    ### ./maybehere07/.file2
  cat maybehere07/.file2
```
Level 6 password is ```DXjZPULLxYr17uwoI01bNLQbtFemEgo7```

### Level 6
```sh
  cd /
  find -group bandit6 -user bandit7 -size 33c
  cd /var/lib/dpkg/info/
  ls -al
  file bandit7.password   ### ASCII text
  cat bandit7.password
  ```
  Level 7 password is ```HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs```


