---
layout: component
title: "Owntracks"
description: "Instructions how to use Owntracks to track devices in Home Assistant."
date: 2015-09-22 07:00
sidebar: true
comments: false
sharing: true
footer: true
logo: owntracks.png
ha_category: Presence Detection
featured: true
---


This platform allows you to detect presence using [Owntracks](http://owntracks.org/). OwnTracks allows users to track their location on Android and iOS phones and publish it to an MQTT broker. This platform will connect to the broker and monitor for new locations.

This component requires [the MQTT component](/components/mqtt/) to be set up and works very well together with [the zone component](/components/zone/).

To integrate Owntracks in Home Assistant, add the following section to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry
device_tracker:
  platform: owntracks
```

There is no further configuration needed for tracking Owntracks devices.

Owntracks can also be used with other device trackers, such as [Nmap](/components/device_tracker.nmap_scanner/) or [Netgear](/components/device_tracker.netgear/). To do this, fill in the `mac` field to the Owntracks entry in `known_devices.yaml` with the MAC address of the device you want to track. This way the state of the device will be determined by the source that reported last.
