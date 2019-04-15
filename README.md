# generateCarPlate
```
生成车牌识别/OCR识别训练数据
generate Car Plate dataset for PR/OCR training
国内蓝色普通车牌生成，忘了参考过哪里的代码，其他类型牌照参考一下按需自己随意
```

## Todo：
```
1.增加全类型(新能源 特殊车辆等)
2.背景更真实
3.还没想好，可能顺便重构一下
```
## 想法：
```
1.把生成的字符串写到蓝色车牌模版照片上，生成车牌；
2.把车牌照片放到背景照片上；
3.增加旋转、噪声，参见 def generate（）
```

## 用法：
```
python genCarPlate.py
```

### param：
```
--根据自己的训练要求 照片大小即背景照片(Background/)设置为了256*128，按需自己随意
--为了使得车牌占比约为80% 设置车牌大小为(220, 70)，按需自己随意
--每个省份生成照片数量设置IMG_COUNT_PER_PROVINCE = 随意
--为了使得每个省份中每个城市的车牌数量均衡，即车牌汉字后的第一个字母在24个字母中分布平均，
   参见 genplate.py：38行
   i = iter // IMG_COUNT_PER_PROVINCE
   iterChar = (iter % IMG_COUNT_PER_PROVINCE) // 9
```
