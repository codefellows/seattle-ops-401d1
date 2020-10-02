# Ops Challenge - File Encryption Script Part 1 of 3

## Demo Code

The demo code below introduces concepts necessary to complete the challenge.

### Print environment variables readably

```python

import os
 
for k, v in os.environ.items():
    print(f'{k}={v}')

```
 
### Fetch a specific environment variable's value.

```python

import os
 
home_dir =os.environ['HOME']
username = os.environ['USER']
print(f'{username} home directory is {home_dir}')

```

### Set an environment variable in Python.

```python

import os
 
env_var = input('Please enter environment variable name:\n')
 
env_var_value = input('Please enter environment variable value:\n')
 
os.environ[env_var] = env_var_value
 
print(f'{env_var}={os.environ[env_var]} environment variable has been set.')

```
"DEMO.md" 45L, 1015C                                                                                                                                                 1,1           Top


