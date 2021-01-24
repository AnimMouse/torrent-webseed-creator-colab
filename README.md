# Torrent Webseed Creator
Webseeded Torrent Creator using Google Colaboratory.

Inspired by [BurnBit †](https://web.archive.org/web/20160304022643/http://burnbit.com/) and [URLHash](http://www.urlhash.com/).

Powered by [py3createtorrent](https://github.com/rsnitsch/py3createtorrent) to create a torrent file.

An alternative to BurnBit and URLHash.

Convert direct HTTP link to .torrent

Your file is then burned into a torrent.

## How to use
1. Open in Google Colaboratory.
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AnimMouse/torrent-webseed-creator-colab/blob/master/Torrent_Webseed_Creator.ipynb)
2. Input data on form.
   * Name: The name of the torrent file.
   * Comment: The comment inside the torrent file.
   * URL: The URL of the file to download and create a torrent from.
   * File name: The file name of the file you will create a torrent from.
   * Piece size: The size of the torrent pieces in kilobyte or 0 for automatic calculation.
3. Click play in every cell.
4. After the last cell, verify it on your Google Drive.

## URL requirements
1. URL must be accessible without cookies. [Source](http://www.urlhash.com/)
2. The URL should not expire, or it will stop working sometime if there is not enough seeders. [Source](https://web.archive.org/web/20160310075751/http://burnbit.com/faq#httpseeds)

## Recommend piece size
Keep it on 0 for automatic calculation or follow this guide.

* 512 KiB for filesizes between 512 MiB - 1024 MiB
* 1024 KiB for filesizes between 1 GiB - 2 GiB
* 2048 KiB for filesizes between 2 GiB - 4 GiB
* 4096 KiB for filesizes between 4 GiB - 8 GiB
* 8192 KiB for filesizes between 8 GiB - 16 GiB
* 16384 KiB for filesizes between 16 GiB - 512 GiB This is the max you should ever have to use.
* 32768 KiB (note that utorrent versions before 3.x CANNOT load torrents with this or higher piece-size)

Source: [Seedboxes.cc](https://community.seedboxes.cc/articles/how-to-create-a-torrent-via-the-command-line)

## Increase disk space
1. Go to Runtime.
2. Change Runtime Type and give GPU or TPU as the Hardware Accelerator.

## Difference on GitHub Actions version
The [GitHub Actions](https://github.com/AnimMouse/torrent-webseed-creator) version of this program has a soft limit of ≈25 GB, this Google Colaboratory version has a soft limit of ≈100 GB.