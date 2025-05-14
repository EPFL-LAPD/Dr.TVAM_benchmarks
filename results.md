# Benchmarks of Dr. TVAM

## Hardware Specifications

* **RTX306012GB (2020)**: Entry-level consumer hardware GPU, priced around **~300USD**.
* **L40S (2022)**: Professional graphics card used primarily in server clusters, priced around **5000USD**.

## Test Subjects

* **Dr. TVAM**: Tested on **RTX306012GB** and **L40S40GB**.
* **Benchy**:
  * Size: **10mm**
  * Pixel size: **25µm**
  * Resolution on DMD: **400x400 pixels**
  * Angles: **400**

## Rendering Performance

### Rendering Configurations

The following configurations were tested on the RTX 3060:
* **Julia-based index-matched**
* **Julia-based cylindrical**

### Performance Results

| Configuration | Rays per Pixel | Rendering Time (RTX3060) | Rendering Time (L40S) |
| --- | --- | --- | --- |
| index-matched |1 | **122s** | **20s** |
| cylindrical |1 | **130s** | **23s** |
| square |1 | **135s** | **20s** |
| cylindrical scattering |16 | **6000s** | **850s** |
| square scattering |16 | **6000s** | **860s** |
| square scattering (surface-aware loss, disable black pixels) |16 | **1500s** | **225s** |

