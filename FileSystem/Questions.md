# File System questions
- 
<details>
<summary>1. What is the difference between an ext2 and ext3 file system?</summary>

```
An ext3 file system has journaling built in to it, whereas the ext2 file system doesn’t
```
</details>
<details>
<summary>2. What command can you use to create a file system?</summary>

```
mkfs.ext4
```
</details>
<details>
<summary>3. Can you grow a file system?</summary>

```
Yes. Use the resize2fs command to grow a file system.
```
</details>
<details>
<summary>4. What is the superblock used for?</summary>

```
The superblock is a structure that contains metadata of the file system. If this becomes corrupt, you are in trouble
```
</details>
<details>
<summary>5. What is a swap? Is it created as a partition or device file?</summary>

```
A swap is scratch space on your file system used as virtual memory. A swap can be created as a partition or a device file.
```
</details>
<details>
<summary>6. How can you check the currently mounted file systems?</summary>

```
The mount command lists all currently mounted file systems.
```
</details>
<details>
<summary>7. What file needs to be edited so that the system will mount a file system at boot time?</summary>

```
The /etc/fstab file.
```
</details>
<details>
<summary>8. Before you work with quotas, what do you need to do to the file system?</summary>

```
The file system where quotas will be implemented must be mounted with the
usrquota and grpquota options before quotas will work properly.
```
</details>
<details>
<summary>9. What command do you use to change the permissions on a file or directory? To change ownership?</summary>

```
The chmod command is used to change the permissions of files and directories.
The chown command is used to change the ownership of files and directories.
```
</details>
<details>
<summary>10. Explain the difference between soft and hard limits in quotas.</summary>

```
A soft limit acts like an alarm, signaling you when you are reaching your limit.If you don’t specify a grace period, the soft limit is the max. A hard limit is required only when a grace period exists. It is the max limit you can hit before your grace period expires.
```
</details>
<details>
<summary>11. What command do you use to report information on quota usage?</summary>

```
repquota
```
</details>
<details>
<summary>12. Before you work with ACLs, what do you need to do to the file system?</summary>

```
The file system where ACLs will be implemented must be mounted with the acl option before ACLs will work properly.
```
</details>
<details>
<summary>13. What command can you use to view the current ACL on a file?</summary>

```
The file system where ACLs will be implemented must be mounted with the acl option before ACLs will work properly.
```
</details>