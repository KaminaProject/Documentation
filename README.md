# Kamina
<p align="center">
	<img src="logo/kamina_logo.svg" width="400" align="middle"/>
</p>  
<small>Nice logo amirite.</small>

## Overview
**Kamina** is a decentralized social network, pro free-speech. With IPFS in its core, **Kamina** is  divided into communities, each with a unique government system.

## Vision
We want to develop a decentralized social network, that gives control to its users over their own personal information. We decided to
start doing this project after all the stuff that has being going on with facebook, like the cambridge analytica issue, or the fact that
facebook sells your data to advertisers (remember, if some service is free, you probably are the product).

## Design
*Kamina* aims to be as much as decentralized as it can become without actually becoming a distributed system. After anaylizing the
possible technologies that could help us reach this objective, we found out that IPFS, while still being in its early stages, is a good option
for the storage information within *Kamina*.  
This being said, the **Kamina** project is divided into 3 projects, that will be able to communicate with each other. This 3 sub projects are
*Kamina Community*, *Kamina User* and *Kamina Search*.  

### Kamina Community
*Kamina Community* is where all the users interact. Each *Kamina Community* instance will have a single
topic of discussion, just how Reddit divides itself into sub-reddits or 4chan into boards.  Anyone can access and start using a 
*Kamina Community* instance, but the user will be limited on what it can do. In order to access all the funcionality the instance has, 
the user has to register into that community.  
The registration requires the user to download and start a *Kamina User* instance in its pc.
Have a sneak peek of what a *Kamina Community* instance would look like.
   
![community-preview](./img/preview.png)

This design could change in the future though, caveat emptor.

### Kamina User
Hey, we said the user would be in control of its information, that is why the user's information will  be stored in their computers!, they will have
to download some software for that though. After the user downloads and initializes the instance, it can register into any existing
*Kamina Community* instances. This software that the user will download will expose an API the the *Kamina Community*
instance can use in order to exchange information.  
Though, because the user has to instance running in a device, it will only be possible to login/register in that device because the
*Kamina Community* instance will only be able to communicate with *localhost*. One way to circunvent this problem is to give
the *Kamina Community* instance an IP or domain to connect.

### Kamina Search
*Kamina Search* will be in charge of combining both *Kamina Community* and *Kamina User* instances. In will work like this
Mastodon instances [search page](https://instances.social/list#lang=&allowed=&prohibited=&users=). But *Kamina Search* will also store backup information from *Kamina Community* instances, in case any of them dissapear.  
This way, any user can access the content of a *Kamina Community* up until the date of the creation of the backup.

## Technicalities
<small>Is that how it is supposed to be written? dunno</small>
  
We will be using python for all three projects, since it is cross platform and easy for anyone to learn. The APIs from each project will be
managed by flask and the frontend of each project will be handled by using VueJS.

## How to contribute
Third-party changes are essential in order for kamina to improve. We simply don't have access 
to every platform in existance, so we want to keep it simple for you to contribute patches that
get things working in your environment. There are a few guidelines before you can start making
pull requests.

### Getting Started
* Make sure you have a github account.
* Create an issue in the corresponding project (community, user, search, etc.) if one does not already exist.
	- Clearly describe the issue including steps to reproduce if it is a bug.
	- Make sure to add the earliest version that contains that issue.
* Fork the repository on github.

### Making Changes
* Create a new branch from where you will base your work.
* Make commits of logical and atomic units.
* Be sure you are following pep-8 when writing the codez.

### Submitting Changes
* Push your changes to a branch in your fork of the repository.
* Before submitting a pull request:
	- Run pylint in all the files you have modified
	- Describe the changes you've made as verbose as possible
* Submit a pull request to the project's repository.
* If after 2 weeks of giving feedback there is no activity, the pull request will be closed.

### Additional Resources
[pylint](https://www.pylint.org/)
[PEP 8](https://www.python.org/dev/peps/pep-0008/)
