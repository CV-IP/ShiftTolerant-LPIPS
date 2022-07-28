
# ShiftTolerant-LPIPS

**Shift-tolerant Perceptual Similarity Metric**

[Abhijay Ghildyal](https://abhijay9.github.io/), [Feng Liu](http://web.cecs.pdx.edu/~fliu/). In ECCV, 2022. [[Arxiv]](https://arxiv.org/abs/2207.13686)

<img src="https://raw.githubusercontent.com/abhijay9/abhijay9.github.io/main/image/st-lpips_teaser.png" width=500>

### Quick start
**Todo**

Please run `python lpips_2imgs.py`

### Test Script

Please download the original BAPPS dataset using this [script (here)](https://github.com/richzhang/PerceptualSimilarity/blob/master/scripts/download_dataset.sh). Then, update path to the dataset in [global_config.json](https://github.com/abhijay9/ShiftTolerant-LPIPS/tree/main/util/config).

To reproduce the results in the paper run the following:

*AlexNet Vanilla*  
`nohup bash n_pixel_shift_study/test_scripts/test.sh alex vanilla 2 64 50 > logs/eval_alex_vanilla.out &`

*AlexNet Shift-tolerant*  
`nohup bash n_pixel_shift_study/test_scripts/test.sh alex shift_tolerant 1 64 50 > logs/eval_alex_shift_tolerant.out &`

**Note:** To train and test our models in this paper, we used Image.BICUBIC. The results are similar when other resizing methods are used. Please feel free to switch back to bilinear as used in the original LPIPS work (here).

### Other Evaluations

For other evaluations refer to [./n_pixel_shift_study/](https://github.com/abhijay9/ShiftTolerant-LPIPS/tree/main/n_pixel_shift_study).

## Citation

If you find this repository useful for your research, please use the following.

```
@inproceedings{ghildyal2022stlpips,
  title={Shift-tolerant Perceptual Similarity Metric},
  author={Ghildyal, Abhijay and Liu, Feng},
  booktitle={ECCV},
  year={2022}
}
```

## Acknowledgements
This repository borrows from [LPIPS](https://github.com/richzhang/PerceptualSimilarity), [Anti-aliasedCNNs](https://github.com/adobe/antialiased-cnns), and [CNNsWithoutBorders](https://github.com/oskyhn/CNNs-Without-Borders) repositories. We thank the authors of these repositories for their incredible work and inspiration.
