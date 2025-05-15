# Benchmarks of Dr. TVAM

## Hardware Specifications

* **RTX3060 12GB (2020)**: Entry-level consumer hardware GPU, priced around **~300USD**.
* **L40S 48GB (2022)**: Professional graphics card used primarily in server clusters, priced around **5000USD**.

## Test Subjects

* **Dr. TVAM**: Tested on **RTX3060 12GB** and **L40S 40GB**.
* **Benchy** boat as target:
  * Size: **10mm**
  * Pixel size: **25µm**
  * Resolution on DMD: **400x400 pixels**
  * Angles: **400**
  * 40 iterations with gradient based L-BFGS optimizer

## Computation Performance

| Configuration | Rays per Pixel | Rendering Time (RTX3060) | Rendering Time (L40S) |
| --- | --- | --- | --- |
| Julia Radon based |1 | **197s** |  |
| index-matched |1 | **122s** | **20s** |
| index-matched |1 | **122s** | **20s** |
| cylindrical |1 | **130s** | **23s** |
| square |1 | **135s** | **20s** |
| cylindrical scattering |16 | **6000s** | **850s** |
| square scattering |16 | **6000s** | **860s** |
| square scattering (surface-aware loss, disable black pixels) |16 | **1500s** | **225s** |

