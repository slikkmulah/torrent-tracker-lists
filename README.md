# torrent-tracker-lists
these lists are updated daily

*HOW TO CHECK TRACKERS FOR VALIDITY*

trackerping
===========

Connectivity test tool for BitTorrent trackers.

## Usage

Install it via pip:

```bash
pip install trackerping
trackerping -h
```

... or directly download and run the script:

```bash
pip install -r ./requirements.txt
python3 ./trackerping.py -h
```

### Ping a single tracker

Ping a single tracker url and print the result.

```bash
trackerping http://tracker.example.com/announcen
trackerping --timeout=10 udp://tracker.example.com:80/announce
trackerping ws://webtorrent.example.com:80/announce
```

### Ping all treackers in a trackerslist

Ping all trackers url in a local or remote trackerslist (one url per line).

```bash
trackerping -l ./trackerslist.txt
trackerping -l https://example.com/trackerslist.txt
```

Write available trackers to the new trackerslist:

```bash
trackerping -l -o ./newtrackerslist.txt https://example.com/trackerslist.txt
```
