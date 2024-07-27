# EFSAM
TITLE: Error-Filterd Segment Anything Model for Few-shot Semantic Segmentation

Our model relies on two models, BAM and SAM.

Firstly, clone **[BAM](https://github.com/chunbolang/BAM)**, and download datasets and model weights.

Then, clone **[SAM](https://github.com/facebookresearch/segment-anything)**, and download model weights.

cd BAM-main, make new folder visual, and visual/query, visual/output, visual/label/, visual label2.
```
mkdir visual
```

Copy our test_EF.py/test_EF.sh and test_save.py/test_save.sh to BAM-main, run 

```
sh test_save.sh
```

Then, copy visual folder to ../segment-anything-main/notebooks.

Copy our EFSAM.ipynb to ../segment-anything-main/notebooks. Make new file output2 and output2pt.
```
mkdir output2
```
Run EFSAM.ipynb to get results and save in output2/output2pt.

Copy output2pt to ../BAM-main, run
```
sh test_EF.sh
```
To get the final results by EF-SAM.
