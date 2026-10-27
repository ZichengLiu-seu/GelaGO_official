# GelaGO Project Page

Static project page for **GelaGO**, served through GitHub Pages.

## Structure

```
.
├── index.html              overview, dataset summary, citation
├── dataset.html            archive layout, feature schema, download
├── code.html               repository status, environment, workflow
├── assets/style.css        single stylesheet, no external dependencies
├── files/
│   └── OpenSourceDataset.7z    AES-256 encrypted archive, 78.3 MB
├── .nojekyll               serve files verbatim, skip Jekyll
└── README.md
```

## Local preview

```
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Deployment

1. Push this repository to GitHub.
2. Open **Settings → Pages**.
3. Set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`.
4. The site appears at `https://<username>.github.io/<repository>/`.

## Archive

`files/OpenSourceDataset.7z` is encrypted with AES-256 and filename encryption.
The extraction password is deliberately not stored in this repository. It is
provided to reviewers through the supplementary material.

Digest of the current archive:

```
sha256  7e0d8c887010d42ae2a1e38629307a0dffb624e7ebee3ecc6394a1fb9f99e371
```

## Replacing the archive

The 78 MB file sits inside the Git history, so every replacement adds a new
blob of the same size. If the archive needs frequent updates, move it to a
release asset and point `dataset.html` at that URL instead.

## Before publishing

- Replace the placeholder title in `index.html` with the full paper title.
- Complete the author list and affiliations.
- Fill in the BibTeX entry.
- Confirm the GitHub URL in `code.html` points at the real private repository.
