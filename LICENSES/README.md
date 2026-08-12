# Asset licences

`cortical_maps` ships **no brain data**. It fetches assets on demand (see `cortical_maps.downloader`)
and this folder carries the terms under which the redistributable ones (bucket A) travel. Each asset's
licence is recorded in `../manifest.toml` and announced when the file is fetched; a
`<file>.provenance.json` sidecar records it permanently on disk. Query any time with `cm.license(name)`.

| Licence | File | Assets it governs |
|---|---|---|
| HCP Open Access DUT | `HCP-OpenAccess-DataUseTerms.txt` | fs_LR surfaces, sulc, medial walls, registration spheres, **Glasser HCP-MMP1.0** |
| FreeSurfer v1.0 | `FreeSurfer-LICENSE.txt` | fsaverage/6/5 surfaces + sulc; Destrieux, Desikan parcellations |
| MIT (CBIG) | `CBIG-MIT-LICENSE.txt` | Schaefer 2018, Yeo 2011 parcellations |

**Not redistributed here (bucket B).** Some parcellations carry no redistribution grant, or a
non-commercial restriction (FreeSurfer Brodmann BA_exvivo), or exist only in another space upstream
(Gordon, von Economo). `cortical_maps` records their terms in the manifest but does not ship the files:
obtain them from their upstream source. Brodmann's non-commercial download is gated behind
`CORTICAL_MAPS_ACCEPT_NONCOMMERCIAL=1`.
