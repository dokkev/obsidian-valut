Issac Sim Install
https://docs.omniverse.nvidia.com/isaacsim/latest/installation/install_workstation.html


Orbit Install
https://isaac-orbit.github.io/orbit/source/setup/installation.html#installing-isaac-sim


Orbit Install Debugging in Building extensions:
1)  Typo in `source/extensions/omni.isaac.orbit_envs/setup.py`
https://github.com/NVIDIA-Omniverse/Orbit/commit/e99c2dec2cb872cef91747dfaf28396af1d3baf3
```
Looking in indexes: https://pypi.tuna.tsinghua.edu.cn/simple, https://pypi.ngc.nvidia.com
Obtaining file:///home/ubuntu/Orbit/source/extensions/omni.isaac.orbit_envs
  Preparing metadata (setup.py) ... error
  error: subprocess-exited-with-error

  × python setup.py egg_info did not run successfully.
  │ exit code: 1
  ╰─> [3 lines of output]
      error in omni-isaac-orbit_envs setup command: 'install_requires' must be a string or list of strings containing valid project/version requirement specifiers; Expected end or semicolon (after version specifier)
          setuptools<=66h5py
                    ~~~~^
      [end of output]

  note: This error originates from a subprocess, and is likely not a problem with pip.
error: metadata-generation-failed

× Encountered error while generating package metadata.
╰─> See above for output.
```


2) Gym Install error with `opencv-python` 
https://github.com/openai/gym/issues/3202#issuecomment-1511268727
```
          opencv-python>=3.
                       ~~~^
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
  ERROR: Failed building wheel for gym
  Running setup.py clean for gym
Failed to build gym
ERROR: Could not build wheels for gym, which is required to install pyproject.toml-based projects

```
