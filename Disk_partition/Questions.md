# Disk and partitioning questions
- Creating partitions is a key part to system management. You need to understand how to plan ahead and create custom partition layouts on systems as well as how to create the partition scheme you have designed. It is also important to understand the usefulness of RAID and LVM, along with how to implement them properly. These can both be very powerful tools when used correctly. 
<details>
<summary>1. What option is used with both the fdisk and parted commands to display the current partition tables?</summary>

```
The print option is used with both the fdisk and parted commands to display the current partition tables.
```
</details>
<details>
<summary>2. What does the partprobe command do?</summary>

```
The partprobe command forces the kernel to reread the partition table. You should always call it after making any changes to your system partitions.
```
</details>
<details>
<summary>3.  Do you need to write changes to the disk when using the parted command? What about fdisk?</summary>

```
When you exit the parted utility, all your changes are automatically written to disk. With the fdisk command, you need to manually write your changes to disk for them to take effect.
```
</details>
<details>
<summary>4. What are the three different types of RAID described in this chapter?</summary>

```
RAID 0 (Striping), RAID 1 (Mirror), and RAID 5 (Striping with parity).
```
</details>
<details>
<summary>5.  What command can you use to query information from the kernel about RAID arrays?</summary>

```
cat /proc/mdstat
```
</details>

<details>
<summary>6. What are the three items that make up LVM?</summary>

```
Physical volumes, volume groups, and logical volumes.
```
</details>
<details>
<summary>7. What are the side effects of shrinking a volume group or logical volume?</summary>

```
If you shrink a volume group or logical volume, there is a chance you could lose data depending on how much you shrink the volume.
```
</details>
<details>
<summary>8. What is the biggest benefit to using LVM over basic partitions?</summary>

```
If you shrink a volume group or logical volume, there is a chance you could lose data depending on how much you shrink the volume.
```
</details>
<details>
<summary>9. What command can you use to get information about logical volumes?</summary>

```
You have the flexibility to resize and add new volumes on the fly. With basic partitions, any time that you want to make a change, you need to destroy the partition and create it again.
```
</details>