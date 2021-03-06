---
layout: documentation
title: Documentation - Introduction to NAT64
---

# [Doc](doc-index.html) > [Introduction](doc-index.html#introduction) > Jool

## Index

1. [Overview](#overview)
2. [Compatibility](#compatibility)
3. [Considerations](#considerations)

## Overview

Jool is an Open Source implementation of a Stateful NAT64 on Linux. It is intended to comply perfectly with the RFC. As of now (2014-07-30), we're one feature away from the goal:

1. <a href="https://github.com/NICMx/NAT64/issues/41" target="_blank">Filtering policies</a>.

## Compatibility

We're supposed to support Linux kernels 3.0.0 and up. While most of the development time has been spent experimenting on Ubuntu 12.04 using kernel 3.2.0-63-generic-pae, we've performed a healthy amount of formal testing on Jool 3.1.5 in the following variants:

| Distribution | Kernels |
| -------------|---------|
| CentOS 7 | 3.10.0-123.el7.x86_64 |
| Debian 7.5 | 3.2.0-4-amd64 |
| Red Hat Enterprise Linux 7 | 3.10.0-123.4.4.el7.x86_64 |
| SuSE Linux Enterprise Desktop 11 SP3 | 3.0.101-0.31-default |
| Ubuntu 12.04 | 3.1.10-030110-generic, 3.2.60-030260-generic |
| Ubuntu 12.10 | 3.3.8-030308-generic, 3.4.94-030494-generic, 3.5.7-03050733-generic |
| Ubuntu 13.04 | 3.6.11-030611-generic, 3.7.10-030710-generic, 3.8.13-03081323-generic |
| Ubuntu 13.10 | 3.9.11-030911-generic, 3.10.44-031044-generic, 3.11.10-03111011-generic |
| Ubuntu 14.04 | 3.12.22-031222-generic, 3.13.11-03131103-generic |
| Ubuntu 14.10 | 3.14.8-031408-generic, 3.15.1-031501-generic |

Red Hat and CentOS introduce a compilation warning due to a kernel version mismatch between Red Hat-based kernels and Debian-based kernels. <a href="https://github.com/NICMx/NAT64/issues/105" target="_blank">We're still researching ways to address this warning</a>, but it hasn't caused any problems during testing.

## Considerations

Our missing feature (see above) means that you cannot firewall your packets being translated. If you need to filter, you're better off placing another node next to the NAT64 to do the task.

And that's really all you need to know to [install](mod-install.html).

