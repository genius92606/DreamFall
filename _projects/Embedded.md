---
title : Robotic arm & Image processing
permalink: projects/Robictic-arm-and-image-processing-in-embedded-system
header:
  image: /assets/projects/embedded.jpg
  teaser: /assets/projects/embedded.jpg


---

Our goal is to track a ball.
We install a camera on a robotic arm.
The camera was connected to the laptop so MATLAB can do image processing, then communicate to Arduino through bluetooth.
Once the Arduino get the information, it will move the robotic arm, and keep tracking the ball.  

<iframe src="https://docs.google.com/viewer?srcid=1q6uEkvvlZpvp1dqxDUB5Zn_Hqjh3qUGX&pid=explorer&efh=false&a=v&chrome=false&embedded=true" style="width:100%; height:500px;" frameborder="0" allowfullscreen></iframe>


<iframe width="640" height="360" src="https://www.youtube-nocookie.com/embed/mlY6fdEGLOI?controls=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>


這次我們三個一起合作製做一基於機械手臂的影像追蹤系統，目標是要將鏡頭放置在手臂上，追蹤想要追蹤的物體，物體動到哪裡，攝影機就追到哪裡。透過影像處理找到明確的目標，進而傳輸指令給機械手臂，使其自動化的到達物體位置。為了到達目的，我們購買Tinkerkit Braccio，由Arduino原廠出品的機械手臂，其優點是可以完全相容Arduino控制板，而Arduino控制板也是一很好取得且方便使用的控制板，再來我們也購買了Kinyo webcam當作我們的攝影機，最後使用藍芽模組作為影像處理以及機械手臂之間溝通的橋樑。我們的做法如下: 首先，先取得攝影機鏡頭影像，選定乒乓球色塊轉換成binary畫面，接下來濾除小雜點後進行填補形成圓形，利用取平均的方法找出圓球中心點。找到球的中心點後，計算其與整體影像中心點的相對位置，推算相機需動的方向及距離，整理成一個變數後，透過藍芽將該變數傳輸給Arduino進行馬達動作。最終希望可以將此技術應用在內視鏡手術當中，我們將透過微攝影機進入內視鏡管，追將手術器械，醫生將不用多空一隻手來操控攝影機，有些需多人進行的手術，就不用那麼多人了，那將會大大的簡少人事成本!