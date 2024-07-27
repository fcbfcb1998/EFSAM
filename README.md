# EFSAM
Error-Filterd Segment Anything Model for Few-shot Semantic Segmentation

Our model relies on two models, BAM and SAM.

Firstly, clone **[BAM](https://github.com/chunbolang/BAM)**, and download datasets and model weights.

Then, clone **[SAM](https://github.com/facebookresearch/segment-anything)**, and download model weights.

cd BAM-main, mkdir visual, and visual/query, visual/output, visual/label/, visual label2.

Copy our test_EF.py/test_EF.sh and test_save.py/test_save.sh to BAM-main, run 

```
sh test_save.sh
```

Then, copy
