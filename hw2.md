## run a nfs_client (source) in another console
## on linux10.di.uoa.gr
./nfs_client -p 5556

## run another nfs_client (target) in another console
## on linux11.di.uoa.gr
./nfs_client -p 5557

## run nfs_manager in aterm connected at linux09.di.uoa.gr and 5555
./nfs_manager -l np_nfs_manager.log -c sysprotest/config_nfs.cfg -n 5 -p 5555 -b 7

## run nfs_console in another console
./nfs_console -l np_nfs_console.log -h linux09.di.uoa.gr -p 5555

##check initial sync in target client

## console //
cancel /sysprotest/config_source_dir1

## console
add /sysprotest/added_source_dir@linux10.di.uoa.gr:5556 /sysprotest/added_target_dir@linux11.di.uoa.gr:5557
ls sysprotest/added_target_dir


## console //
shutdown

## Anoixe kai deixe ta log arxeio toy manager kai toy console
