# 基于yolov5的甲骨文图形化检测工具



**界面**

![界面](https://github.com/LuckyBoy1798/yolov5-pyqt/blob/main/imgs/界面.png)

**本地图片检测画面：**

![本地图片](https://github.com/LuckyBoy1798/yolov5-pyqt/blob/main/imgs/图片.png)

**本地视频检测画面：**

![本地视频](https://github.com/LuckyBoy1798/yolov5-pyqt/blob/main/imgs/视频.png)



**功能：**

1. 模型选择
2. 输入选择(本地文件、摄像头、RTSP)；在检测RTSP视频流的时候，尽量不要启用帧间延时，否则会出现很高的延时，用yolo5x模型时，rtsp会很卡，建议抽帧检测, 把main.py中的133-135行注释取消
```python
                    # jump_count += 1
                    # if jump_count % 5 != 0:
                    #     continue
```

3. IoU调整
4. 置信度调整
5. 帧间延时调整
6. 播放/暂停/结束
7. 统计检测结果（显示边框时，支持中文标签）


**使用：**
```bash
# conda创建python虚拟环境
conda create -n yolov5_pyqt5 python=3.8
# 激活环境
conda activate yolov5_pyqt5
# 到项目根目录下
cd ./
# 安装依赖文件
pip install -r requirements.txt
# 将下载好的模型放在pt文件夹下
# 运行main.py
python main.py
```
运行*main.py*开启检测界面后**会自动检测已有模型**。ui文件已上传，可以按照自己的想法更改ui界面。

**注：由于官方给出的yolov5版本会持续更新。为了避免不兼容的问题，建议使用本仓库的yolov5。如果想兼容最新版本的yolov5，自行更改对应的代码即可。**

本仓库的yolov5版本为**v5.0**，是直接从官方仓库拉取的，支持训练。

本仓库依赖模型有yolov5s.pt、yolov5m.pt、yolov5l.pt、yolov5x.pt,下载地址：https://github.com/ultralytics/yolov5/releases/tag/v5.0
点击地址后翻到最下面有下载链接，将下载好的模型放在pt文件夹下，运行界面时，**会自动检测已有模型**，也可以放入**自己训练的模型文件**。
