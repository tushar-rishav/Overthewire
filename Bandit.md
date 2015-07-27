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

### Level 7
```sh
  ls -al
  cat data.txt|grep millionth
```
Level 8 password is ```cvX2JJa4CFALtqS87jk27qwqGhBM9plV```

### Level 8
```sh
  ls -al
  sort data.txt|uniq -cu
```
Level 9 password is ```UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR```

### Level 9
  ```sh
    ls -al
    strings data.txt|grep =
  ```
Level 10 password is ```truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk```

### Level 10
```sh
    ls -al
    base64 -d data.txt
```
Level 11 password is ```IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR```

### Level 11
```sh
  ls -al
  cat data.txt|tr [a-mn-zA-MN-Z] [n-za-mN-ZA-M]
```
Level 12 password is ```5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu```

### Level 12
```sh
  mkdir /tmp/tushar/
  cp data.txt /tmp/tushar/
  cd /tmp/tushar/
  xxd -r data.txt>data
  file data
  mv data data.gz
  gunzip data.gz
  file data
  mv data data.bz2
  bzip2 -d data.bz2
  file data
  mv data data.gz
  gunzip data.gz
  file data
  tar -xvf data
  file data5.bin
  tar -xvf data5.bin
  file data6.bin
  mv data6.bin data6.bz
  bzip2 -d data6.bz
  file data6
  tar -xvf data6
  file data8.bin
  mv data8.bin data8.gz
  file data8      ### ASCII TEXT
  cat data8  
```
Level 13 password is ```8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL```

### Level 13
```sh
  ls -al
  file sshkey.private
  ssh bandit14@localhost -i sshkey.private
  cd /etc/bandit_pass/
  file bandit14
  cat bandit14
```
Level 14 password is ```4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e```

### Level 14
```sh
  telnet localhost 30000
  4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
```
Level 15 password is ```BfMYroe26WYalil77FoDi9qh59eK5xNr```

### Level 15
```sh
  openssl
  s_client -connect localhost:30001 -quiet
  BfMYroe26WYalil77FoDi9qh59eK5xNr
```
Level 16 password is ```cluFn7wTiGryunymYOu4RcffSxQluehd```


