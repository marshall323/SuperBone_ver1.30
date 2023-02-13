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
      │       └── pattern_feature        
```

# Image Feature and Mechnical Feature
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
├── mechnical features
      ├── Max stress
      └── Strain at max stress            
```

# Update Log

# How to Use SuperBone_MECH

1) 執行模擬之圖片檔可放置於 img_src 的 mechanical_src 中，可依據需求存放多個 mechanical_src 資料夾，如 mechanical_src_1、mechanical_src_2 等...
   以便在同個資料夾同時進行多個核心運算

2) 目前執行 SuperBone_MECH.bat 會出現以下兩行指令

   ```bash
   Please choose a unit (si or real)
   Please choose a simulation (LJ or LSM)
   ```
   第一行為模擬時使用之單位，可參考LAMMPS的官方文件，目前為si
   第二行為模擬之模型，目前為LSM

   自行輸入si、LSM 即可 (可不區分大小寫)

3) 接著會跳出視窗要求點選圖片來源資料夾，即 img_src 的 mechanical_src

4) 點擊繼續，模擬即開始進行
