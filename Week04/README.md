# 2D_Digital_Compositing
## Week 03 Assignment
### What is colorspace?
- Colorspace
<pre>
<code>
- 색 표시계(color system)를 3차원으로 표현한 공간 개념이다. 
- 색 표시계의 모든 색들은 이 색 공간에서 3차원 좌표로 나타낸다.
- 색상(hue), 명도(lightness), 채도(chroma)를 3차원 공간의 각각의 기본 축으로 하는 공간
</code>
</pre>

- 색공간의 이해
<pre>
<code>
- 색의 3속성 색상, 명도, 채도를 3차원 공간의 각각의 축으로 형성
- 자주 쓰이는 색 공간 : RGB색공간, CMYK색공간, HSV색공간, CIE색공간
</code>
</pre>

- RGB색공간

![Alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week04/images/200px-RGBCube_b.svg.png)


- CMYK색공간

![Alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week04/images/%EB%8B%A4%EC%9A%B4%EB%A1%9C%EB%93%9C.jpg)


- HSV색공간

![Alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week04/images/200px-HSV_cone.jpg)


- CIE xyz 색공간 : XYZ 색 공간은 RGB 색 공간으로부터 선형변환을 통해 얻을 수 있으며, 모든 값이 양수를 갖는다.

![Alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week04/images/CIE-1931-color-space.jpg)


- CIE lab 색공간 : Lab 색 공간은 인간 시각의 길항 이론에 의거하여, CIE XYZ 색 공간을 비선형 변환하여 만들어진 색 공간

![Alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week04/images/CIE-LAB-1976-color-space.png)


- CIE luv 색공간 : CIE가 1976년에 정한 균등 색공간의 하나로서 다음의 3차원 직교 좌표를 이용하는 색공간

![Alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week04/images/CIELUV.png)

균등 색공간 : 동일한 크기로 지각되는 색차가 공간 내의 동일한 거리와 대응하도록 의도한 색공간

선형 변환 : 자료의 분포 모양을 그대로 유지하면서 점수 혹은 측정치를 일정 규칙에 따라 다른 점수 혹은 척도로 바꾸는 것


-------------
### Gamma / Linear workflow

------------
### What is LUT? Color LookUpTable?

---------------
### What is Logspace and what is main difference wiht sRGB, why and when we use?
