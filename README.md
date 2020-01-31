Very Deep Convolutional Networks For Large-Scale Image Recognition
============================================================================
논문 링크 : <https://arxiv.org/pdf/1409.1556.pdf>   
   
   
   
논문요약
--------
>1. ILSVRC 2014 대회에서 2등을 차지한, Karen Simonyan과 Andrew Zisserman이 만든 CNN 모델
>2. VGGnet, GoogleNet 이전의 depth는 8layers 수준에서 머물렀다면 GoogleNet, VGGnet 이후 크게 깊어졌다.
>3. 
>4. 최근에는 이미지 특징(feature)을 추출하는 데 이용되는 등 기본 네트워크 모델로 활용되고 있음.
>5. 매우 많은 파라미터를 이용하여 연산한다는 단점이 있음.

receptive field
---------------
5x5 Convolution Filter 가 아니라 3x3
VGGNet의 특징은 작은 컨볼루션 필터(3x3, 1 strides)로 깊은 레이어(16-19 weight layers)를 만들어 좋은 성능을 낸다.

실험내용
--------
   
