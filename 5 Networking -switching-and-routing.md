# Host system must have a physical or virtual network interface, by running `ip link` command we can see that interface.

There are multiple interfaces such as eth, veth, and lo.

### System must have a physical or virtual network interface attached to it


1. **Host System and Network Interfaces**: Your computer, or the "host system," needs to have a way to connect to the internet or other devices. It does this through something called a "network interface," which is like a doorway to the internet world. This interface can be either a physical part of your computer (like a network card or Wi-Fi adapter) or a virtual one (created by software).

2. **Using the "ip link" Command**: To understand what network interfaces your computer has, you can use a special command called "ip link." When you run this command, your computer tells you about all the different network interfaces it knows about. It's a bit like asking your computer to introduce you to all its friends.

3. **Types of Interfaces**: There are different types of these network interfaces, and some of them have names like "eth," "veth," and "lo." These names help your computer recognize and manage each of them.

   - "eth" might stand for Ethernet, which is a common way to connect to the internet using a cable.
   - "veth" could be a virtual interface, meaning it's not a physical part of your computer but created by software, often used for special purposes.
   - "lo" stands for "loopback." It's a special interface that allows your computer to talk to itself, like a phone call from you to you. It's used for various technical tasks on your computer.

So, when you run "ip link" and see these different interfaces, it's your computer showing you all its friends that help it connect to the internet and do different tasks. Understanding them can be important for managing your computer's connections and making sure everything works smoothly.

# command can be used to display the kernel ip routing table.
From the route command, we can see the route table of the host system.
![image](https://github.com/Althaf-official/DevOps/assets/105126131/1106c149-252b-4279-b381-7f82dd26cd7f)

# Which of the following is preferred device to connect two system which are on different networks?

For example, if System A is on 192.168.1.0/24 network and System B is on 192.168.2.0/24 network. 


bridge


switch


router


gateway
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

It is router, which helps us to connect two networks together like network A can be reached to the different network B with the help of a router.

Sure, let's explain it in a simple way:

Think of a router like a traffic cop for the internet. It helps connect two different neighborhoods (or networks) so that they can talk to each other.

Imagine Network A as one neighborhood and Network B as another. These neighborhoods are like separate towns, and they have their own rules.

Now, the router is like a bridge between these two towns. It knows how to get from one neighborhood to the other. So, if you want to send a message or visit someone from Network A to Network B, the router helps you do that. It makes sure your message or visit gets to the right place in the other town.

In a nutshell, a router is like the friendly guide that helps people and data travel between different neighborhoods (or networks) on the internet. It's what makes the internet work by connecting all these different places together.



# We have four app server from app01 to app04. You can access each app from jump host using command ssh app01 and similarly for other apps. Assign new IPs to each host as per details given below:


a. Assign 172.16.238.15/24 ip address to app01

b. Assign 172.16.238.16/24 ip address to app02

c. Assign 172.16.239.15/24 ip address to app03

d. Assign 172.16.239.16/24 ip address to app04

e. We also need to remove existing IPs from these apps after assigning them new IPs but do not remove them right now as it can break your connection, if you are sure you are done with required changes just click on Check button below, it will do the rest.

Warning: If changes aren't made correctly it can break your connection to the environment and you may need to reload the lab.


----------------------------------------------------------------------------------------------------------------------

Note: Please ensure to execute the commands on their respective app nodes.


For example:-

To assign new IPs for app01 , the below command need to be executed on app01.

For app01: sudo ip addr add 172.16.238.15/24 dev eth0

Please follow the same procedure for other app nodes as well:

For app02: sudo ip addr add 172.16.238.16/24 dev eth0

For app03: sudo ip addr add 172.16.239.15/24 dev eth0

For app04: sudo ip addr add 172.16.239.16/24 dev eth0
![image](https://github.com/Althaf-official/DevOps/assets/105126131/f185f5fa-b26d-4667-bee9-4d4e02dce006)


# Now if you try to SSH into each app one by one from jump host you will find that you are able to SSH into app01 and app02 but not into app03 and app04. Why so ?

In the previous question, we assigned the new IPs to app servers.

We assigned app01 & app02 to 172.16.238.x and app03 & app04 to 172.16.239.x which is in different network range.

So you can check the same for jump host by running ip a command, you will see that it's in the same network range of app01 and app02 that's why we are able to SSH.

![image](https://github.com/Althaf-official/DevOps/assets/105126131/9847e132-f57c-4a4b-945e-e77acdfdd438)

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# FIX ME
# Since now app03 and app04 are on different network range than jump host so you are not able to SSH into those hosts from jump host. To make SSH work make required changes on jump host.


a. Assign a new IP address 172.16.239.10/24 to jump host with same network range which app03 and app04 are using.

b. Now you will be able to SSH into all apps from jump host.

NOTE: - After the change, you may experience a delay when trying to SSH from the jump server to the app servers.

Use command: sudo ip addr add 172.16.239.10/24 dev eth0


# FIXME
# Now jump host is able to access all four apps. But if you try to ping app03 or app04 from app01 or app02 or vice versa you will see ping is not working. So now we want to use jump host as a router so that app01 and app02 can access app03 and app04 and vice versa, lets add some routing table entries on these hosts to make it work.


a. Add a routing table entry in app01 and app02 hosts so that these hosts can reach app03 and app04 hosts via jump host.

b. Add a routing table entry in app03 and app04 hosts so that these hosts can reach app01 and app02 hosts via jump host.

c. Now try to ping app03 and app04 from app01 and app02 and vice versa, every app should be able to ping each other.



Use below mentioned command:

On app01 and app02: sudo ip route add 172.16.239.0/24 via 172.16.238.10

On app03 and app04: sudo ip route add 172.16.238.0/24 via 172.16.239.10
