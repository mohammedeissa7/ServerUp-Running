# Questions about boot process 
- These Questions will help you to described the boot process, the GRUB, and service management during and after the boot process. Knowing how to troubleshoot boot issues through.

<details>
<summary>1. GRUB has three stages. Can you name them?</summary>

```
1. Stage 1: During this stage, the primary bootloader is read into memory by the BIOS from the MBR. Stage 1.5: During this stage, the bootloader is read into memory by the stage 1 bootloader (only if necessary). Stage 2: During this stage, the bootloader reads the operating system or kernel.
```
</details>

<details>
<summary>2. What option at the GRUB boot menu can you use to append something to
 a kernel?</summary>

```
2. By entering the GRUB boot menu, you can choose the a option to append something to the kernel command-line options.
```
</details>

<details>
<summary>3. The old SysInit scripts have been replaced in Red Hat Enterprise Linux 6 for
 what new boot utility?</summary>

```
3. Upstart. The Upstart utility is now used in the boot process for Red Hat 
Enterprise Linux 6.
```
</details>

<details>
<summary>4. Runlevel 0 reboots the system. True or False?</summary>

```
4. False. Runlevel 0 halts the system. Runlevel 6 reboots the system.
```
</details>

<details>
<summary>5. If your system crashes and becomes unbootable, you have to reinstall the
 whole operating system. True or False?</summary>

```
5. False. Most boot issues can be resolved by entering rescue mode and repairing the problem.
```
</details>

<details>
<summary>6. What command can you use to manage system services?
</summary>

```
6. The service command is used to start, stop, and manage system services.
```
</details>

<details>
<summary>7. What command disables the SSH service from running when the system boots?</summary>

```
7. chkconfig sshd off
```
</details>
<details>
<summary>8. How can you list all services on the system to tell whether they will boot dur
ing startup?</summary>

```
8. chkconfig —list
```
</details>
<details>
<summary>9. What does S12rsyslog in the /etc/rc.d/rc2.d directory mean?</summary>

```
9. When the system enters into runlevel 2, the rsyslog service has a priority of 12
when starting. Anything with a lower number (or the same number and lower
first letter) starts before the rsyslog service.
```
</details>

<details>
<summary>10. How can you verify the status of the SSH service after the system has booted?</summary>

```
10. service sshd statuts
```
</details>


<details>
<summary>11. What command and option can you use to enable a service to start on boot?</summary>

```
11. Use the chkconfig command to enable or disable services during the boot process. The on option enables the service and off disables it.
```
</details>
