# <a name="linux-introduction"></a>Linux Introduction

**Table of Contents**

* [What is Linux?](#what-is-linux)
* [Why use Linux?](#why-use-linux)
* [Where is Linux deployed?](#where-is-linux-deployed)
* [Linux Distros](#linux-distros)
* [Virtual Box](#virtual-box)
---

## What is Linux?

Quoting from [Wikipedia](https://en.wikipedia.org/wiki/Linux)

>Linux is a family of free and open-source software operating systems built around the Linux kernel. Typically, Linux is packaged in a form known as a Linux distribution (or distro for short) for both desktop and server use. 
The defining component of a Linux distribution is the Linux kernel, an operating system kernel first released on September 17, 1991, by Linus Torvalds. Many Linux distributions use the word "Linux" in their name. The Free Software Foundation uses the name GNU/Linux to refer to the operating system family, as well as specific distributions, to emphasize that most Linux distributions are not just the Linux kernel, and that they have in common not only the kernel, but also numerous utilities and libraries, a large proportion of which are from the GNU project

<br>

## Why use Linux?

* Faster, Secure, Stable
    * it helps that developers from all over the world contribute, instead of just a single company
* Highly configurable
* Suitable for both single/multiuser environment
* Well defined hierarchy and permissions to allow networking across different groups and sites
* Strong set of commands to automate repetitive manual tasks

## Where is Linux deployed?

* Servers
* Supercomputers
    * To quote [TOP500 article on wikipedia](https://en.wikipedia.org/wiki/TOP500), "Since November 2017, all the listed supercomputers (100% of the performance share) use an operating system based on the Linux kernel"
* Embedded/IoT devices like POS, Raspberry Pi
* Smart phones
	* Android - built on top of Linux kernel
	* iOS - Unix based
* Personal and Enterprise Computers
* And many more uses, thanks to being open source
* [Usage Share of Operating Systems](https://en.wikipedia.org/wiki/Usage_share_of_operating_systems)

## Linux Distros
There are various Linux flavors called 'distribution' (distro for short), to cater the needs of beginners to advanced users as well as highly customized as per end use case

* There are [hundreds of known distributions](https://en.wikipedia.org/wiki/List_of_Linux_distributions)
* One can keep track of them at [distrowatch](https://distrowatch.com/)
    * [Statistics of various Linux Distros](https://distrowatch.com/dwres.php?resource=popularity)


# Virtual Box
### Virtualbox network Connection Settings
#### NAT (network address translation)
The vm and the host system share a single network identity that is not visible outside the network. 
Select NAT if you do not have a separate IP address for the vm, but you want to be able to connect to the internet. 
#### Bridged networking
The vm has direct access to an external Ethernet network. The vm must have its own IP address on the external network. Other computers in the network can then communicate directly with the vm. 