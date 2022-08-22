# Image Segmentation


## Semantic Segmentation

### [U-Net: Semantic segmentation with PyTorch](https://github.com/milesial/Pytorch-UNet)
<details>

<summary>Environment setup</summary>

```bash
$
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
$ pip install -r requirements.txt
$ pip install 'git+https://github.com/cocodataset/cocoapi.git#subdirectory=PythonAPI'
```
  
</details>

<details>

<summary>Inference</summary>
  
#### Image

```bash
$ # Display qualitative results on the specified image.
$ python eval.py --trained_model=weights/yolact_base_54_800000.pth --score_threshold=0.15 --top_k=15 --image=my_image.png

$ # Process an image and save it to another file.
$ python eval.py --trained_model=weights/yolact_base_54_800000.pth --score_threshold=0.15 --top_k=15 --image=input_image.png:output_image.png

$ # Process a whole folder of images.
$ python eval.py --trained_model=weights/yolact_base_54_800000.pth --score_threshold=0.15 --top_k=15 --images=path/to/input/folder:path/to/output/folder
```

#### Video

```bash
$ # Display a video in real-time. "--video_multiframe" will process that many frames at once for improved performance.
$ # If you want, use "--display_fps" to draw the FPS directly on the frame.
$ python eval.py --trained_model=weights/yolact_base_54_800000.pth --score_threshold=0.15 --top_k=15 --video_multiframe=4 --video=my_video.mp4

$ # Display a webcam feed in real-time. If you have multiple webcams pass the index of the webcam you want instead of 0.
$ python eval.py --trained_model=weights/yolact_base_54_800000.pth --score_threshold=0.15 --top_k=15 --video_multiframe=4 --video=0

$ # Process a video and save it to another file. This uses the same pipeline as the ones above now, so it's fast!
$ python eval.py --trained_model=weights/yolact_base_54_800000.pth --score_threshold=0.15 --top_k=15 --video_multiframe=4 --video=input_video.mp4:output_video.mp4
```

</details>




## Reference
