# TSD: Tooth Structured Instance Segmentation Dataset (Early Access Version)

A dataset for tooth structured instance segmentation of dental panoramic X-ray.

![Tooth Structured Instance Segmentation](dsis-dpr.gif)

We commit to fully open-sourcing our data once it passes the ethical review by the hospital.

## Download Link

The dataset will be available for download . Stay tuned for updates.

[Google Drive Download Source](https://drive.google.com/file/d/1TSxERnUNkguPM3cPqBvzEqXFCjGtXt7E/view?usp=drive_link)
[Baidu Yun Download Source](https://pan.baidu.com/s/1BizJp9d7DAio3sHYpaNGfA?pwd=piat)

## Dataset Structure

The dataset is organized as follows:

```
TSD/
├── images
│   ├── img_001.png
│   ├── img_002.png
│   ├── img_003.png
│   └── ...
├── train/val/test_json_files/
│   ├── info
│   ├── license
│   ├── images_reference
│   ├── annotations/
│   │   ├── instance 1
│   │   ├── instance 2
│   │   │   ├── segmentation (list)
│   │   │   │   ├── instance_polygons
│   │   │   │   ├── dentin_polygons
│   │   │   │   ├── pulp_polygons
│   │   │   │   ├── materials_polygons
│   │   │   │   └── decay_polygons
│   │   │   ├── image_id (image ref of instance)
│   │   │   ├── instance_bounding_box
│   │   │   └── instance_id
│   │   └── ... instance n
```
Each segmentation annotation consists of a list of 5 items, with all polygons represented by sequences of points in the format (x1, y1, x2, y2, ...). 

To organize the structured instance of a tooth, arrange the polygons in the specified order.

## Paper

Our research paper provides detailed information about the dataset, the methodology used for annotation, and the results of our experiments.

[Read the paper here](https://ieeexplore.ieee.org/abstract/document/10520935/)

## Citation

If you use this dataset in your research, please cite our paper as follows:

```bibtex
@article{wang2024dsis,
  title={DSIS-DPR: Structured Instance Segmentation and Diffusion Prior Refinement for Dental Anatomy Learning},
  author={Wang, Xianyun and Wang, Linhong and Yang, Zhenchen and Zhou, Jiacong and Zheng, Yuchen and Chen, Feng and Hong, Richang and Yu, Jun and Yang, Fan},
  journal={IEEE Transactions on Multimedia},
  year={2024},
  publisher={IEEE}
}
