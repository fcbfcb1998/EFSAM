# EFSAM
# Error-Filterd Segment Anything Model for Few-shot Semantic Segmentation

# Datasets

- PASCAL-5<sup>i</sup>:  [VOC2012](http://host.robots.ox.ac.uk/pascal/VOC/voc2012/) + [SBD](http://home.bharathh.info/pubs/codes/SBD/download.html)

- COCO-20<sup>i</sup>:  [COCO2014](https://cocodataset.org/#download)

   Download the [data](https://mailnwpueducn-my.sharepoint.com/:u:/g/personal/langchunbo_mail_nwpu_edu_cn/ESvJvL7X86pNqK5LSaKwK0sByDLwNx0kh73PVJJ_m1vSCg?e=RBjfKp) lists (.txt files) and put them into the `BAM/lists` directory. 

- Run `util/get_mulway_base_data.py` to generate [base annotations](https://mailnwpueducn-my.sharepoint.com/:f:/g/personal/langchunbo_mail_nwpu_edu_cn/Eg7-69tgeE5Em5jEHUyvafEBA9Gj9ZCtCNV-N8rtcxySKg?e=dFvKW5) for **stage1**, or directly use the trained weights.

# Getting Started

Our model relies on two models, BAM and SAM.

Firstly, clone **[BAM](https://github.com/chunbolang/BAM)**, and download datasets and model weights.

Then, clone **[SAM](https://github.com/facebookresearch/segment-anything)**, and download model weights.

cd BAM-main, make new folder visual, visual/query, visual/output, visual/label, and visual/label2, then make new folder output2pt.
```
mkdir visual
```

Copy our test_EF.py, test_EF.sh and test_save.py, test_save.sh to BAM-main, run 

```
sh test_save.sh
```

Then, cd ../segment-anything-main/notebooks.

Copy our EFSAM.ipynb and EFSAM-multiple.ipynb to ../segment-anything-main/notebooks. Make new file output2.
```
mkdir output2
```
Run EFSAM.ipynb or EFSAM-multiple.ipynb to get results and save in ../../BAM-main/output2pt/. 
- Note: the mIoU results in EFSAM.ipynb and EFSAM-multiple.ipynb are not the final mIOU.
- Note: Do not use EFSAM-old.ipynb and EFSAM-multiple-old.ipynb.

cd ../../BAM-main, run
```
sh test_EF.sh
```
To get the final results by EF-SAM.
