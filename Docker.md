IIEC RISE ID: RISE2020_71_6_1

## Docker Summary for 04-Apr-2020:
- Base Operating System
- Cleaning environment
- Launching images
- Checking ip of particular OS
- Connecting webpage from another laptop
- Connecting to the different network
- Is IP forwarding? Is our system forwarding ip? So that we can ping to google.
- Checking the port number is NAT (Natting) opposite (PAT)
- Exposing our ip address to the ousider world.
Launching a container
- iptables (firewall / does natting)
- change iptables chain setting to accept packets (default to drop)
- docker proxy - manage router
- never clean environment in production
- Empheral vs Persistent storage
- creating alias
- Volume = storage
- attaching volume/storage
- mount storage in the respective folder only.
- Launching a new web browser
- Accessing same volume by different OS
- This helps a lot in Load Balancing
- If persistent storage created, "mounts" will have data else blank
- we can give multiple drivers as well
- in centos, yum is already configured
- remove all repos forcefully
- creating local yum
- on ubuntu yum doesn't work. There is apt-get command.
- Why Docker is fast?
- About next technology, ML on DevOps
