MedManip 离线补充材料网页

1. 使用方法
   解压 ZIP。把你的视频放进 media 文件夹，然后双击 index.html。
   index.html 和 media 必须保持在同一层。页面可以在断网时打开。
   模板自带视频位置和文件名提示。把 MP4 放到对应位置后重新打开页面。

2. 默认视频位置
   Reconstruction Results         数据恢复效果
     media/reconstruction-oral-scanner.mp4
     media/reconstruction-medicine-box.mp4

   Reconstruction Comparisons     数据恢复对比
     media/comparison-oral-scanner-grail.mp4
     media/comparison-oral-scanner-medmanip.mp4

   Simulation Results             仿真实验
     media/simulation-oral-scanner.mp4
     media/simulation-medicine-box.mp4

3. 更换名字或添加案例
   用文本编辑器打开 index.html，搜索 PROJECT_MEDIA。
   label 是页面显示的对象名或方法名，detail 是可选的小标签，
   file 是相对 index.html 的文件路径。可加 poster 指定本地视频封面。

   三个列表对应 reconstructions、comparisons 和 simulations。
   添加普通视频时，从同一列表复制一条记录，修改 label 和 file。
   添加对比案例时，复制一个包含 label 和 methods 的完整区块。
   添加新基线时，在同一案例的 methods 内复制一条方法记录。

   例：
     { label: "Syringe", detail: "4D reconstruction",
       file: "media/reconstruction-syringe.mp4",
       poster: "media/reconstruction-syringe.jpg" }

4. 准备对比视频
   导出 MP4，推荐 H.264 视频编码和 yuv420p 像素格式。
   同组视频建议用同一视角、帧率和动作起点。网页的对比控件按秒对齐，
   共同时间轴到最短视频的结尾。如果需要逐帧严格对齐，先在剪辑软件中
   对齐每一帧并导出一条同屏 MP4，再把它作为一个普通播放器条目加入页面。

5. 打包前检查
   解压自己最终打包的 ZIP 再检查一次。断网打开 index.html，播放各段视频，
   确认对比区的暂停、拖动进度和重新开始正常。建议随包保留原始 MP4，
   便于直接播放。需要匿名时，也检查文件名、视频画面及媒体元数据。
   投稿时，以 OpenReview 对补充材料上传格式和大小的要求为准。
