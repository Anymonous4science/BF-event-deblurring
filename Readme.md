# BF Event Deblurring

### Installation
```
pip install -r requirements.txt
python setup.py develop --no_cuda_ext
```
### Dataset 
GoPro with raw events: [[link](https://data.vision.ee.ethz.ch/csakarid/shared/EFNet/GOPRO_rawevents.zip)] from EFNet. Place the dataset in ```./datasets```
It should be like:
  
    ```bash
    ./datasets/
    ./datasets/GOPRO_rawevents/train/
    ./datasets/GOPRO_rawevents/test/

### Train:
```python3 -m torch.distributed.launch --nproc_per_node=8 --master_port=4321 basicsr/train.py -opt options/train.yml --launcher pytorch```


### Test:
Download the pre-trained model from [gdrive](https://drive.google.com/file/d/1cgR8vNu3FBbzNWValoMqq9Yb1ImHDYzE/view?usp=share_link) to ```./pretrained/net_g_bfnet.pth```.

```python3 basicsr/test.py -opt options/test.yml```


### Visual Results:
Download visual results of GOPRO from [gdrive](https://drive.google.com/file/d/15p6Fz7I9KVX6xQPDfnf7BvaI7-Jz9_Ub/view?usp=share_link)

