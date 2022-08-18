# Segmentation


## Semantic Segmentation

### [U-Net: Semantic segmentation with PyTorch](https://github.com/milesial/Pytorch-UNet)
<details>

<summary>Conda env.</summary>

```bash
$ conda create -n UNet python=3.9 -y
$ conda activate UNet
```
  
</details>

### [Semantic Segmentation on MIT ADE20K dataset in PyTorch](https://github.com/CSAILVision/semantic-segmentation-pytorch)
<details>

<summary>Environment setup</summary>

```bash
$ conda create -n SemanticSegmentation python=3.7 -y
$ conda activate SemanticSegmentation

$ git clone https://github.com/CSAILVision/semantic-segmentation-pytorch
$ cd semantic-segmentation-pytorch/
$ pip install -r requirements.txt
>> scipy
>> torch>=0.4.1
>> torchvision
>> opencv-python
>> yacs
>> tqdm
```
  
</details>

<details>

<summary>Inference</summary>

```bash
$ chmod +x demo_test.sh
$ ./demo_test.sh
  
$ python3 -u test.py \
    --imgs bentley.jpg \
    --cfg config/ade20k-resnet50dilated-ppm_deepsup.yaml \
    DIR ckpt/ade20k-resnet50dilated-ppm_deepsup \
    TEST.result ./ \
    TEST.checkpoint epoch_20.pth
```

</details>

<details>

<summary></summary>

</details>




<details>

<summary></summary>

</details>


## Instance Segmentation

### [You Only Look At CoefficienTs](https://github.com/dbolya/yolact)
<details>

<summary>Environment setup</summary>

```bash


$ git clone https://github.com/dbolya/yolact.git
$ cd yolact/
$ conda env create -f environment.yml
$ conda activate yolact-env
$ # Cython needs to be installed before pycocotools
$ pip install cython
$ pip install opencv-python pillow pycocotools matplotlib 
```
  
</details>

<details>

<summary>Inference</summary>

```bash
$ chmod +x demo_test.sh
$ ./demo_test.sh
  
$ python3 -u test.py \
    --imgs bentley.jpg \
    --cfg config/ade20k-resnet50dilated-ppm_deepsup.yaml \
    DIR ckpt/ade20k-resnet50dilated-ppm_deepsup \
    TEST.result ./ \
    TEST.checkpoint epoch_20.pth
```

</details>

