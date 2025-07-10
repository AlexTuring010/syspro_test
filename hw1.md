## run fss_manager in a term
```bash
./fss_manager -l np_fss_manager.log -c config_fss.cfg -n 5
```

## runn fss_console in another console
```bash
./fss_console -l np_fss_console.log
```

## check config file syncs
```bash
diff -r /home/users/sdi2200284/t/sysprotest/config_source_dir1 /home/users/sdi2200284/t/sysprotest/config_target_dir1
```

```bash
diff -r /home/users/sdi2200284/t/sysprotest/config_source_dir2 /home/users/sdi2200284/t/sysprotest/config_target_dir2
```

## console //prepei na epistrepsei oti parakoloutheite
```bash
status /home/users/sdi2200284/t/sysprotest/config_source_dir1
```

## console //
```bash
cancel /home/users/sdi2200284/t/sysprotest/config_source_dir1
```

## console //prepei na epistrepsei oti DEN parakoloutheite
```bash
status /home/users/sdi2200284/t/sysprotest/config_source_dir1
```
## console
```bash
add /home/users/sdi2200284/t/sysprotest/added_source_dir /home/users/sdi2200284/t/sysprotest/added_target_dir
```

##check add file syncs
```bash
diff -r /home/users/sdi2200284/t/sysprotest/added_source_dir /home/users/sdi2200284/t/sysprotest/added_target_dir
```
## console //status of added dir. prepei na epistrepsei oti  parakoloutheite
```bash
status /home/users/sdi2200284/t/sysprotest/added_source_dir
```

## console //prepei na epistrepsei oti  parakoloutheite
```bash
sync /home/users/sdi2200284/t/sysprotest/config_source_dir2
```

#check updates replace sdi

#add a file
```bash
cp /home/users/sdi2200284/t/sysprotest/test_files/f4_1000.txt /home/users/sdi2200284/t/sysprotest/config_source_dir2
```

```bash
ls -las /home/users/sdi2200284/t/sysprotest/config_target_dir2
```

#add a file
```bash
cp /home/users/sdi2200284/t/sysprotest/test_files/f4_2000.txt /home/users/sdi2200284/t/sysprotest/config_source_dir2
```

```bash
ls -las /home/users/sdi2200284/t/sysprotest/config_target_dir2
```

#remove a file
```bash
rm -rf /home/users/sdi2200284/t/sysprotest/config_source_dir2/f4_2000.txt
```

```bash
ls -las /home/users/sdi2200284/t/sysprotest/config_target_dir2
```

#update a file
```bash
ls -las /home/users/sdi2200284/t/sysprotest/config_source_dir2
```

```bash
cat /home/users/sdi2200284/t/sysprotest/test_files/f4_1000.txt >> /home/users/sdi2200284/t/sysprotest/config_source_dir2/f4_1000_copy.txt
```

```bash
ls -las /home/users/sdi2200284/t/sysprotest/config_target_dir2
```

## console //
```bash
shutdown
```

### fss script
##εμφανίζει όλους τους καταλόγους, την ημερομηνία και ώρα τελευταίου συγχρονισμού, μαζί με status
```bash
./fss_script.sh -p np_fss_manager.log -c listAll
```

##τους καταλόγους που παρακολουθούνται ενεργά.
```bash
./fss_script.sh -p np_fss_manager.log -c listMonitored
```

##τους καταλόγους που δεν παρακολουθούνται πλέον
```bash
./fss_script.sh -p np_fss_manager.log -c listStopped
```

##διαγράφει μόνο τον target κατάλογο ή το logfile
```bash
./fss_script.sh -p np_fss_manager.log -c purge
```

## Anoixe kai deixe ta log arxeio toy manager kai toy console
