Most of these commands are from a Linux terminal unless otherwise noted.

Tarring each folder within current folder:

    find . -maxdepth 1 -mindepth 1 -type d -exec tar cvf {}.tar {}  \;

This can take days to complete to have it run in the background and create a "log" of what is in each tar file, the nohup.out file that is created will be a plain text searchable log:

    nohup find . -maxdepth 1 -mindepth 1 -type d -exec tar cvf {}.tar {}  \;&

To see if the nohup.out is still being written to:

    tail -f nohup.out

To check if the nohup process is still running:

    ps -ef |grep nohup 
    
Test ZIP file:

    unzip -t example.zip
    
Let list of files in ZIP without unzipping file:

    unzip -l example.zip

Get checksum for file or folder (on Mac) this is helpful when you're creating your own zip or tar files and you want to be sure they are still intact after transfer to new location:

    md5 /path/to/file

On Linux:

    md5sum /path/to/file
    
Get SHA1 checksum:

    sha1sum somefile.txt

Zip on Mac without hidden files:

    zip -r -X archive_name.zip folder_to_compress

Count # of directories in current folder:
 
    find . -mindepth 1 -maxdepth 1 -type d | wc -l

Count # of files in current folder:

    find . -mindepth 1 -maxdepth 1 -type f | wc -l
    
Checking for storage usage:

    df -h —> to get space available in both Gig and TB
    du -ch fedora-testing/ | grep total
    ls -sh —> human readable file sizes
    
Renaming files and subdirectories recursively (from https://stackoverflow.com/questions/15012631/rename-files-and-directories-recursively-under-ubuntu-bash):
    
    find . -depth -execdir rename 's/old/new/g' '{}' \+ 
    
Splitting 10000 files into 10 new folders of 1000 files each (from https://fedingo.com/how-to-split-folder-into-subfolders-in-linux/):

    i=0; 
    for f in *; 
    do 
        d=dir_$(printf %03d $((i/1000+1))); 
        mkdir -p $d; 
        mv "$f" $d; 
        let i++; 
    done
    
Removing ".DS_STORE" files:

    find . -name '.DS_Store' -type f -delete [enter]
