---
layout: post
title:  "Backup using rclone"
date:   2022-07-10 19:35:53 +0530
categories: cloud drive sync rclone
---
[Rclone][rclone-source] is a command-line program to manage files on cloud storage. It is a feature-rich alternative to cloud vendors' web storage interfaces. Over 40 cloud storage products support rclone including S3 object stores, business & consumer file storage services, as well as standard transfer protocols.

Rclone has powerful cloud equivalents to the unix commands rsync, cp, mv, mount, ls, ncdu, tree, rm, and cat. Rclone's familiar syntax includes shell pipeline support, and --dry-run protection. It is used at the command line, in scripts or via its API.

How to use rclone:

1. [Install rclone][rclone-install]  
`brew install rclone`

2. [Configure rclone][rclone-usage]  
`rclone config` to create new remote
- Follow the steps to configure
  - [box][rclone-config-box]
  - [mega][rclone-config-mega]

3. [rclone copy][rclone-copy]  
`rclone copy "Books/Building Microservices 2nd Edition (9781492034018)/9781492034018.epub"  box:"Books/Building Microservices 2nd Edition (9781492034018)"`

4. [rclone sync][rclone-sync]  
`rclone sync "Books" mega:Books --include "*.epub" -P`

[rclone-source]: https://github.com/rclone/rclone
[rclone-install]: https://rclone.org/install/
[rclone-usage]: https://rclone.org/docs/
[rclone-config-box]: https://rclone.org/box/
[rclone-config-mega]: https://rclone.org/mega/
[rclone-copy]: https://rclone.org/commands/rclone_copy/
[rclone-sync]: https://rclone.org/commands/rclone_sync/
