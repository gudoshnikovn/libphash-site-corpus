# libphash-site-corpus

The photo corpus of the [libphash](https://github.com/gudoshnikovn/libphash) documentation
site: 200 photographs from [Wikimedia Commons](https://commons.wikimedia.org/), every one
rated a Quality image by Commons' reviewers and released under CC0 or into the public
domain. The site's charts of how each hash behaves under edits are measured on them.

`photos/` holds each photograph as the site measures it: Commons' standard 1280-pixel-wide
rendition (960 for a portrait), named by the SHA-256 of its bytes. `corpus_photos.tsv`
lists them with the file's name on Commons, its subject, license, author, digest, size, the
URL of the rendition and the page on Commons where the license and the author can be
checked. The libphash repository keeps the same list in `tools/site/corpus_photos.tsv`,
and the site's [photo corpus page](https://gudoshnikovn.github.io/libphash/project/corpus/)
credits every author.

The libphash build downloads the files from a fixed commit of this repository and checks
each one against its digest. A copy is kept here because a page on Commons is a living
one: when a file's description is edited, the metadata inside the rendition changes, and
so do its bytes, while the corpus has to stay the bytes its digests name. A commit here
never changes; a new selection of photographs is a new commit, named by the libphash
manifest that lists it.

## License

Each photograph carries the license its author gave it on Commons, CC0 1.0 or public
domain, as `corpus_photos.tsv` records; neither requires attribution, and the authors are
credited all the same. The rest of this repository (this file) is CC0 1.0.
