Ferret code f02, age p0, no cortex.
26 Octobre 2015, R. Toro

I eroded the original segmentation of the pial surface to eliminate the cortex, and manually corrected the segmentation (using StereotaxicRAMON, file eroded-BF02_11012013_MGE_TEsum_magn-cerebellum). I saved the selection as a binary mask using the command saveSelection. The result is the file p0-f02.img/hdr (Analyze format). I used isosurf v1.5 to make a triangular mesh: po-f02.wrl. I used meshgeometry to convert that to PLY format, imported the file into MeshLab, inverted the face normals, decimated the triangulation; result: p0-f02-dec.ply. Used MeshSurgery to fix the mesh to have Euler caracteristic=0; smoothed the mesh using a Taubin lambda/mu smooth (20 iterations with default settings); result: p0-f02-dec-tau.ply. Used meshgeometry to subdivide the mesh using the sqrt(3) algorithm.

Final result: p0-f02-dec-tau-sub.ply


