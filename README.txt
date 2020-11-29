This is a bash script to generate random nested directory files and was orginally written by nrgwsth.  This script uses the dd command to generate files which means it's a bit slow depending on your inputs

Usage: "./filegen.sh foldername 2,3,4 small"

The foldername variable is the destination directory

The three comma separated numbers represent the complexity of what is being generated: 
    1st number is how many top level directories you want
    2nd number is how many directories under each top level directory you want
    3rd number is how many files in the second directory tier you want

The last value is how big you want the files to be (approximately):
    small (example size for small listed below)
    medium
    large


For example, if you run this: "filegen.sh ./fakefilesandfolders 2,3,4 small" then script will create directories and folders like this:

tree
.
├── dir_1
│   ├── dir_1
│   │   ├── file_1
│   │   ├── file_2
│   │   ├── file_3
│   │   └── file_4
│   ├── dir_2
│   │   ├── file_1
│   │   ├── file_2
│   │   ├── file_3
│   │   └── file_4
│   └── dir_3
│       ├── file_1
│       ├── file_2
│       ├── file_3
│       └── file_4
└── dir_2
    ├── dir_1
    │   ├── file_1
    │   ├── file_2
    │   ├── file_3
    │   └── file_4
    ├── dir_2
    │   ├── file_1
    │   ├── file_2
    │   ├── file_3
    │   └── file_4
    └── dir_3
        ├── file_1
        ├── file_2
        ├── file_3
        └── file_4


The above script created 8 directories, 24 files, and it's total size is 83.755472 GB

Also, here's some file size info from one of the second level dirs:
  axisfour@ubuntu:~/Documents/filetest/dir_1/dir_1$ ls -l --block-size=G
  total 14G
  -rw-rw-r-- 1 axisfour axisfour 4G Nov 25 13:49 file_1
  -rw-rw-r-- 1 axisfour axisfour 5G Nov 25 13:51 file_2
  -rw-rw-r-- 1 axisfour axisfour 1G Nov 25 13:51 file_3
  -rw-rw-r-- 1 axisfour axisfour 5G Nov 25 13:53 file_4


