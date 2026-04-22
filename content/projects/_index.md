---
title: Projects
---

Here are some of the projects I've worked on — feel free to explore and reach out if anything catches your eye.

## CVE Notifier

A Discord bot that monitors the [NVD (National Vulnerability Database)](https://nvd.nist.gov/) and posts new and updated CVEs to a Discord channel in real time. It runs in two modes — syncing the full database on startup, then polling every 30 minutes for new or updated CVEs. Supports a `/cve` slash command to look up any CVE by ID.

**GitHub:** [cve-notifier](https://github.com/ssung099/cve-notifier)  
**Tech Stack:** Python, Discord.py, SQLite

Here is an example of a CVE notification embed posted to Discord, showing the CVE ID, description, publish time, CVSS score, severity, and CWE classification.
![CVE Notifier](/images/projects/cve_message.png)

## BitTorrent Client

A Python BitTorrent client that downloads files from peers using the BitTorrent protocol, verifying each piece against the torrent metadata before writing to disk. Once the download is complete, the client seeds the file back to the network. Includes a local testing client for verifying seeding behavior directly on the same machine without going through a tracker.

**GitHub:** [BitTorrent-Client](https://github.com/ssung099/BitTorrent-Client)  
**Tech Stack:** Python

Here is the client downloading `debian-13.4.0-arm64-netinst.iso` from peers.
![BitTorrent Client downloading](/images/projects/bittorrent.png)

The local tester connects directly to the client once it enters seeding mode, and successfully downloads the same file from our client.
![BitTorrent local tester](/images/projects/bittorrent_local.png)

Both downloads produce the same SHA512 hash, which also matches Debian's [official SHA512SUMS](https://cdimage.debian.org/debian-cd/current/arm64/iso-cd/SHA512SUMS), confirming end to end file integrity.