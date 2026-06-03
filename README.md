# AI for Biomedical Systems & Critical Systems

A Beamer presentation covering safety, reliability, regulation, and deployment patterns for AI in biomedical and critical systems — built for the UAB Heersink School of Medicine.

## Files

| File | Description |
|------|-------------|
| `ai_biomedical_critical_systems_beamer.tex` | Beamer source |
| `.github/workflows/build-pdf.yml` | GitHub Actions workflow |

## Build locally

Requires `xelatex` and the following TeX Live packages:
`texlive-xetex`, `texlive-latex-extra`, `texlive-fonts-extra`, `texlive-science`, `texlive-pictures`, `lmodern`

```bash
# Ubuntu/Debian
sudo apt-get install texlive-xetex texlive-latex-extra texlive-fonts-extra \
  texlive-science texlive-pictures lmodern

# Compile (two passes to resolve frame numbers)
xelatex ai_biomedical_critical_systems_beamer.tex
xelatex ai_biomedical_critical_systems_beamer.tex
```

## Download the built PDF via GitHub Actions

1. Open the repository on GitHub.
2. Click **Actions** in the top nav.
3. Open the latest successful workflow run.
4. Download the `beamer-pdf` artifact.

## Notes

- The original workflow template used `xu-cheng/latex-action@v3`, which relies on a Docker image that may not have `lmodern` installed by default. This workflow installs dependencies directly on `ubuntu-latest` to avoid that issue.
- Two compile passes are required: the first builds the document, the second resolves frame-number cross-references.
- Governance framing is based on the NIST AI RMF: Govern, Map, Measure, Manage.
