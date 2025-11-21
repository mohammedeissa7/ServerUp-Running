# system Logging and monitor

<details>
<summary>1. What option can you change in the rsyslog config file to accept remote logs (acting as a centralized logging server)?</summary>

```
Uncomment the following line in the /etc/rsyslog.conf file:
#$ModLoad imudp.so
#$UDPServerRun 514
```
</details>
<details>
<summary>2. What two commands are special for dealing with user login events?</summary>

```
The lastlog and faillog commands are used to view user login–related events
```
</details>
<details>
<summary>3. Can you name the two commands that can be used to view the free space on the system?</summary>

```
The du and df commands are used to view available space on the system.
```
</details>
<details>
<summary>4. What command can you use to view system processes and their CPU usage?</summary>

```
Use the ps command to view processes and their CPU usage.
```
</details>
<details>
<summary>5. The at command is used to schedule reoccurring system jobs. True or False?</summary>

```
False. The at command is used to schedule one-time-only jobs. The cron service handles reoccurring system jobs.
```
</details>
<details>
<summary>6. What happens to jobs that are scheduled to run while the system is off?</summary>

```
When the system starts up again, the cron service will run any jobs that were missed while the system was off. On Red Hat Enterprise Linux5, the anacron service handles this functionality.
```
</details>
<details>
<summary>7. What command can be used to view the queue for at service jobs?</summary>

```
atq
```
</details>
<details>
<summary>8. What is the top command used for?</summary>

```
Use the top command to view CPU and memory usage.
```
</details>
