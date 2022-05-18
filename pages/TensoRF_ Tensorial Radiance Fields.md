title:: TensoRF: Tensorial Radiance Fields

- Unlike [[NeRF]] that purely uses MLPs, we model the radiance field of a scene as a 4D tensor, which represents a 3D voxel grid with per-voxel multi-channel features.
- Both efficient in training time and compact in memory footprint, and at the same time achieves state-of-the-art rendering quality.