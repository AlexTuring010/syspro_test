## run a nfs_client (source) in another console
## on linux10.di.uoa.gr
```bash
./nfs_client -p 6556 
```

## run another nfs_client (target) in another console
## on linux11.di.uoa.gr
```bash
./nfs_client -p 6557
```

## run nfs_manager in aterm connected at linux09.di.uoa.gr and 6555
```bash
./nfs_manager -l np_nfs_manager.log -c sysprotest/config_nfs.cfg -n 5 -p 6555 -b 7
```

## run nfs_console in another console
```bash
./nfs_console -l np_nfs_console.log -h linux09.di.uoa.gr -p 6555
```

##check initial sync in target client

## console //
```bash
cancel /sysprotest/config_source_dir1
```

## console
```bash
add /sysprotest/added_source_dir@linux10.di.uoa.gr:6556 /sysprotest/added_target_dir@linux11.di.uoa.gr:6557
```

```bash
ls sysprotest/added_target_dir
```

## console //
```bash
shutdown
```
## Anoixe kai deixe ta log arxeio toy manager kai toy console
