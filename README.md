## Scripts for testing FIO

```shell
# Single thread
fio -filename=/tmp/fio/FIO_FILE -ioengine=libaio -bs=16k -size=10G -numjobs=1 -runtime=10 -group_reporting -name=test -debug=ruiming -iodepth=4 -direct

# 4-thread (near-saturated)
fio -filename=/tmp/fio/FIO_FILE -ioengine=libaio -bs=16k -size=10G -numjobs=4 -runtime=10 -group_reporting -name=test -debug=ruiming -iodepth=32 -direct
```