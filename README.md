# Finna API — Postman Collection (Finland)

A Postman (v2.1) collection (16 requests) for the **[Finna.fi](https://www.finna.fi) API**. Finna searches the catalogues of about 400 Finnish archives, libraries and museums in one place, including the **National Archives of Finland (Kansallisarkisto)**.

**Import link** (Postman → Import → Link):
```
https://raw.githubusercontent.com/mikeyeves/Finna-API-Postman/main/Finna_API.postman_collection.json
```
You don't need a key or an environment file.

## Folders
| Folder | Requests | Notes |
|---|---|---|
| ★ Search | 10 | Search all fields or by author or subject; date ranges; photos only; ready-made filters for National Archives (KA), Finnish Heritage Agency and SLS; facets and organisation-code lookup |
| Records | 3 | One or several records, including the full source record (MARC, LIDO or EAD) |
| Authorities | 2 | Name records for people, families and organisations |
| Lists | 1 | Public user lists |

Search requests include a **Visualizer** results table with links to finna.fi and image thumbnails. Open the *Visualize* tab to see it.

## Tested at build time
- `Viipuri` limited to photos returned 18,769 records.
- The National Archives of Finland (`building:"0/KA/"`) has about 2.1M records; `Viipuri` within it returned 70,865.
- Author search, the 1850–1900 date-range filter, record lookup and authority search all returned `OK`.

## Useful filter codes
| Organisation | filter |
|---|---|
| National Archives of Finland | `building:"0/KA/"` |
| Finnish Heritage Agency | `building:"0/Museovirasto/"` |
| Swedish Literature Society in Finland | `building:"0/SLS/"` |
| Kansan Arkisto (People's Archives) | `building:"0/kansan_arkisto/"` |
| Photos only | `format:"0/Image/"` |
| Online material only | `online_boolean:"1"` |

Run *Find an organisation code* to look up others, for example local history archives (*kotiseutuarkisto*).

## Genealogy tips
- Finna holds archive **descriptions**, not indexed baptisms. Scanned parish registers are in the National Archives' **Digital Archive** (digi.kansallisarkisto.fi). Transcribed parish records are in **HisKi** (hiski.genealogia.fi), which has no API.
- Place names changed over time: try both the Finnish and Swedish forms (*Viipuri* / *Viborg*, *Turku* / *Åbo*). Set `lng=sv` for Swedish labels.
- Be polite: no more than about 10 requests per second.

## Related collections
[Riksarkivet (Sweden)](https://github.com/mikeyeves/Riksarkivet-API-Postman) · [Norway](https://github.com/mikeyeves/Digitalarkivet-API-Postman) · [Open Archives](https://github.com/mikeyeves/Open-Archives-API-Postman) · [European Archives](https://github.com/mikeyeves/European-Archives-APIs-Postman)

*Unofficial. Not affiliated with Finna or the National Library of Finland.*
