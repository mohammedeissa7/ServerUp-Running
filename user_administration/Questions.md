# User Administration


<details>
<summary>1. What command (and options) can be used to create a user named JSmith with the description “Jr Admin”?</summary>

```
useradd –c “Jr Admin” JSmith
```
</details>
<details>
<summary>2. What is the format of the /etc/shadow file?</summary>

```
The format of the /etc/shadow file is <username>:<encrypted password>:<lastpasswdchange>:<min>:<max>:<warn>:<inactive>:<expires>:<not used>.
```
</details>
<details>
<summary>3. What command would you use to create a group? How about to add the user JSmith to the group?</summary>

```
Use the groupadd command to create a group. You can then add user JSmith with the following: usermod –G <group name> JSmith
```
</details>
<details>
<summary>4. Is it possible to share files among groups? What permissions would you set on the directory to accomplish file sharing if possible?</summary>

```
You can use the sudo command to run a command with elevated privileges provided you have the rights in the /etc/sudoers file.
```
</details>
<details>
<summary>5. Is it possible to share files among groups? What permissions would you set on the directory to accomplish file sharing if possible?</summary>

```
Yes. You can use the setgid flag to create the appropriate permissions (chmod 2770).
```
</details>
<details>
<summary>6. If you want a specific action to take place when user01 logs in to the system, which file would you edit?</summary>

```
You add your action to the end of the /home/user01/.bashrc file.
```
</details>
<details>
<summary>7. You can add files to a user’s home directory during creation. True or False?</summary>

```
True. Place all files you want added to a user’s home directory in the /etc/skel directory.
```
</details>

<details>
<summary>8. By default, what is the path to a user’s home directory?</summary>

```
A user’s home directory is created under the /home directory.
```
</details>
<details>
<summary>9. What is the benefit to using centralized authentication?</summary>

```
By using centralized authentication, you don’t need to re-create or maintain multiple accounts across every system in your organization.
```
</details>
<details>
<summary>10. What commands can you use to add a client machine to an LDAP server?</summary>

```
You can use the authconfig-tui command or the authconfig command.
```
</details>