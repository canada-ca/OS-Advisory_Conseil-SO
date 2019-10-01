# Tools Working Group

2019-01-09

## Present

* Guillaume Charest
* Nick Schonning
* Adam Peck
* Jim Cowie
* Mike Nguyen
* Reg Maltais
* Andrew Sinkinson
* Al Akdari
* Caster Parham

## Agenda
* Review OSAB action items
* Review last meeting action items
* New priority: GC Version Control System

## Roundtable

Nick: Back end/help desk, parts of the VCS

Reg: Kent Jacobs (ESDC) for Geospatial already in place and published online.

Mike: Unlimited free private repos for up to 3 collaborators.

There are efforts being made to make it easier to live in both on-premise and online worlds.

PSPC has identified the need for a central DVCS as part of its offerings for other government departments.

Need for scoping:

(Mike) Inner source only for this scope: all departments should have access but not public, yet.

(Reg) If at some point the project is to be released as open source, it would be migrated to an open source repo on a public tool (GitHub, BitBucket, GitLab, etc. online offerings)

(Mike) Enterprise version of GitHub is trying to solve the on-premise/PaaS version.

(Reg) Requirements for 
* internal Inner Source (share across all departments with private repos nonetheless)
* publish open source projects
* might be a need for keeping other VCS in specific departments

Question: 
Hosting internally vs externally (Cloud first)
Hosting production code: day to day use
Accessing repos internally vs publicly (Exception to )

Requirement of solution: Need to provide proper hooks and APIs to support different SDLC models and environments.

Out of scope: CI/CD functionalities

If Cloud based: agnostic of service provider

Open Source instance running on hybrid cloud? Services already exist and the cost may be higher to host.

(Reg) Industry Canada (?) used to host a VCS (RedMind) for internal use.
