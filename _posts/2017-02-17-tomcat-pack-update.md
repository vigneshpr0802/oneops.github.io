---
layout: post
title:  Tomcat Pack Update
published: false
authors: [bbourquin, mmoser]
---

<img src="/assets/img/logos/integrations/tomcat.png" align="right"/>

The `tomcat`  pack provides version 7.x of the [Apache Tomcat](http://tomcat.apache.org/) web application server
and is a very popular pack for OneOps users running Java-powered web applications. With the 
[recent release](/general/blog/2017-02-15-oneops-release-170215stable.html) we are bringing you an important update to
the pack.

<!--more-->

The pack is updated to Tomcat version 7.0.75 as the new default version from 7.0.70. The upgrade brings numerous fixes
including the important mitigation of the security issue
[CVE-2016-8745](https://tomcat.apache.org/security-7.html#Fixed_in_Apache_Tomcat_7.0.75) 
([original announcement](http://mail-archives.apache.org/mod_mbox/tomcat-announce/201701.mbox/%3C04ead0cb-c989-1386-0fd1-a51ef80f7b57%40apache.org%3E)). 
Check out
[the changelog](http://tomcat.apache.org/tomcat-7.0-doc/changelog.html) for specific details about other changes.

In addition, the OneOps `artifact` component is now propagated to `tomcat`. This means that any updates to the tomcat pack,
such an upgrade to the version from this release, affect the artifact. For example, the artifact could be your 
web application deployed to Tomcat. A change to the `tomcat` pack automatically results in that web application to be
re-deployed to the new application server location and hence also restarted.

We recommend to all users of the `tomcat` pack to upgrade their usage to the latest version and roll out the upgrade to
all affected assemblies and their compute nodes.