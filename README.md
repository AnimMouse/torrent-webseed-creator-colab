# Torrent Webseed Creator on Colab
Webseeded Torrent Creator using Google Colaboratory.

Inspired by [BurnBit †](https://web.archive.org/web/20160304022643/http://burnbit.com/) and [URLHash](http://www.urlhash.com).

Powered by [torrenttools](https://github.com/fbdtemme/torrenttools) to create a torrent file.

An alternative to BurnBit and URLHash.

Convert direct HTTP link to .torrent

Your file is then burned into a torrent.

Torrents created are trackerless, relying on Distributed Hash Table and Peer EXchange, to help reduce the burden of torrent trackers.

For people that have unstable internet.\
Can be paused because it is a torrent.\
Utilizes the power of peer to peer downloads and the client-server downloads.\
Combines the best of both worlds (P2P and Direct HTTP Link).

## How to use
1. Open in Google Colaboratory.
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AnimMouse/torrent-webseed-creator-colab/blob/main/Torrent_Webseed_Creator.ipynb)
2. Input data on form.
   * Name: The name of the torrent file.
   * Comment: The comment inside the torrent file.
   * URL: The URL of the file to download and create a torrent from.
   * File name: The file name of the file you will create a torrent from.
   * Piece size: The size of the torrent pieces in power of 2 (2^n) or in kilobyte (KB) or auto for automatic calculation.
   * Protocol Version: The version of BitTorrent protocol to use. Either [v1](https://www.bittorrent.org/beps/bep_0003.html), [v2, or hybrid](https://www.bittorrent.org/beps/bep_0052.html).
3. Click play in every cell.

### URL requirements
1. URL must be accessible without cookies. [Source](http://www.urlhash.com)
2. The URL should not expire, or it will stop working sometime if there is not enough seeders. [Source](https://web.archive.org/web/20160310075751/http://burnbit.com/faq#httpseeds)

### Recommend piece size
| Piece Size | torrenttools | for file sizes     |
|------------|--------------|--------------------|
| Automatic  | auto         | Any                |
| 512 KiB    | 19 or 512K   | 512 MiB - 1024 MiB |
| 1024 KiB   | 20 or 1024K  | 1 GiB - 2 GiB      |
| 2048 KiB   | 21 or 2048K  | 2 GiB - 4 GiB      |
| 4096 KiB   | 22 or 4096K  | 4 GiB - 8 GiB      |
| 8192 KiB   | 23 or  8192K | 8 GiB - 16 GiB     |
| 16384 KiB  | 24 or 16384K | 16 GiB - 512 GiB   |
| 32768 KiB  | 25 or 32768K | >512 GiB           |

Source: [Seedboxes.cc](https://community.seedboxes.cc/articles/how-to-create-a-torrent-via-the-command-line)

### File size limit
As of 2024-02-27
* CPU: ≈81.3 GB
* T4 GPU: ≈51.9 GB
* TPU: ≈79 GB

#### Alternatives
1. [Torrent Webseed Creator on GitHub Actions](https://github.com/AnimMouse/torrent-webseed-creator)