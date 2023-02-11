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
      │              └── ......other directory you need
      │       ├── lammps_needfile        
      │       ├── SuperBone_main
      │              ├── DCMsearch
      │              ├── DCMtoIMG
      │              ├── IMGtoFeature
      │              ├── IMGtoParticle
      │              ├── LAMMPStoDATA
      │              └── ......other .py file
      │       ├── test
      │       ├── test_tool
      │       ├── feature_output.csv
      │       ├── mechanic_output.csv
      │       ├── search_output.csv
      │       └── ......other .bat and .sh file to execute program  
      └── dcm_output
      │       ├── mechanical_feature
      │       └── pattern_feature        
```
# Update Log
