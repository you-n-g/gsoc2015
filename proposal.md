MY GSOC 2015 Proposal
=====================

## Basic Info
Project Info
- [Google Kubernetes](https://github.com/GoogleCloudPlatform/kubernetes/)
- Project Idea: [Make kubectl awesome](https://github.com/GoogleCloudPlatform/kubernetes/issues/5275)

Applicant Info
- Name: Young Yang
- IRC: young
- Github: [you-n-g](https://github.com/you-n-g)
- [Contribution to Kubernetes so far](https://github.com/GoogleCloudPlatform/kubernetes/commits?author=you-n-g)
- Education:
    - 2014.09-present: [Institute of Software Chinese Academy of Sciences](http://english.is.cas.cn/), Master, Computer Software and Theory
    - 2008.09-2012.06: [Beihang University](http://ev.buaa.edu.cn/), Bachelor, Software Engineering.
- Email: XXXX
- Phone: XXXX


## Abstract
Kubernetes is an open source system for managing containerized applications across multiple hosts, providing basic mechanisms for deployment, maintenance, and scaling of applications. However, there is still a lot of room for improvement. [Make kubectl awesome](https://github.com/GoogleCloudPlatform/kubernetes/issues/5275) is part of the potential improvemens. I love opensource and I'm Interested in Kubernetes. So I'm applying kubernetes as my GSOC2015 project.


## Project Proposal

I'm a master student in UCAS. I love opensource and use [github](https://github.com/you-n-g) quite often. I've some experience of developing systems used by a lot of people, such as [”The Challenge Cup” Online Contest Platform](http://www.tiaozhanbei.net/). I recently learned a lot about docker, kubernetes and GO. Also, I was a participant of ACM ICPC Contests and have ever won the Bronze Medal in The 2009 ACM-ICPC Asia Wuhan Regional Contest.  So far I have committed [some patches to Kubernetes](https://github.com/GoogleCloudPlatform/kubernetes/commits?author=you-n-g).
So I decide to apply kubernetes as my GSOC2015 prject and contribute my efforts to [Make kubectl awesome](https://github.com/GoogleCloudPlatform/kubernetes/issues/5275).  Some ideas for kubectl improvements are listed in the [CLI roadmap](https://github.com/GoogleCloudPlatform/kubernetes/blob/master/docs/cli-roadmap.md). I plan to pick up some of them to make up my GSOC 2015 project.


## Deliverables
The final deliverable would consist of the selected items listed in the [CLI roadmap](https://github.com/GoogleCloudPlatform/kubernetes/blob/master/docs/cli-roadmap.md) and in my schedule. If I have time after finishing these, I'm really glad to contribute my time to other features listed there.

## Technical details
The technical details I have concerned so far are listed below by each item planed in the schedule.
- item 1: It's similar to item 15. But the readiness of services is more complicated.
- item 3: I plan to just add a option to `kubectl create`, such as  "-k pods,services", to filter the object streams.
- item 4: The things that are not pretty enough need to be discussed. I think the printing of some other kubectl commands is also not pretty enough, such as `kubectl version` just print the Info struct literally. I plan to improve them as well.
- item 5: Detailed requirements need to be discussed.
- item 6: Following the code in `pkg/kubectl/cmd/get.go` will let me find which resources are supported, and then list them out.
- item 7: I plan to read the API of swagger and integrate it into kubectl.
- item 8: I plan to overwrite the name according the parameters supplied by `--name` or `--name-suffix`
- item 9: Similar to item 8. The differences I considered are that the labels will be overwrited or added.
- item 10: Similar to item 8, 9.
- item 15: I think the syntax and different meaning of readiness should be descussed. The functions in `kubernetes/pkg/util/wait` can be used. We can support more functions by writing something like `pkg/client/conditions.go`
- item 18: I plan to create a command such as `kubectl derive <pod POD|rc POD REPLICAS|services <POD|RC>> -o output.json`  to generate a json. We may add some options to make it start immediately
- item 25: I think I can find something useful in the command `kubectl get` and integrate some features of it into `kubectl describe`


## Schedule

I’m planning to devote 4 to 5 hours each day from monday to friday and 7 to 8 hours each day in the weekend. Sum up to 34~41 hours a week. I really want to start early to ensure the project is finished on time. I’m certainly willing to make more efforts if the project is behind schedule.

Because I've been familiar with Kubernetes and the community already, I think I can begin coding from April 27 at the latest(I plan to finish some features before that time). There will be about 16 weeks for coding. Accordingly, my planned schedule(the items in my schedule correspond to the items in the [CLI roadmap](https://github.com/GoogleCloudPlatform/kubernetes/blob/master/docs/cli-roadmap.md)):
- week 1: Open a issue for each item if there isn't one and begin or continue all the discussions early. This will make it earsier to trace them and help me understand the requirements more clearly.
- week 2~3: item 3, 4.
- week 4~5: item 5, 6. 
- week 6~7: item 1.
- week 8~9: item 7, 8.
- week 10~11: item 9, 10.
- week 12~13: item 18, 25.
- week 14~15: item 15
- week 16: Handling unforeseen problems if necessary. tidying up any loose ends and do summary.


## Why Kubernetes
I have some experience about Docker and cloud computing and I'm interested in them. Then I found  Kubernetes closely related to them and really fascinating. Besides, the community is really friendly and is a good place for me to learn some knowledge. What's more, I believe Kubernetes will serve numerous projects in the future, it's extremely cool!!!!
