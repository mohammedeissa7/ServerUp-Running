# Package Managemnt
-  Learning to work with software is important because the rest of this book and the Red Hat exams require you to install and configure different software packages. You also need to be able to verify that packages have been installed successfully and fix them when they are not. The package management process isn’t difficult and can be very useful for keeping your systems in order. As you become more skilled with package management, you will start to get a feel for what packages can also be safely removed from your system to prevent security attacks.

<details>
<summary>1. What two commands are used for package management?</summary>

```
The yum and rpm commands are used for package management.
```
</details>
<details>
<summary>2. What are the three modes in which the rpm command can operate?</summary>

```
The rpm command can operate in install, query, or verify modes.
```
</details>
<details>
<summary>3. What option would you use to query an installed package using the rpm command?</summary>

```
You can use the -q option to query an installed package. Combining grep and the -qa options, you can search among all installed packages on the system.
```
</details>
<details>
<summary>4. How would you install a group of packages all at a single time?</summary>

```
Use the yum groupinstall command to install multiple packages in a single group at once.
```
</details>
<details>
<summary>5. What options with the yum command would you use to remove a package?</summary>

```
You can use the remove or erase options with yum to remove a package.
```
</details>
<details>
<summary>6. Where are Yum repository config files located?</summary>

```
Yum repository config files (.repo files) are located in the /etc/yum.repos.d directory. You can also make direct entries into the main /etc/yum.conf file.
```
</details>
<details>
<summary>7. What command can you use to create your own repositories?</summary>

```
createrepo
```
</details>
<details>
<summary>8. What command is used to create an RPM package?</summary>

```
rpmbuild
```
</details>
<details>
<summary>9. What are the five required directories when building RPMS?</summary>

```
The five directories are BUILD, RPMS, SOURCES, SPECS, and SRPMS.
```
</details>
<details>
<summary>10. If a package is built on an RHEL6 system and deployed to a custom RHEL5 repository, are RHEL5 systems able to use it?</summary>

```
No. Red Hat Enterprise Linux 6 uses a different key to sign its packages.
```
</details>