# Ops Challenge - Event Logging Tool Part 3 of 3 

## Demo Code

The demo code below introduces concepts necessary to complete the challenge.

In this example, we will email ERROR types but not WARNING types.

```python

'''
class-28 demo.py

Log handlers help us record events to output devices like log files, sockets, and notification mechanisms.

This demo script shows two of the three logging handlers in practice, StreamHandler and FileHandler. Refer to https://docs.python.org/3/library/logging.handlers.html for more information.

The StreamHandler class sends logging output to streams such as sys.stdout, sys.stderr or any file-like object.

The FileHandler class sends logging output to a disk file. It inherits the output functionality from StreamHandler.
'''
import logging, time, os

# Create a custom logger
logger = logging.getLogger(__name__)
'''
NOTE: Use __name__ to generically reference the name of the python file that called logging.getlogger. This way if you change the file name, you don't have to update this.

Create handlers.
'''
print("Welcome! This demo script will illustrate the workflow for creating handlers. Let's begin.")
time.sleep(2)

print("Creating handlers...")
c_handler = logging.StreamHandler()
f_handler = logging.FileHandler('file.log') # This file will appear in the same directory as this script.
c_handler.setLevel(logging.WARNING)
f_handler.setLevel(logging.ERROR)
time.sleep(2)
'''
Next, we will create formatters and add it to handlers. 
For warnings we want name, level, and message. 
For errors we want to record time, name, level, and message to a log file.
'''
print("Creating formatters and adding them to handlers respectively...")
c_format = logging.Formatter('%(name)s - %(levelname)s - %(message)s')
f_format = logging.Formatter('%(asctime)s - %(name)s - %(levelname)s - %(message)s')
c_handler.setFormatter(c_format)
f_handler.setFormatter(f_format)
time.sleep(2)

# Add handlers to the logger
print("Adding handlers to the logger...")
logger.addHandler(c_handler)
logger.addHandler(f_handler)
time.sleep(2)

# These should print to the screen. However, because errors are sent into the file handler, they'll also get appended into the log file.
print("Generating one warning log and one error log...")
logger.warning('This is a warning')
logger.error('This is an error')
time.sleep(2)

print("Program complete. View 'file.log' to see errors.")
os.system("ls -al")

# Incorporate Streamhandler and Filehandler into your own Python script. Good luck!

```


"DEMO.md" 45L, 1015C                                                                                                                                                 1,1           Top


