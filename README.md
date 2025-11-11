
<p align="center">
  <h1 align="center">
    <img src="media/logo.png" width="50" style="vertical-align: middle; margin-right: 8px;">
    Inpaint360GS: Efficient Object-Aware 3D Inpainting via Gaussian Splatting for 360° Scenes
  </h1>

  <p align="center">
  <a href="https://shaoxiang777.github.io/"><strong>Shaoxiang Wang</strong></a>
  ·
  <a href="https://www.linkedin.com/in/shihong-zhang-97861a293/"><strong>Shihong Zhang</strong></a>
  · 
  <a href="https://scholar.google.com/citations?user=8p9OOd0AAAAJ&hl=en&oi=sra"><strong>Christen Millerdurai</strong></a>
  ·
  <a href="https://www.professoren.tum.de/westermann-ruediger"><strong>R&uuml;diger Westermann</strong></a>
  ·
  <a href="https://www.dfki.de/en/web/about-us/employee/person/dist01"><strong>Didier Stricker</strong></a>
  ·
  <a href="https://www.dfki.de/en/web/about-us/employee/person/alpa02"><strong>Alain Pagani</strong></a>
</p>

<p align="center"> <strong>WACV 2026</strong></p>
    <h3 align="center"><a href="https://dfki-av.github.io/inpaint360gs/">Project Page</a> | <a href="https://dfki-av.github.io/inpaint360gs/">Dataset</a> | <a href="https://arxiv.org/abs/2511.06457">Paper</a> | <a href="https://dfki-av.github.io/inpaint360gs/">Evaluation Result</a></h3>
    <div align="center"></div>
</p>


<p align="center">
  <a href="">
    <img src="./media/teaser.jpg" alt="Logo" width="80%">
  </a>
</p>

<p align="center">
    Inpaint360GS performs flexible, object-aware 3D inpainting in 360° unbounded scenes —
    not only for individual objects, but also for complex multi-object environments.
</p>

## Run
First download and zip the crowd sequence of Inpain360GS dataset
#### 1. Training Object-aware Gaussians 

#### 2. Removing Objects

#### 3. Generating 2D Inpainted Color and Depth

#### 4. 3D Inpaint


## Dataset Structure
1. Inpaint360GS dataset has following structure:
```yaml
  -data
    - {scene_name_1}
      - images
        - IMG_0001.JPG
        - IMG_0002.JPG
        - ...
        - IMG_0050.JPG
        - test_IMG_0051.JPG
        - test_IMG_0052.JPG
        - ...
        - test_IMG_0100.JPG
      - sparse/0
    - {scene_name_2}
```
All images in a scene share the same camera intrinsics and extrinsics.
```test_IMG_xxxx.JPG``` denotes the image after object removal, which serves as input for inpainting evaluation.

2. Prepare your own dataset:
Follow the image naming convention described above, then run:
```
python convert.py -s data/to/your/path --resize --magick_executable convert
```

## Contact
You can contact the author through email: shaoxiang.wang@dfki.de.

## Citing
If you find our work useful, please consider citing:
```BibTeX
@misc{wang2025inpaint360gsefficientobjectaware3d,
      title={Inpaint360GS: Efficient Object-Aware 3D Inpainting via Gaussian Splatting for 360{\deg} Scenes}, 
      author={Shaoxiang Wang and Shihong Zhang and Christen Millerdurai and Rüdiger Westermann and Didier Stricker and Alain Pagani},
      year={2025},
      eprint={2511.06457},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2511.06457}, 
}
```

### Acknowledgement
This work has been partially supported by the EU projects CORTEX2 (GA No. 101070192) and LUMINOUS (GA No. 101135724), as well as by the German Research Foundation (DFG, GA No. 564809505). Special thanks to Shihong Zhang for his contributions during his Master's thesis at DFKI!


<br>
