## 主要依赖的及版本
tensorflow==2.0

jieba

scikit-learn

## 数据处理
1.删除了含有0的各行数据

2.利用jieba分词进行简单的切分
## TFIDF + 逻辑回归

| CV_num | 年龄| 性别| 教育|
|------ | ------ | ------ | ------ |
|1|0.61325499|0.84417199|0.63907565| 
|2|0.61721001|0.84761851|0.63766314| 
|3|0.61973104|0.84077297|0.63803820| 
|4|0.61481523|0.84421969|0.63413945| 
|5|0.61046446|0.84314612|0.63803820| 
|avg|0.61509515|0.84398585|0.63739093| 

## TFIDF + LGBM

LGBM训练时间较长，我在colab上训练的预计训练时间在12小时以上

| CV_num | 年龄| 性别| 教育|
|------ | ------ | ------ | ------ |
|1|0.60969546|0.83688344|0.63173061| 
|2|0.61291598|0.83784395|0.62941409| 
|3|0.61577579|0.83698723|0.63278337| 
|4|0.61102949|0.83710024|0.63238784| 
|5|0.60939089|0.83337100|0.62758504| 
|avg|0.61176153|0.83643717|0.63078019| 

## LDA + 逻辑回归（LGBM）
LDA的主题个数选择是 6 x 6 x 2 = 72，效果很差

LGBM结果（逻辑回归结果差不多就不往上贴了）

| CV_num | 年龄| 性别| 教育|
|------ | ------ | ------ | ------ |
|1|0.46607200|0.65789000|0.48861500|
|2|0.47160900|0.66060200|0.48415200|
|3|0.46971400|0.65239000|0.48338800|
|4|0.46920600|0.65866200|0.48231400|
|5|0.47242600|0.65510200|0.48056300|
|avg|0.46980540|0.65692920|0.48380640|
