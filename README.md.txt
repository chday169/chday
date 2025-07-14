# 🧊 Marching Cubes Surface Extraction (No Lookup Table)

This project demonstrates a simplified implementation of the Marching Cubes algorithm for 3D surface extraction — without relying on predefined lookup tables. It’s designed to be clear, educational, and adaptable to environments like Scratch and Python.

## ✨ Features

- Extracts surface triangles from an implicit 3D function `f(x, y, z)`
- Detects edge sign changes to locate surface crossings
- Triangulates raw intersection points radially (no lookup tables needed)
- Visualizes the surface from 4 viewpoints using `matplotlib`

## 📈 Example Surface Types

```python
def f(x, y, z, r=0.49, cx=0.5, cy=0.5, cz=0.5, iprob=0):
    if iprob == 0:
        return (x - cx)**2 + (y - cy)**2 + (z - cz)**2 - r**2  # Sphere
    else:
        return (x - cx)**2 + (y - cy)**2 - 2*(z - cz)**2 - r**2  # Hyperboloid
