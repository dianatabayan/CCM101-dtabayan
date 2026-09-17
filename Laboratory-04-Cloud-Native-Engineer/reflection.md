# Mission Reflection

Working through this lab made the difference between virtual machines and
containers feel real instead of theoretical. Spinning up an Nginx container
took only seconds, whereas setting up an operating system on a traditional VM
can take fifteen minutes or more just to reach a usable state. That gap comes
down to what's actually being started: a VM boots an entire guest OS, with
its own kernel, drivers, and services, while a container is just a process
launched on a kernel that's already running. There's no OS to initialize and
no login services to wait on — the image is unpacked and the app starts
almost immediately.

Port mapping (`-p 8080:80`) was necessary because a container's network is
isolated from the host by default. Nginx listens on port 80 inside the
container, but nothing on the host can reach that port directly unless it's
explicitly forwarded. The mapping tells Docker to take any traffic arriving
at port 8080 on the host machine and route it into port 80 inside the
container, which is exactly what made the `curl http://localhost:8080`
request succeed.

Running `docker rm` also clarified something about how containers handle
data: because containers are meant to be disposable, any data written inside
the container's writable layer disappears the moment the container is
removed, unless that data was explicitly stored in a mounted volume outside
the container. That's a very different model from a VM, where the disk
persists by default.

More broadly, this shifts how developers and operations teams work together.
Because a container packages the application with its exact dependencies,
"it works on my machine" stops being a valid excuse — the same image runs
identically in development, testing, and production. That consistency is a
big part of why DevOps practices lean so heavily on containers: it collapses
the traditional handoff between writing code and deploying it into something
far more continuous.

My GitHub portfolio is evolving from a place to store finished code into a
running record of infrastructure and deployment work — not just what I built,
but how I built and shipped it.
