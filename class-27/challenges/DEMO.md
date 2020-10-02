# Ops Challenge - Event Logging Tool Part 2 of 3 

## Demo Code

The demo code below introduces concepts necessary to complete the challenge.

```python

import logging
import time
from logging.handlers import RotatingFileHandler
#----------------------------------------------------------------------
def create_rotating_log(path):
    """
    Creates a rotating log
    """
    logger = logging.getLogger("Rotating Log")
    logger.setLevel(logging.INFO)
    
    # add a rotating handler
    handler = RotatingFileHandler(path, maxBytes=20,
                                  backupCount=5)
    logger.addHandler(handler)
    
    for i in range(10):
        logger.info("This is test log line %s" % i)
        time.sleep(1.5)
        
#----------------------------------------------------------------------
if __name__ == "__main__":
    log_file = "test.log"
    create_rotating_log(log_file)

```


"DEMO.md" 45L, 1015C                                                                                                                                                 1,1           Top


