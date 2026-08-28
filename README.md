# Optima Art Assets

Public artwork images for Optima Academy Online, served from GitHub Pages and embedded in
Canvas lessons and the Art Reference Library widget.

**Every image here is free to use with no conditions attached.** Two routes get an image
into this repo, and `manifest.json` records which one each took in `image_source`:

- **17 from Optima's own files**, where the file itself carries an explicit CC0
  public-domain dedication in its metadata.
- **24 re-sourced from Wikimedia Commons**, where the artwork is out of copyright but our
  own copy is not redistributable. Each was confirmed by comparing it side by side with
  our copy before publication; a licence check cannot tell the right title on the wrong
  painting. Public domain / PD-Art / PD-old / CC0 only, never CC-BY or CC-BY-SA.

This is not the catalogue.

| | |
|---|---|
| Images | 41 |
| Long edge | 1600 px |
| Total size | 16.5 MB |
| Base URL | `https://optimaondemand.github.io/optima-art-assets/` |
| Manifest | [`manifest.json`](manifest.json) |

## This repo is generated. Do not hand-edit it.

Images and `manifest.json` are written by `_build/publish_assets.py` in the **private**
[`optima-art-library`](https://github.com/optimaondemand/optima-art-library) repo, which
holds the 529-work catalogue, the rights pipeline and the publish gate. To add or change
an image, run the pipeline there and push the output here. A hand-edit will be silently
overwritten on the next build, and worse, it bypasses the licence gate.

## Why so few images for so large a catalogue

The catalogue holds 529 distinct works. 41 are here. The gap is not copyright — most of
those 529 works are centuries out of copyright — it is **redistribution licence**.

The source files were exported from Artstor (now Images on JSTOR), and 433 of 480 of them
carry embedded XMP reading *"This item is part of an Artstor Collection."* Paid
subscription access is not a right to republish, so a 500-year-old painting can be firmly
in the public domain and still not ours to upload. Those works are catalogued with a
JSTOR link instead of an image, and are being progressively re-sourced from Wikimedia
Commons and museum open-access programmes.

Full disposition of the catalogue:

| Disposition | Works | Meaning |
|---|---|---|
| publish | 41 | free to publish: 17 CC0 in our own files, 24 verified Commons replacements |
| re-source | 54 | public domain, but find a freely licensed copy first |
| link-only | 365 | still in copyright, or the photograph carries its own rights |
| research | 94 | no reliable date established; decide nothing yet |

## Filenames are work ids, not titles

`images/aw_7fa594b483fb.jpg`, not `images/seurat-bathers.jpg`. Work ids are ledger-backed
and never change; titles change the moment a record is verified against a real source.
A lesson page that links an image by work id keeps working after any amount of
re-cataloguing. Look the id up in `manifest.json`.

## Using an image

```html
<img src="https://optimaondemand.github.io/optima-art-assets/images/aw_7fa594b483fb.jpg"
     alt="Georges Seurat, Study for &quot;Bathers at Asnieres&quot;, c. 1883-84">
```

Do not hotlink from a museum's own servers instead — several block requests carrying a
`github.io` referer, which is why these are self-hosted.

## Attribution

CC0 imposes no attribution requirement. Credit the artist anyway: `manifest.json` carries
`creator`, `creator_full` (with nationality and life dates), `title`, `date`, and a
`jstor_url` pointing at the catalogue record the file came from.
