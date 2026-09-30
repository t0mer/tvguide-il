# tvguide-il

An XMLTV electronic programme guide (EPG) for Israeli TV channels, published as a single file: [`guide.xml`](guide.xml).

> [!WARNING]
> **The guide is no longer updated.** The last update was committed on 2024-10-07, and the listings in the file end on 2024-10-13. Any player that loads it today will show no current programmes.

## What's in the file

| | |
|---|---|
| Format | [XMLTV](https://github.com/XMLTV/xmltv/blob/master/xmltv.dtd) (`<tv>` root with `<channel>` and `<programme>` elements), UTF-8 |
| Generator | [WebGrab+Plus](http://www.webgrabplus.com) 5.2 (from the file's `generator-info-name` attribute) |
| Channels | 170 |
| Programme entries | 23,662 |
| Date range | Programmes starting 2024-10-07 to 2024-10-13 |
| Size | About 12 MB |

Each `<channel>` has a display name tagged `lang="he"` (in Hebrew or Latin script), a link to the source site and, for most channels (133 of 170), a logo URL. The listings come from the HOT (`hot.net.il`, 106 channels) and yes (`yes.co.il`, 64 channels) websites; the listings and logos belong to their respective providers.

## Usage

Point any XMLTV-capable player or server at the raw file URL:

```
https://raw.githubusercontent.com/t0mer/tvguide-il/main/guide.xml
```

For example, use it as the EPG source in Tvheadend (XMLTV grabber), Jellyfin or Plex Live TV, Kodi's IPTV Simple Client, or an IPTV app. Channel IDs in the file are channel names (for example `MTV MUSIC`), so you may need to map them to your own channel list.

Keep in mind the warning above: the data is outdated.

## How it was produced

The file was generated with WebGrab+Plus and committed as "Update tvguide" commits, usually several times a day but with gaps of up to 11 days, from June to October 2024. The WebGrab+Plus configuration and whatever pushed the updates are not part of this repository.

## License

The repository is licensed under the [Apache License 2.0](LICENSE). The programme listings and channel logos remain the property of their respective owners.
