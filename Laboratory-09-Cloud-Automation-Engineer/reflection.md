# Mission Reflection

**1. Why is automation critical when managing hundreds of cloud servers?**
Manual work across hundreds of servers is slow, inconsistent, and error-prone. A script like backup.sh behaves the same way every time, and cron removes the need for a human to remember. Automation lets one engineer manage a whole fleet and frees people for higher-value work.

**2. What are the potential dangers of automation?**
Automation multiplies mistakes as well as successes. A destructive typo, such as a wrong path in an rm command, would hit all 1,000 servers at once and could erase data within seconds. Testing on one server first, staged rollouts, backups, code review, and least-privilege permissions reduce the risk.

**3. How did writing a Bash script differ from creating a Docker Compose YAML file?**
A Bash script is imperative: I wrote each step in order, such as creating the folder, compressing the data, and printing a message. A Docker Compose file is declarative: I described the desired end state, including services, images, and ports, and Docker figured out how to reach it. Bash is more flexible, but Compose is easier to read and reproduce.

**4. How has your understanding of Cloud Computing transformed from Laboratory 1 to 9?**
At the start, I saw the cloud as "someone else's computer" and followed commands without fully understanding them. Over the semester I learned how the pieces fit together: the Linux terminal, permissions, containers, networking, and now automation. Reviewing my repository, each laboratory built on the one before it. I now see cloud work as designing reliable, repeatable systems, and I feel far more confident fixing problems myself.

**5. Which role did you enjoy the most and why?**
I enjoyed the Infrastructure Engineer role the most. Building the backup script, fixing the "Permission denied" error with chmod, and scheduling it with cron gave me a satisfying result: a system that protects data without anyone watching it. I like making things dependable.
