# VEDAI - Vehicle Detection in Aerial Images
- A demo application for UIT graduation thesis about vehicle detection in aerial images.
- The detector is the [TOOD](https://drive.google.com/drive/folders/1OCSTrmViOpQNXB_DlmqoDTdVtlupLBO5?usp=sharing) model that using [UAVDT](https://sites.google.com/view/grli-uavdt/%E9%A6%96%E9%A1%B5) detection dataset for training.

## Note
The app server are built only for UIT private network.
- For UIT, connect to UIT private network before using the app. (Refer to [UIT private network connection guide](https://phongdl.uit.edu.vn/su-dung-openvpn) for remote connection)
- If you are not studying/working at UIT, please refer to installation guide below.

## Installation (for non-UIT)
### Install Server
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
- Download and upload [demo.py](https://drive.google.com/file/d/1k4ahEhTAH0XXiCfdLKFaimQ-LZoBysA0/view?usp=sharing), [config](https://drive.google.com/file/d/1gZHoNqo2q_9AyqI3F6Fj6MQO_ajbuNfK/view?usp=sharing), [checkpoint](https://drive.google.com/file/d/1I7N8BG20jTtyxFaQI5OyYPo_N95aPxKu/view?usp=sharing) files to server.
- Update the directory of demo_path (folder contains demo.py directory), input_path, output_path, config_file, checkpoint_file in demo.py.
- Run server
```
python demo.py
```
### Update Client
- Clone the project.
- Update the Server IP and Port of the url in detect.html, history.html, history-detail.html.
- Run the project.
## Reference
- Feng, C., Zhong, Y., Gao, Y., Scott, M. R., & Huang, W. (2021, October). Tood: Task-aligned one-stage object detection. In 2021 IEEE/CVF International Conference on Computer Vision (ICCV) (pp. 3490-3499). IEEE Computer Society.
- Du, D., Qi, Y., Yu, H., Yang, Y., Duan, K., Li, G., ... & Tian, Q. (2018). The unmanned aerial vehicle benchmark: Object detection and tracking. In Proceedings of the European conference on computer vision (ECCV) (pp. 370-386).
- MMDetection of OpenMMLab: https://github.com/open-mmlab/mmdetection
