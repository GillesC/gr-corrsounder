
# gr-corrsounder

![gr-corrsounder signal flow](gr-corrsounder-signalflow.png)

![gr-corrsounder architecture](gr-corrsounder-architecture.png)

# Requirements

 * GNU Radio
 * python package psutil
 * python package scipy

# Build/Install instructions

0. Recommended installing an old version of Ubuntu (18.04) to support the legacy code of the corrsounder.

1. Install/Build GNU Radio (it is recommended to use [PyBOMBS](https://github.com/gnuradio/pybombs))

```sh
sudo apt-get install python3-pip
sudo pip3 install pybombs
pybombs auto-config
pybombs recipes add gr-recipes git+https://github.com/gnuradio/gr-recipes.git
pybombs recipes add gr-etcetera git+https://github.com/gnuradio/gr-etcetera.git
pybombs config --package gnuradio gitrev v3.7.11
pybombs prefix init ~/prefix-3.7 -R gnuradio-default
source ~/prefix-3.7/setup_env.sh
```

2. Get *gr-corrsounder* from github - `git clone https://github.com/inIT-HF/gr-corrsounder.git`

3. Optional: Change to which prefix *gr-corrsounder* shall be installed - `source ~/corrsounder_prefix/setup_env.sh`

4. Configure *gr-corrsounder* - `mkdir build && cd build && cmake ../`

5. Build and install *gr-corrsounder* - `make && sudo make install` 

# Uninstall/Remove instructions

1. Navigate to gr-corrsounder/build

2. Optional: Change from which prefix *gr-corrsounder* shall be uninstalled - `source ~/corrsounder_prefix/setup_env.sh`

3. Uninstall *gr-corrsounder* - `sudo make uninstall`

4. Delete the gr-corrsounder folder

# Contributors

 * Niels Fliedner
 * Dimitri Block

# References
1. Niels Hendrik Fliedner, Dimitri Block, Uwe Meier “A Software-Defined Channel Sounder for Industrial Environments with Fast Time Variance”. Submitted to the 15th International Symposium on Wireless Communication Systems (ISWCS 2018). [Arxiv preprint](https://arxiv.org/abs/1805.01236)
