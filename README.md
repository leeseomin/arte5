# arte5

<img src="https://github.com/leeseomin/arte5/blob/main/out/grainout.png" width="2000">


### Dependency install on ubuntu 16.04  + torch + nvidia Pascal gpus (ex. gtx1080ti, gtx1080, gtx1070, gtx1070ti)


```
 # torch install

http://torch.ch/docs/getting-started.html


 # parallel install
 
 sudo apt install parallel
 
 
   #  gimp gmic install

sudo add-apt-repository ppa:otto-kesselgulasch/gimp-edge

sudo apt-get update

sudo apt-get install gmic gimp-gmic


 #   imagemagick install

sudo apt install graphicsmagick-imagemagick-compat

sudo apt install imagemagick-6.q16


 #  Gmic update filters (follow the link)
 
https://telegra.ph/Gmic-update-filters-07-26

```



### Install

```

git clone https://github.com/leeseomin/arte5

cd arte5

mkdir s{1..25}


```

### Usage
```

input images folder : s ,   result folder : s25


bash main.sh

```




###  Results

### input image1

 <img src="https://github.com/leeseomin/arte5/blob/main/s/grain.png" width="700">

### output (image1)
 
  <img src="https://github.com/leeseomin/arte5/blob/main/out/grainout.png" width="2000">



### input image2

 <img src="https://github.com/leeseomin/arte5/blob/main/s/monet.png" width="700">

### output (image2)
 
  <img src="https://github.com/leeseomin/arte5/blob/main/out/monetout.png" width="2000">




### input image3

 <img src="https://github.com/leeseomin/arte5/blob/main/s/2855.png" width="700">

### output (image3)
 

  <img src="https://github.com/leeseomin/arte5/blob/main/out/2855out.png" width="2000">




### input image5

 <img src="https://github.com/leeseomin/arte5/blob/main/s/11.png" width="700">

### output (image5)
 
  <img src="https://github.com/leeseomin/arte5/blob/main/out/11out.png" width="2000">


```  
  
### make smooth video
```
ffmpeg -framerate 1 -pattern_type glob -i '*.png' \
  -c:v libx264 out.mp4
  
ffmpeg \
  -i out.mp4 \
  -crf 10 \
  -vf "minterpolate=fps=60:mi_mode=mci:mc_mode=aobmc:me_mode=bidir:vsbmc=1" \
  smooth_60fps.mp4  
  
ffmpeg -i out.mp4 -plays 0  apngout.apng
  
```    

### License

The code is based on Dmitry Ulyanov's texture_nets.

This repo is made freely available to academic and non-academic entities for non-commercial purposes 
such as academic research, teaching, scientific publications. 
Permission is granted to use the arte5 given that you agree to my license terms. Regarding the request for commercial use, 
please contact me via email (leeseomin@gmail.com)




###  Author

LEE SEOMIN


