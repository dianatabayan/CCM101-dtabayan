# Mission Reflection

## Why monitor the host server's resources?
Monitoring the host server's resources is important even when my containers are running perfectly because every container shares the same underlying machine. If the host runs out of memory, disk space, or CPU capacity, all of the containers on it can slow down, crash, or fail to start, no matter how well each one is configured. A healthy container can hide a struggling server, so a Cloud Operations Engineer needs a baseline of the host's normal behavior. With that baseline, a problem such as a filling disk can be noticed and fixed before it turns into an outage for the client.

## How would docker logs help with a login complaint?
If a user complains that they cannot log into a web application, the docker logs command would help me find the cause quickly. The logs record every request the application receives, along with its status code and timestamp. I could look for the user's request and see whether it returned an error such as a 404, 401, or 500, and what time it happened. That evidence shows me whether the problem is a missing page, a failed authentication, or a server fault, so I can fix the right thing instead of guessing.

## Logs vs. metrics
The difference between monitoring logs and monitoring metrics is the kind of question each one answers. Logs, which I used in Checkpoint 4, are a detailed record of individual events, such as the single failed request to the hidden admin page. They tell me what happened and why. Metrics, which I used in Checkpoint 5 with docker stats, are numbers measured over time, such as CPU percentage and memory usage. They tell me how healthy the container is right now and whether it is consuming too many resources. Logs help me investigate a specific problem after it occurs, while metrics help me notice trouble early. A good engineer uses both together, because metrics show that something is wrong and logs help explain it.
