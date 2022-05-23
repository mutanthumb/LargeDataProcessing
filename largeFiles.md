Most of these commands are from a Linux terminal unless otherwise noted.

Tarring each folder within current folder:

    find . -maxdepth 1 -mindepth 1 -type d -exec tar cvf {}.tar {}  \;

This can take days to complete to have it run in the background and create a "log" of what is in each tar file, the nohup.out file that is created will be a plain text searchable log:

    nohup find . -maxdepth 1 -mindepth 1 -type d -exec tar cvf {}.tar {}  \;&

To see if the nohup.out is still being written to:

    tail -f nohup.out

To check if the nohup process is still running:

    ps -ef |grep nohup 

Get checksum for file or folder (on Mac) this is helpful when you're creating your own zip or tar files and you want to be sure they are still intact after transfer to new location:

    md5 /path/to/file

On Linux:

    md5sum /path/to/file

Zip on Mac without hidden files:

    zip -r -X archive_name.zip folder_to_compress

Count # of directories in current folder:
 
    find . -mindepth 1 -maxdepth 1 -type d | wc -l

Count # of files in current folder:

    find . -mindepth 1 -maxdepth 1 -type f | wc -l
