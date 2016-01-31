+++
date = "2015-12-15T20:59:34+01:00"
draft = false
title = "Configuring i2 amazon instances for SSDs"
categories=["tech"]
+++

If you are configuring Amazon instances for storage optimized workloads, You might want to use amazon i2 instances. They are backed by super fast SSDs than
conventional hard drives therefore it is suitable for disk intensive workloads.

if you issue the command
```
df -h
```

you may inspect current available disk storage and mounted paths.

In that case, have you ever wondered that your newly spawn amazon I2 instance(if i2.xlarge ==> 1 800GB SSD and if it i2.2xlarge 2x 800GB so on.) does not have 800GB hard disks it claimed to have. If so it is because both I2 and R3 instances support TRIM. 

So here is what you need to do to make that storage available.


To format and mount the disk you can follow the below steps.

1) Examine available drives

```
sudo fdisk -l
```

2) choose the drive you need to create a file system. (eg: if you choose xvdb and want to create ext3 file system for linux)

```
sudo mkfs.ext4 -E nodiscard /dev/xvdb
```

3) You can now mount the disk to any folder path you need. In this you mount the formatted disk to /mnt/my-data

```
sudo mount -o discard /dev/xvdb /mnt/my-data
```

Now you may

If you need further details please refer following link.

http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ssd-instance-store.html#InstanceStoreTrimSupport