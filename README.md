# This is a bash script to generate random nested directory files.
# !filegen
# filegen by nrgwsth 
# FYI, script uses dd command to generate files which means it's a bit slow depending on your inputs
#



Usage:  "./filegen.sh foldername 2,3,3 small"

   The foldername variable is the destination directory

   The three comma separated numbers represent the complexity of what is being generated: 
        1st number is how many top level directories you want 
        2nd number is how many directories under each top level directory you want
        3rd number is how many files in the second directory tier you want
        
   The last value is how big you want the files to be (approximately)
        small
        medium
        large
     

For example, if you run this:  "filegen.sh ./fakefilesandfolders 2,3,4 small"  then script will create directories and folders 



 
