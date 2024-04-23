# Sim Mesh

Common computer graphics meshes that are (trying to be):

1. Simulation ready.
2. Centered at the origin.
3. Scaled to a unit box.
4. Heading +Y and facing +Z (default camera can be looking at (0,0,0) from (1,1,1)).
5. Small to medium file size.

## Gallery

We provide several representations:

- Triangle Mesh
  - `Tri-1`: Fine triangle mesh with ~100k faces (or textured mesh); `Tri-2`: Coarse triangle mesh with ~5k faces.
  - `.ply` for both. `.obj` and `.png` for textured mesh.
- Tetrahedral Mesh
  - `Tet-1`: Fine tetrahedral mesh with 0.01 edge length; `Tet-2`: Coarse tetrahedral mesh with 0.05 edge length.
  - `.npz` for both. `np.load(f)['verts']` and `np.load(f)['elems']` for vertices and elements respectively.
- Point Cloud
  - `PCD-1`: Fine point cloud with ~100k points; `PCD-2`: Coarse point cloud with ~10k points.
  - `.ply` for both.
- More to come...

| Name | `Tri-1` | `Tri-2` | `Tet-1` | `Tet-2` | `PCD-1` | `PCD-2` |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| [Blub](data/blub)[^1] | ![Triangle Mesh (Texture)](data/blub/images/tri-texture.png) | ![Triangle Mesh (Coarse)](data/blub/images/tri-5000.png) | ![Tetrahedral Mesh (Fine)](data/blub/images/tet-0.01.png) | ![Tetrahedral Mesh (Coarse)](data/blub/images/tet-0.05.png) | ![Point Cloud (Fine)](data/blub/images/pcd-100000.png) | ![Point Cloud (Coarse)](data/blub/images/pcd-10000.png) |
| [Bob](data/bob)[^1] | ![Triangle Mesh (Texture)](data/bob/images/tri-texture.png) | ![Triangle Mesh (Coarse)](data/bob/images/tri-5000.png) | ![Tetrahedral Mesh (Fine)](data/bob/images/tet-0.01.png) | ![Tetrahedral Mesh (Coarse)](data/bob/images/tet-0.05.png) | ![Point Cloud (Fine)](data/bob/images/pcd-100000.png) | ![Point Cloud (Coarse)](data/bob/images/pcd-10000.png) |
| [Nefertiti](data/nefertiti)[^1] | ![Triangle Mesh (Fine)](data/nefertiti/images/tri-100000.png) | ![Triangle Mesh (Coarse)](data/nefertiti/images/tri-5000.png) | ![Tetrahedral Mesh (Fine)](data/nefertiti/images/tet-0.01.png) | ![Tetrahedral Mesh (Coarse)](data/nefertiti/images/tet-0.05.png) | ![Point Cloud (Fine)](data/nefertiti/images/pcd-100000.png) | ![Point Cloud (Coarse)](data/nefertiti/images/pcd-10000.png) |
| [Spot](data/spot)[^1] | ![Triangle Mesh (Texture)](data/spot/images/tri-texture.png) | ![Triangle Mesh (Coarse)](data/spot/images/tri-5000.png) | ![Tetrahedral Mesh (Fine)](data/spot/images/tet-0.01.png) | ![Tetrahedral Mesh (Coarse)](data/spot/images/tet-0.05.png) | ![Point Cloud (Fine)](data/spot/images/pcd-100000.png) | ![Point Cloud (Coarse)](data/spot/images/pcd-10000.png) |
| [Armadillo](data/armadillo)[^2] | ![Triangle Mesh (Fine)](data/armadillo/images/tri-100000.png) | ![Triangle Mesh (Coarse)](data/armadillo/images/tri-5000.png) | ![Tetrahedral Mesh (Fine)](data/armadillo/images/tet-0.01.png) | ![Tetrahedral Mesh (Coarse)](data/armadillo/images/tet-0.05.png) | ![Point Cloud (Fine)](data/armadillo/images/pcd-100000.png) | ![Point Cloud (Coarse)](data/armadillo/images/pcd-10000.png) |
| [Bunny](data/bunny)[^2] | ![Triangle Mesh (Fine)](data/bunny/images/tri-100000.png) | ![Triangle Mesh (Coarse)](data/bunny/images/tri-5000.png) | ![Tetrahedral Mesh (Fine)](data/bunny/images/tet-0.01.png) | ![Tetrahedral Mesh (Coarse)](data/bunny/images/tet-0.05.png) | ![Point Cloud (Fine)](data/bunny/images/pcd-100000.png) | ![Point Cloud (Coarse)](data/bunny/images/pcd-10000.png) |
| [Dragon](data/dragon)[^2] | ![Triangle Mesh (Fine)](data/dragon/images/tri-100000.png) | ![Triangle Mesh (Coarse)](data/dragon/images/tri-5000.png) | ![Tetrahedral Mesh (Fine)](data/dragon/images/tet-0.01.png) | ![Tetrahedral Mesh (Coarse)](data/dragon/images/tet-0.05.png) | ![Point Cloud (Fine)](data/dragon/images/pcd-100000.png) | ![Point Cloud (Coarse)](data/dragon/images/pcd-10000.png) |
| [Happy](data/happy)[^2] | ![Triangle Mesh (Fine)](data/happy/images/tri-100000.png) | ![Triangle Mesh (Coarse)](data/happy/images/tri-5000.png) | ![Tetrahedral Mesh (Fine)](data/happy/images/tet-0.01.png) | ![Tetrahedral Mesh (Coarse)](data/happy/images/tet-0.05.png) | ![Point Cloud (Fine)](data/happy/images/pcd-100000.png) | ![Point Cloud (Coarse)](data/happy/images/pcd-10000.png) |
| [Lucy](data/lucy)[^2] | ![Triangle Mesh (Fine)](data/lucy/images/tri-100000.png) | ![Triangle Mesh (Coarse)](data/lucy/images/tri-5000.png) | ![Tetrahedral Mesh (Fine)](data/lucy/images/tet-0.01.png) | ![Tetrahedral Mesh (Coarse)](data/lucy/images/tet-0.05.png) | ![Point Cloud (Fine)](data/lucy/images/pcd-100000.png) | ![Point Cloud (Coarse)](data/lucy/images/pcd-10000.png) |
| [Statue](data/statue)[^2] | ![Triangle Mesh (Fine)](data/statue/images/tri-100000.png) | ![Triangle Mesh (Coarse)](data/statue/images/tri-5000.png) | ![Tetrahedral Mesh (Fine)](data/statue/images/tet-0.01.png) | ![Tetrahedral Mesh (Coarse)](data/statue/images/tet-0.05.png) | ![Point Cloud (Fine)](data/statue/images/pcd-100000.png) | ![Point Cloud (Coarse)](data/statue/images/pcd-10000.png) |
| [XYZ Dragon](data/xyz_dragon)[^2] | ![Triangle Mesh (Fine)](data/xyz_dragon/images/tri-100000.png) | ![Triangle Mesh (Coarse)](data/xyz_dragon/images/tri-5000.png) | ![Tetrahedral Mesh (Fine)](data/xyz_dragon/images/tet-0.01.png) | ![Tetrahedral Mesh (Coarse)](data/xyz_dragon/images/tet-0.05.png) | ![Point Cloud (Fine)](data/xyz_dragon/images/pcd-100000.png) | ![Point Cloud (Coarse)](data/xyz_dragon/images/pcd-10000.png) |

[^1]: [Keenan's 3D Model Repository](https://www.cs.cmu.edu/~kmcrane/Projects/ModelRepository/)
[^2]: [The Stanford 3D Scanning Repository](https://graphics.stanford.edu/data/3Dscanrep/)
