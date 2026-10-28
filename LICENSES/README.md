# Asset licences

`cortexmap` ships **no brain data**. It fetches assets on demand (see `cortexmap.io.assets_toolbox`)
and this folder carries the terms under which the redistributable ones (bucket A) travel. Each asset's
licence is recorded in `../manifest.toml` and announced when the file is fetched; a
`<file>.provenance.json` sidecar records it permanently on disk. Query any time with `cx.license(name)`.

| Licence | File | Assets it governs |
|---|---|---|
| HCP Open Access DUT | `HCP-OpenAccess-DataUseTerms.txt` | fs_LR surfaces, sulc, medial walls, registration spheres, **Glasser HCP-MMP1.0** |
| FreeSurfer v1.0 | `FreeSurfer-LICENSE.txt` | fsaverage/6/5 surfaces + sulc; Destrieux, Desikan, Brodmann (PALS-B12) parcellations |
| MIT (CBIG) | `CBIG-MIT-LICENSE.txt` | Schaefer 2018, Yeo 2011 parcellations |

**Modified FreeSurfer data.** The Brodmann parcellation is the PALS-B12 Brodmann areas (Van Essen
2005) that FreeSurfer ships in `fsaverage/label`, *modified* by cortexmap_dataprep: Brodmann areas
only, resampled from fsaverage to fs_LR 32k. Each file's GIFTI `Description` says so, as the FreeSurfer
licence (Part B 1(d)) requires. It is NOT FreeSurfer's BA_exvivo maps (Fischl 2008), which are
non-commercial.

**Not redistributed here (bucket B).** Some parcellations carry no redistribution grant, or exist only
in another space upstream (Gordon, von Economo). `cortexmap` records their terms in the manifest but
does not ship the files: obtain them from their upstream source. Any asset licensed non-commercial is
gated behind `CORTEXMAP_ACCEPT_NONCOMMERCIAL=1`.
