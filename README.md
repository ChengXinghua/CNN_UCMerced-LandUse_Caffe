# CNN_UCMerced-LandUse_Caffe
主要任务：基于深度学习框架完成对光学遥感图像UCMerced LandUse数据集的分类。 
数据特点：共包含21类土地类型图片，每类100张，每张像素大小为256*256，数据类内距离大，类间小。 
完成情况：数据量太小，训练数据出现过拟合；为了克服这个问题，又减小训练时间，采用caffe框架，在别人训练好的bvlc_reference_caffenwt模型上进行fine-tune，对最后一层设置较大的学习速率，结果取得了93%的正确率；在这基础上又在fc7层上提取了每张图片的4096维特征，进行了SVM分类，取得了95%以上的分类正确率，并对结果做了可视化分析。
