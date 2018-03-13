tensorflow object detection api tutorial
==============
# 1 model_builder
from object_detection.builders import model_builder<br>
通过model_builder.build 函数 制定meta_architecture：ssd frcnn fcn等。<br>
detection 框架首先建立feature extractor architecture。提取特征的网络。确定哪几层作为featuremap输出<br>
box_coder_builder:box前面的系数，作为归一化的系数
anchor_generpredictor: 使用派生的子类根据不同特征图以及最大最小尺度范围确定每个特征图的box的包含范围。<br>
box_predictor:使用派生的子类生成预测框，包含参数确定是否加入卷积层等参数。<br>
post_processing_builder:iou以及每类最多预测数。<br>
losses_builder：loss计算反传。hardmining<br>
# 2 trainer.train

