---
cascade:
  project: Corda
  version: 'Corda 5.2'
  section_menu: corda52
description: "CorDapp Developer documentation for Corda 5.2."
title: "Developing Applications"
date: 2023-04-21
menu:
  corda52:
    identifier: corda52-develop
    weight: 3000
---
# Developing Applications

This section describes the tasks performed by {{< tooltip >}}CorDapp{{< /tooltip >}} Developers. For more information about the architecture of Corda 5 from the perspective of CorDapp Developers, see the [Key Concepts section]({{< relref "../key-concepts/cordapp-dev/_index.md" >}}). Depending on the stage of development, Corda supports the following types of networks:

* [Static](#static-networks)
* [Dynamic](#dynamic-networks)

## Static Networks

Static networks are intended for local testing when the list of virtual nodes or members in the network are predetermined.
These networks are composed of only a single cluster as there is no instance of the Membership Group Manager ({{< tooltip >}}MGM{{< /tooltip >}}) to distribute member data across clusters.
For information about deploying locally to a static network with the combined worker, see [Corda Runtime Gradle Plugin Template]({{< relref "./cordapp-template/_index.md" >}}).

## Dynamic Networks

Dynamic networks are used for the following:

* Production networks
* Testing across multiple clusters
* Testing when the number of members are not predetermined in your test network

One of the main differences to static networks is that there is a running MGM that all members must register with before they can transact among the group. The MGM is also responsible for distributing member data across clusters.
