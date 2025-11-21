# Kernel
<details>
<summary>1. What is the difference between the update (-U) and install (-i) options when using rpm to update the kernel?</summary>

```
You should never use the –U option because it erases the prior kernel when updating. This leaves you with no fallback kernel should your system not boot properly.
```
</details>
<details>
<summary>2. What directory is used to represent the virtual file system created by the kernel?</summary>

```
The /proc directory. The /proc/sys directory is the place where you actually tune kernel parameters.
```
</details>
<details>
<summary>3. What file is used to maintain custom parameters for the kernel during system boot?</summary>

```
The /etc/sysctl.conf file maintains a list of custom kernel parameters that should be applied during system boot.
```
</details>
<details>
<summary>4. What critical step must you take after updating the kernel to a newer version?</summary>

```
You must ensure that the /boot/grub/grub.conf file has the new entry for your newly updated kernel to be able to boot into it.
```
</details>