# bookedforwhat-assets

Image host for the [@bookedforwhat](https://instagram.com/bookedforwhat) pipeline.

Everything here is **public domain**, sourced from Wikimedia Commons. Each file
is named `<year>-<commons-title>.jpg` and its provenance is recorded in
`manifest.json` alongside the original Commons URL and licence.

This repo exists because two services in the pipeline can only ingest images
from a public URL:

- **Canva** cannot fetch from Wikimedia at all. `upload.wikimedia.org` returns
  403 to any request without a User-Agent, and Canva's fetcher sends none.
- **The Instagram Graph API** will not accept uploaded bytes; image containers
  require a publicly reachable URL.

`raw.githubusercontent.com` serves both without authentication.
