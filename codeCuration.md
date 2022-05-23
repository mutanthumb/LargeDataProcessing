1. Open code in text editor if Python or in MATLAB if it's a .m file
- I would highly recommend using this so you don't hose up your regular Python environment: Python virtual environments: https://docs.python.org/3/tutorial/venv.html
3. Scan through code looking for relative or absolute file paths
    1. Verify that the files you were provided match those paths
    2. Can you with little effort make the data match these paths?
    - Yes. Proceed
    - No. Check in with researcher to see if you're missing files or folders.
4. Once everything is where the code expects it to be, try running the code.
    1. Does it complete?
    - Yes. YAY nice work. Check the related documentation to see if it can be improved.
    - No. Poop. Check for obvious errors:
        - Are you missing a required library or module?
        - Are you using the same version of Python, MATLAB etc.?
        - Are all of your files/folders in the appropriate PATH? This a common issue with MATLAB.
        - Do a web search on the error you're receiving, if it's easy to resolve take a crack at it and inform the researcher that you received an error and what it was. In my experience errors are not always "news" to researchers and they generally know the cause. 
    2. After troubleshooting does it complete?
    - Yes. YAY nice work. Check the related documentation to see if it can be improved. 
    - No. Poop. Inform the researcher that you received an error and what it was. In my experience errors are not always "news" to researchers and they generally know the cause. 

4. Make suggestions for improving the README.txt file based on your experience trying to run the code.

**Code should be written such that it does NOT rely on the home researcher's machine to run it should be as universal as possible think relative paths to files rather than absolute paths.**

