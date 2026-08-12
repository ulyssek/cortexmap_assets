# cortical_maps_assets

Brain-surface assets fetched on demand by the [`cortical_maps`](https://github.com/ulyssek/brain_statmaps)
Python package — meshes, sulcal-depth maps, medial-wall masks, registration spheres and cortical
parcellations, on the standard human surfaces (fs_LR 32k/164k, fsaverage/6/5).

You do not need to clone this repo. `cortical_maps` downloads individual files from it, on first use,
into a local cache (`~/.cortical_maps/brain_data` by default). It is published here only so that a
plain `pip install cortical_maps` works with no manual data setup.

## Licences — read before reuse

Every file here is redistributed under the terms of its **upstream** source. The full terms live in
[`LICENSES/`](LICENSES/), and each asset's licence is also recorded (with its checksum and citation)
in the package's `manifest.toml`.

| Licence | Assets it governs |
|---|---|
| [WU-Minn HCP Open Access Data Use Terms](LICENSES/HCP-OpenAccess-DataUseTerms.txt) | fs_LR surfaces, sulc, medial walls, registration spheres, and the **Glasser HCP-MMP1.0** parcellation |
| [FreeSurfer Software License v1.0](LICENSES/FreeSurfer-LICENSE.txt) | fsaverage/6/5 surfaces + sulc; Destrieux, Desikan parcellations |
| [MIT — CBIG](LICENSES/CBIG-MIT-LICENSE.txt) | Schaefer 2018, Yeo 2011 parcellations |

Redistribution here is permitted by each of those licences **provided their terms travel with the
data** — which is why `LICENSES/` ships alongside the files. If you use these assets, honour the
attribution/citation each licence requires (see the individual files). The Glasser file is the
fs_LR 32k conversion of the **official HCP dlabel** (governed by the HCP Data Use Terms), not the
fsaverage CC-BY figshare mirror.

Parcellations with no redistribution grant (Gordon, von Economo) or a non-commercial restriction
(FreeSurfer Brodmann) are **deliberately not included** — `cortical_maps` fetches those from their
upstream host, not from here.
