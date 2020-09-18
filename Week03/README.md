# 2D_Digital_Compositing
## Week 02 Assignment
### What is digital compositing?
+ 사전적 정의

    > Digital compositing is the process of digitally assembling multiple images to make a final image,
  typically for print, motion pictures or screen display. It is the digital analogue of optical film compositing. [Wikipedia](https://en.wikipedia.org/wiki/Digital_compositing)

    > 연속된 이미지나 합성 이미지를 만들기 위해 적어도 2개 이상의 소스 이미지들을 디지털로 합성하는 것. [Naver](https://terms.naver.com/entry.nhn?docId=1649302&cid=50372&categoryId=50372)

+ Digital Compositing
<pre>
<code>
- VFX Pipeline(post production)의 마무리 단계
- 여러가지 소스(영상, 이미지, 3D asset..)를 하나의 영상 또는 이미지로 통합하는 과정
</code>
</pre>

![alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week03/the-vfx-pipeline.jpg)
+ Chroma Key
<pre>
<code>
- 두개의 영상을 합성하는 기술로 두개의 영상 중 상위 레이어의 특정한 색깔을 제거한다.
- 제거하고 싶은 색깔과 보여주고 싶은 오브젝트의 색깔이 겹치면 오류가 발생한다.
- 초록과 파랑이 자주 쓰인다.(=사람의 피부와 가장 구별되는 색깔)
Ex.) Green screen(most common), Blue screen, magic pink
</code>
</pre>

+ Rotoscoping
<pre>
<code>
- 상위레이어에 있는 개체 위로 마스크를 움직여 배경과 분리하는 과정
Ex.) Masking, Roto brush, Tracking, Planal tracking
</code>
</pre>

+ Matte painting
<pre>
<code>
- 디지털이나 아날로그 회화기법으로 새로운 이미지를 제작하는 기법
- 카메라로 촬영하기 힘든 장소를 재현하는데 주로 쓰임
- 디지털 기술 이후로 3D카메라로 2.5차원의 평면을 입체적으로 움직이며 복잡한 작업이 가능해짐
</code>
</pre>

+ Digital compositing을 위한 개인 역량과 지식
<pre>
<code>
- 색에 대한 이해도
- 카메라와 렌즈에 대한 지식
- 빛(조명)에 대한 지식
</code>
</pre>

+ Digital compositing tools
<pre>
<code>
- Paint Programs
- Color Correction utilities
- Warping/Morphing Tools
- Matte-Extraction software
- General-purpose compositing packages
Ex.) : NUKE, AE, Photoshop...
</code>
</pre>
[참조링크](http://mlab.taik.fi/touch/DCN/DGbackup.html)

---------------------
### What is the Alpha?

+ Alpha channel
<pre>
<code>
- RGBA(RGB채널에 투명도가 추가됨)에서 A=투명도를 나타냄
- straight alpha (unassociated alpha; unmatted RGB + alpha) : 
   알파값만이 투명도를 나타내고, RGB는 투명도와 관계없이 빨강, 초록, 파랑의 강도만 표현
- premultiplied alpha (associated alpha; matted RGB + alpha) : 
   RGB에 불투명도를 미리 곱해둔 값; 알파값없이 RGB만으로도 투명도가 적용된 색상을 얻을 수 있음
</code>
</pre>

