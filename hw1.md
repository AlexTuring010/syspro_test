## 🟢 Run `fss_manager` in a terminal
```bash
./fss_manager -l np_fss_manager.log -c config_fss.cfg -n 5
```

## 🟢 Run `fss_console` in another terminal
```bash
./fss_console -l np_fss_console.log
```

## 🔍 Check config file syncs
```bash
diff -r /home/users/sdi2200284/Desktop/syspro/sysprotest/config_source_dir1 /home/users/sdi2200284/Desktop/syspro/sysprotest/config_target_dir1

diff -r /home/users/sdi2200284/Desktop/syspro/sysprotest/config_source_dir2 /home/users/sdi2200284/Desktop/syspro/sysprotest/config_target_dir2
```

## 🗂️ Console command: status (should show it's monitored)
```bash
status /home/users/sdi2200284/Desktop/syspro/sysprotest/config_source_dir1
```

## ❌ Console: cancel monitoring
```bash
cancel /home/users/sdi2200284/Desktop/syspro/sysprotest/config_source_dir1
```

## 🟡 Console: add new directory pair
```bash
add /home/users/sdi2200284/Desktop/syspro/sysprotest/added_source_dir /home/users/sdi2200284/Desktop/syspro/sysprotest/added_target_dir
```

## 📁 Add and remove test files
```bash
cp /home/users/sdi2200284/Desktop/syspro/sysprotest/test_files/f4_1000.txt /home/users/sdi2200284/Desktop/syspro/sysprotest/config_source_dir2
cp /home/users/sdi2200284/Desktop/syspro/sysprotest/test_files/f4_2000.txt /home/users/sdi2200284/Desktop/syspro/sysprotest/config_source_dir2
rm -rf /home/users/sdi2200284/Desktop/syspro/sysprotest/config_source_dir2/f4_2000.txt
```

## ✅ Console: shut down
```bash
shutdown
```

## 🧠 fss_script commands
```bash
./fss_script.sh -p np_fss_manager.log -c listAll
./fss_script.sh -p np_fss_manager.log -c listMonitored
./fss_script.sh -p np_fss_manager.log -c listStopped
./fss_script.sh -p np_fss_manager.log -c purge
```

## 📜 Show log files
```bash
cat np_fss_manager.log
cat np_fss_console.log
```
