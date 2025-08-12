# VisdeurBot

VisdeurBot is an AI model created to help identify fish travelling through the Weerdsluis canal of Utrecht, created using the [jetson-inference](https://github.com/dusty-nv/jetson-inference) packages for the Nvidia Jetson Orin Nano SoM.

Learn more about the Fish Doorbell project [here](https://visdeurbel.nl) ([English link](https://visdeurbel.nl/en)).

See the AI in action [here](https://xistnt.neocities.org/projects/visdeurbel.html).

# Dependencies
This model must be run on an Nvidia Tegra system with the jetson-inference packages and the latest release of L4T Ubuntu installed.
To build the jetson-inference packages:
```
git clone --recursive https://github.com/dusty-nv/jetson-inference
cd jetson-inference
mkdir build && cd build
cmake ../
```
It is recommended to install PyTorch when the option shows up at this step, although it can still be installed later.
Continue the setup as below:
```
make -j(nproc)
sudo make install
sudo ldconfig
```

# How to use
Clone and enter the Git repository: 
```
git clone https://github.com/Exist-nt/VisdeurBot.git
cd VisdeurBot
```

Run the detection script:
```
./detectnet.py /path/to/input.mp4 /path/to/output.mp4
```
The input can either be a .mp4 file, or a camera device - usually found at /dev/video0.
