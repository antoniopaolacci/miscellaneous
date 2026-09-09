# miscellaneous
Miscellaneous (things, junk): refers to a varied collection of unrelated, often low-value items that don't fit into a specific category.

---

## Identify Which Process Is Blocking a File in Windows Using Process Explorer

Process Explorer is a _free_ tool from **Microsoft Sysinternals**:

You can acquire Process Explorer using the following WingGet command from command line prompt:

```
Winget install Microsoft.Sysinternals.ProcessExplorer
```

```
In Process Explorer, Go to **Find > Find Handle or DLL**.
```

```
Type part of the file or folder name and click Search.
```

The tool will list all processes currently using the file. Click an entry to highlight the process in the main window.
You can _right-click_ the handle and select **Close Handle** to release the file (use with caution).

---

## Syntax for while loop in Bash cli

```
root@ubuntu24:~# > while true
> do
> curl -k -X 'POST' 'https://localhost:8443/api/encrypt' -H 'accept: application/json' -H 'Content-Type: application/json' -d '{ "value": "ABCDEF" }'
> sleep 10
> done
```

## Trovare le CARTELLE più grandi _in un path_

```
du -h --max-depth=1 . 2>/dev/null | sort -hr | head -20

OUTPUT
20G     .
9.6G    ./var
4.4G    ./usr
3.1G    ./root
1.7G    ./snap
718M    ./opt
144M    ./boot
19M     ./run
6.7M    ./etc
176K    ./tmp
84K     ./dev
16K     ./lost+found
4.0K    ./srv
4.0K    ./sbin.usr-is-merged
4.0K    ./mnt
4.0K    ./media
4.0K    ./lib.usr-is-merged
4.0K    ./home
4.0K    ./bin.usr-is-merged
0       ./sys
```


## Trovare i FILE più grandi _in un path_
Puoi forzare il comando sort a usare esclusivamente la memoria RAM anziché il disco per gestire l'ordinamento. Essendo il disco pieno: _No space left on device_ 

```
du -sh * | sort -h -S 50% --temporary-directory=/dev/shm 

OUTPUT
724K    kern.log.3.gz
800K    ufw.log.2.gz
828K    kern.log.2.gz
864K    ufw.log.4.gz
872K    syslog.3.gz
908K    kern.log.4.gz
916K    cloud-init.log
1.1M    syslog.4.gz
1.2M    syslog.2.gz
1.3M    ufw.log
1.4M    kern.log
2.6M    auth.log.2.gz
3.2M    auth.log.4.gz
3.3M    auth.log.3.gz
3.8M    nginx
5.5M    ufw.log.1
5.7M    kern.log.1
11M     btmp
12M     auth.log
17M     letsencrypt
20M     auth.log.1
49M     journal
54M     mysql
102M    btmp.1
```
