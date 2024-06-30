# VD-CVFI

Code relaese for *Describing Visual Attributes with Pre-trained Image Encoder for Few-shot Fine-grained Recognition*.

## Code environment

* You can create a conda environment with the correct dependencies using the following command lines:

  ```shell
  conda env create -f environment.yml
  conda activate VD-CVFI
  ```

## Dataset

The official link of CUB-200-2011 is [here](http://www.vision.caltech.edu/datasets/cub_200_2011/). The preprocessing of the cropped CUB-200-2011 is the same as [FRN](https://github.com/Tsingularity/FRN), but the categories  of train, val, and test follows split.txt. And then move the processed dataset  to directory ./data.

- CUB_200_2011 \[[Download Link](https://drive.google.com/file/d/1WxDB3g3U_SrF2sv-DmFYl8LS0p_wAowh/view)\]
- cars \[[Download Link](https://drive.google.com/file/d/1ImEPQH5gHpSE_Mlq8bRvxxcUXOwdHIeF/view?usp=drive_link)\]
- dogs \[[Download Link](https://drive.google.com/file/d/13avzK22oatJmtuyK0LlShWli00NsF6N0/view?usp=drive_link)\]

## Train

* To train VD-CVFI on `CUB_fewshot_cropped` with Conv-4 backbone under the 1/5-shot setting, run the following command lines:

```shell
cd experiments/CUB_fewshot_cropped/CVF/Conv-4
./train.sh
```

## Test

```shell
cd experiments/CUB_fewshot_cropped/CVF/Conv-4
python ./test.py
```
