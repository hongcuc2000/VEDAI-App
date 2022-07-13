# VEDAI - Vehicle Detection in Aerial Images
- A demo application for graduation thesis about vehicle detection in aerial images.
- The detector is the [TOOD](https://drive.google.com/drive/folders/1OCSTrmViOpQNXB_DlmqoDTdVtlupLBO5?usp=sharing) model that using [UAVDT](https://sites.google.com/view/grli-uavdt/%E9%A6%96%E9%A1%B5) detection dataset for training.

## Note
The app server are built only for UIT private network.
- For UIT, connect to UIT private network before using the app. (Refer to [UIT private network connection guide](https://phongdl.uit.edu.vn/su-dung-openvpn) for remote connection)
- If you are not studying/working at UIT, please install your own server and update the Server IP to try.

## Server installation (for non-UIT only)
- Install Flask
```
pip install Flask
pip install Flask-Cors
```
- Prepare environment
```
conda create -n openmmlab python=3.7 -y
conda activate openmmlab
conda install pytorch==1.7.0 torchvision==0.8.0 torchaudio==0.7.0 cudatoolkit=11.0 -c pytorch
```
- Download and install [MMDetection V2.22.0](https://github.com/open-mmlab/mmdetection/releases/tag/v2.22.0) (Refer to [MMDetection V2.22.0 documentation](https://mmdetection.readthedocs.io/en/v2.22.0/get_started.html#installation)).
```
pip install mmcv-full -f https://download.openmmlab.com/mmcv/dist/cu110/torch1.7.0/index.html
cd mmdetection # The MMDetection directory
pip install -r requirements/build.txt
pip install -v -e .  # or "python setup.py develop"
```
## Reference
- Feng, C., Zhong, Y., Gao, Y., Scott, M. R., & Huang, W. (2021, October). Tood: Task-aligned one-stage object detection. In 2021 IEEE/CVF International Conference on Computer Vision (ICCV) (pp. 3490-3499). IEEE Computer Society.
- Du, D., Qi, Y., Yu, H., Yang, Y., Duan, K., Li, G., ... & Tian, Q. (2018). The unmanned aerial vehicle benchmark: Object detection and tracking. In Proceedings of the European conference on computer vision (ECCV) (pp. 370-386).
- 
