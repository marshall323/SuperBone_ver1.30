# SuperBone_ver1.30
A tool for converting DICOM files (especially for bones) to threshold images, as well as performing image geometry and mechanical analysis.

# Recommand File Hierarchy
```
├── your driver or directory
      ├── dcm_zip
      ├── dcm_src
      ├── img_src_all
      ├── SuperBone_ver1.30
      │       ├── analyze_figure
      │       ├── img_src
      │              ├── mechanical_src
      │              ├── pattern_src
      │              └── ......other directories you need
      │       ├── lammps_needfile        
      │       ├── SuperBone_main
      │              ├── DCMsearch
      │              ├── DCMtoIMG
      │              ├── IMGtoFeature
      │              ├── IMGtoParticle
      │              ├── LAMMPStoDATA
      │              └── ......other .py file
      │       ├── test
      │       ├── test_tool (分析小工具，陸續更新)
      │       ├── feature_output.csv
      │       ├── mechanic_output.csv
      │       ├── search_output.csv
      │       └── ......other .bat and .sh files to execute program  
      └── dcm_output
      │       ├── mechanical_feature
      │       ├── mechanical_dump
      │       ├── mechanical_txt
      │       └── pattern_feature        
```

# Image Feature and Mechanical Feature
```
├── All image features have their corresponding average and standard deviation.
      ├── Porosity
      ├── Bone Angle
      ├── Thinkness
      ├── Curl
      ├── Area
      ├── Convex Area  
      ├── Ratio of Area to Perimeter
      ├── Compactness
      ├── Circularity 
      ├── Width to Length
      ├── Centroid_X
      └── Centroid_Y             
```
```
├── mechanical features
      ├── Max stress
      └── Strain at max stress            
```

# Update Log

2023-02-15) Update file hierarchy which can differentiate the file types. And rewrite the code for more mechanical purposes.
2023-02-20) Add tool 'random_file_chooser.py' for a better way to move images from img_src_all to img_src.

# How to Use SuperBone_TOOL

1) 開啟 SuperBone_TOOL.bat，可選擇使用那些工具，目前需選擇 'random_file_chooser.py' 將所需圖片檔放入 img_src，以便分析

2) 目前執行 SuperBone_TOOL.bat 會出現以下兩行指令

   ```bash
   Please choose a unit (si or real)
   Please choose a simulation (LJ or LSM)
   ```
   第一行總共需要分析的圖片數量，目前為一萬張
   
   第二行為將總圖片數放入之資料夾數目，可依據需求輸入數量
   
# How to Use SuperBone_FEAT

1) 執行模擬之圖片檔可放置於 img_src 的 feature_src 中，可依據需求存放多個 feature_src 資料夾，如 feature_src_1、feature_src_2 等...
   以便在同個資料夾同時進行多個核心運算 

2) 接著會跳出視窗要求點選圖片來源資料夾，即 img_src 的 feature_src_1、feature_src_2...

3) 點擊繼續，分析即開始進行

# How to Use SuperBone_MECH

1) 執行模擬之圖片檔可放置於 img_src 的 mechanical_src 中，可依據需求存放多個 mechanical_src 資料夾，如 mechanical_src_1、mechanical_src_2 等...
   以便在同個資料夾同時進行多個核心運算

2) 目前執行 SuperBone_MECH.bat 會出現以下兩行指令

   ```bash
   Please choose a unit (si or real)
   Please choose a simulation (LJ or LSM)
   ```
   第一行為模擬時使用之單位，可參考 LAMMPS 的官方文件，目前為 si
   
   第二行為模擬之模型，目前為LSM

   自行輸入si、LSM 即可 (可不區分大小寫)

3) 接著會跳出視窗要求點選圖片來源資料夾，即 img_src 的 mechanical_src_1, mechanical_src_2...

4) 點擊繼續，模擬即開始進行
