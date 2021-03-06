## High-Resolution Image Inpainting using Multi-Scale Neural Patch Synthesis

![teaser](images/teaser.png "Sample inpainting results on held-out ImageNet images")

This is the code for [High-Resolution Image Inpainting using Multi-Scale Neural Patch Synthesis](https://arxiv.org/pdf/1611.09969). Given an image, we use the content and texture network to jointly infer the missing region. This repository contains the pre-trained model for the content network and the joint optimization code, including the demo to run example images. The code is adapted from the [Context Encoders](https://github.com/pathak22/context-encoder) and [CNNMRF](https://github.com/chuanli11/CNNMRF). Please contact [Harry Yang](http://www.harryyang.org) for questions regarding the paper or the code. Note that the code is for research purpose only.

### Demo

1. Install Torch:  http://torch.ch/docs/getting-started.html#_

2. Clone the repository
```Shell
  git clone https://github.com/leehomyc/High-Res-Neural-Inpainting.git
```

   Run the Demo
```Shell
  cd High-Res-Neural-Inpainting
  # This will populate the `./models/` folder with trained content models.
  bash ./models/download_content_models.sh
  # This will use the trained model to generate the output of the content network
  th run_content_network.lua
  # This will use the trained model to run texture optimization
  th run_texture_optimization.lua
  # This will generate the final result
  th blend.lua
```


### Citation

If you find this code useful for your research, please cite:

```
@article{yang2016high,
  title={High-Resolution Image Inpainting using Multi-Scale Neural Patch Synthesis},
  author={Yang, Chao and Lu, Xin and Lin, Zhe and Shechtman, Eli and Wang, Oliver and Li, Hao},
  journal={arXiv preprint arXiv:1611.09969},
  year={2016}
}
```


