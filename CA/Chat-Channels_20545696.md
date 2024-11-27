1. [Community Architects](index.html)
2. [Community Architects Team](Community-Architects-Team_20545564.html)
3. [Best Practices](Best-Practices_20545700.html)

# Community Architects : Chat Channels

Created by Tracy Kuhrt, last modified by David Boswell on Dec 02, 2019

This document covers best practices surround the naming, information fields, and roles for the chat channels. Today, we have the following type of chat channels (see [chat channel mapping](Chat-Channel-Mapping_20548329.html)):

- Project channels (e.g., fabric-\*, sawtooth-\*)
- Working Group channels (e.g., architecture-wg, identity-wg)
- Special Interest Group channels (e.g., social-impact-sig, healthcare-sig)
- Community channels (e.g., community-\*)
- Language-specific channels (e.g., russia, portuguese)
- Lab channels (e.g., labs, private-data-objects)
- Program channels (e.g., meetup, ambassador)
- Event channels (e.g., blockchain4good, hackfests)
- Devops channels (e.g., ci-pipeline, jenkins-robot)
- Tools channels (e.g., github-taskforce, jira)
- Bot channels (e.g., hyperledger-bot, sorabot-test-channel)
- General channels (e.g., general, jobs)

# Channel Naming

This section covers the best practices for naming for each of the different channel types.

## Project Channels

- All project related channels must be named using the project name as the prefix.
- All projects should have a contributors channel (e.g., fabric-contributors, sawtooth-contributors). Naming must be consistent across all projects. Today, we have both `-contributor` and `-dev` channels.
- Project channels should be limited to ensure that people know where to look and eliminate fragmentation. The following channels should be created for all new projects:
  
  - *project*`-maintainers` - Used by the maintainers to the project to discuss topics related to the direction and vision of the project.
  - *project*`-contributors` - Used by the contributors to the project to discuss topics related to the development of the project.
  - *project*`-end-users` - Used by the end users of the projects to discuss topics and questions related to how to use the project.
- Project channels should not be created for every single component of the project.

## Working Group Channels

- All working group related channels must be named using `-wg` as a suffix.

## Special Interest Group Channels

- All special interest group related channels must be named using `-sig` as a suffix.

## Community Channels

- All community related channels must be named using `community-` as the prefix.

## Language-specific Channels

Today, language-specific channels are just the name of the language (e.g., russia, japanese, portuguese). Ideally, we should name these in some way that reflects that these were created for people who speak the same language to have a place to communicate. This best practice is not followed today. It may even make sense that the three language-specific channels that we have become community channels. Thus renaming them to community-russia, community-japanese, and community-portuguese.

## Lab Channels

Today, we have the general #labs channel for discussions by the lab stewards and people that are interested in creating a lab. We have also created upon request a channel for the individual labs within Hyperledger.

- Since we only have a single channel for each lab, all lab-specific channels must be named using the format `lab-`*lab-name*.

## Program Channels

Today, program channels are not easily discoverable (e.g., ambassadors, meetup). This best practice will ensure that programs can be more easily located.

- All program channels must be named using `-program` as a suffix.

## Event Channels

Today, we have two event channels – blockchain4good and hackfest. Many people have mistaken the blockchain4good channel to be used outside of the event.

- All event channels must be named using `event-` as a prefix.

## DevOps Channels

- All DevOps channels must be named using `devops-` as a prefix.

## Tools Channels

- All tools channels must be named using `tools-` as a prefix.

## Bot Channels

- All bot channels must be named using `bot-` as a prefix.

## General Channels

- No more general channels should be added.

# Channel Information

Chat allows the administrator to specify a "Topic", "Description", and "Announcement" via the room information. The following best practices will allow people to discover and properly use the channels.

- All channels must have a topic specified. This will be a short description of the channel.
- All channels must have a description specified. This will be a longer description that specifies information about how and for what this channel is used, as well as, when this channel should not be used.
- The "Announcement" field shall only be used when you want to call attention to something specific related to this channel. An example could be a new release of the project.

# Chat Channel Tips

If you go into a specific chat channel directly, without logging in, you will see a spinner that will not resolve. Please follow the steps below:

01. You need to have a Linux foundation ID
02. Go to [https://chat.hyperledger.org](https://chat.hyperledger.org/channel/capital-markets-sig)
03. It will show you the general channel, click on general
04. Go to the bottom of the general channel and it will show a link (sign in to start talking)
05. Click on that link you will be prompted for your LFID and password (you can also setup your LFID from here)
06. Then you click on the capital markets sig link and it will take you right there ([https://chat.hyperledger.org/channel/capital-markets-sig](https://chat.hyperledger.org/channel/capital-markets-sig))
07. If you are already logged into chat then you can directly click on the link above and it will take you there.
08. In both cases (6. and 7.) it will ask whether you want to join the capital-markets-sig and you choose to join the channel
09. If you are logged in to Rocketchat you can also search for capital-markets-sig and do the same thing as in point number 8.
10. You can also add it to your favorites if you have many channels open

# Roles

This section covers the best practices surrounding roles for the chat channels. Today, our chat program supports the following roles:

- Admin
- Moderator
- Owner
- User

By default, all users will have the User role. The other three roles should be granted only in these instances:

Channel TypeGroupRoleProjectMaintainersModeratorWorking GroupWG Chair and Vice ChairModeratorSIGSIG Chair and Vice ChairModeratorSIGEcosystem Point of ContactOwnerProgramResponsible LF StaffOwnerAllLF StaffAdminAll (except program and SIG)hyperledger-botOwner

From the above, you will see the following:

- Some of our channel types will not have moderators. This is because there is no one person or set of people who act in this role.
- Ownership is only provided to LF Staff. Owners can perform the following tasks over and above moderators that should not be provided to the community: Archive Room, Delete Public Channels, Force Delete Message, Set Leader, Set Moderator, Set Owner,  Set React when ReadOnly, Set ReadOnly.
- All channels, except program and SIG channels, will have the owner set to a Hyperledger-owned account to allow for administrators to leave channels that they created.

Document generated by Confluence on Nov 26, 2024 13:04

[Atlassian](http://www.atlassian.com/)
