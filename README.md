# PosterLayout: A New Benchmark and Approach for Content-aware Visual-Textual Presentation Layout

This repository contains the benchmark and Pytorch implementation of "PosterLayout: A New Benchmark and Approach for Content-aware Visual-Textual Presentation Layout", CVPR 2023.

For more details and **dataset downloads**, please visit our [project page](http://59.108.48.34/tiki/PosterLayout/).

## How to Run
### Prerequisites

If your operating system is ```linux-64```, directly run
```
conda create --name yourenvname --file spec-file.txt
```

Otherwise, 
- Environment
```
Python 3.9
CUDA 11.0
```
- Module
```
torch==1.12.1
torchvision==0.13.1
timm==0.6.5
opencv-python==4.6.0.66
pandas==1.4.3
Pillow==9.2.0
```

### Models
1. Download pre-trained weights from [PKU Netdisk](https://disk.pku.edu.cn:443/link/B11CA3D24A7A59332A3DDDF2A0A608B2) or [Google Drive]()
2. Put pth files under ```model_weight``` and ```output```, as follow:
```
model_weight/
├─ resnet18-5c106cde.pth
├─ resnet50_a1_0-14fe96d1.pth
output/
├─ DS-GAN-Epoch300.pth
```

### Dataset
1. Download PKU PosterLayout from the [project page](http://59.108.48.34/tiki/PosterLayout/)
2. Unzip compressed files to corresponding directories
3. Put directories under ```Dataset/```, as follow:
```
Dataset/
├─ train/
│  ├─ inpainted_poster/
│  ├─ saliencymaps_basnet/
│  ├─ saliencymaps_pfpn/
├─ test/
│  ├─ image_canvas/
│  ├─ saliencymaps_basnet/
│  ├─ saliencymaps_pfpn/
├─ train_csv_9973.csv
```

### Usage
- Training
```
sh train.sh
```

- Testing and Evaluating
```
sh test_n_eval.sh
```

## Paper
If our work is helpful for your research, please cite our paper:
```
@inproceedings{Hsu-2023-posterlayout,
    title={PosterLayout: A New Benchmark and  Approach for Content-Aware Visual-Textual Presentation Layout},
    author={HsiaoYuan Hsu, Xiangteng He, Yuxin Peng, Hao Kong and Qing Zhang},
    booktitle={Proceedings of IEEE Conference on Computer Vision and Pattern Recognition (CVPR)},
    year={2023}
}
```

## Contact us
For any questions or further information, please email Mrs. Hsu (kslh99@stu.pku.edu.cn).
