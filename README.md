# NeuroPixels
With the development of technology, human interests have expanded to the brain, which used to be an unknown area.
There are fMRI, EEG, and many other methods for brain analysis.
So why do we use a new method called neuropixels?
First, basically, neuropixels measure Neuron signals directly by inserting them into the brain while awake.
For this reason, meaningful data can be obtained while learning several tasks.
Next, the neuropixel has a total of 384 channels and can measure numerous signals simultaneously in each channel.
It is possible to obtain information on vast Neuron population by simultaneously measuring many neurons at a time.


## VR rig
The most important key point when setting up multiple devices to use neuropixels is to be perfectly horizontal and perpendicular.
This is a necessary process to probe the exact part of the mouse brain.

### lick sensor with water reward system
<img src = "https://user-images.githubusercontent.com/90582481/156494129-5e2e5222-1b04-467e-9068-8ffcea865737.png" width="20%"><img src = "https://user-images.githubusercontent.com/90582481/156494144-80a0ae98-6b52-4bb0-92b6-5f06a101e496.png" width="20%">
### rotary encoder with wheel
<img src = "https://user-images.githubusercontent.com/90582481/156494116-d21c112b-537b-4176-bbae-25c31bf51d3d.png" width="20%"> <img src = "https://user-images.githubusercontent.com/90582481/156494148-8824cbb9-6522-42d9-9c2a-cdd4107ba32b.png" width="20%">
### head fix with linear actuator
<img src = "https://user-images.githubusercontent.com/90582481/156494028-3f07a84f-1b72-4a92-b20e-d2703cc7dde9.png" width="20%"><img src = "https://user-images.githubusercontent.com/90582481/156494028-3f07a84f-1b72-4a92-b20e-d2703cc7dde9.png" width="20%"> <img src = "https://user-images.githubusercontent.com/90582481/156494202-53508f10-a145-4227-b95e-febc316ae776.png" width="20%">
### monitor
### DAQ (PXIe) - Neuropixels
<img src = "https://user-images.githubusercontent.com/90582481/156494053-0ef8a7aa-0ced-4634-b611-c68227b12455.png" width="20%"> <img src = "https://user-images.githubusercontent.com/90582481/156494068-f4347089-09bd-430e-bac5-4f6df522aa4e.png" width="20%"> <img src = "https://user-images.githubusercontent.com/90582481/156494078-fe365dee-62a2-4b15-8222-1e0069e7667c.png" width="20%"> <img src = "https://user-images.githubusercontent.com/90582481/156494100-89d26f9d-e3fb-4633-95ae-9ce6415f050a.png" width="20%">
## NeuroPixels probe

1. Assembling- NeuroPixels
Carefully place the neuropixels neatly.
The probe and the iron bar must align parallel.

<img src = "https://user-images.githubusercontent.com/90582481/156494229-9692fd08-0659-458b-8dd6-5777a691a05f.png" width="20%"> <img src = "https://user-images.githubusercontent.com/90582481/156494281-b1645a9a-bee4-4b7c-9b3f-489497938d71.png" width="20%"> <img src = "https://user-images.githubusercontent.com/90582481/156494323-487a77d4-93a5-46de-bfc0-79dd34d23978.png" width="20%">


2.Combine-NeuroPixels,iron bar
Using 5 minute epoxy.

<img src = "https://user-images.githubusercontent.com/90582481/156494373-bd023185-a1f9-4f25-9ed2-1dbafadfc874.png" width="20%">


3.Connect-ground pin
Align the neuropixels as shown in the picture, and spread the space to put in thick paper.protect from heat
Soldering the ground pins that have been manufactured in advance.

<img src = "https://user-images.githubusercontent.com/90582481/156494424-b3947f1e-62d1-45ac-bb38-cbaed9a8e227.png" width="20%"> <img src = "https://user-images.githubusercontent.com/90582481/156494431-04749844-335f-48e0-9c79-b7f1224d1e1a.png" width="20%"> <img src = "https://user-images.githubusercontent.com/90582481/156494439-23e639b8-d331-40bf-bc74-f450781aed62.png" width="20%">


4. Finish

<img src = "https://user-images.githubusercontent.com/90582481/156494463-408669b9-adea-4770-b9d7-510b6494c0e3.png" width="20%"> <img src = "https://user-images.githubusercontent.com/90582481/156494471-f0a802b5-447f-484c-884c-4de52ac373dd.png" width="20%">
## Surgery
### leveling
### headfix
### ground pin
### craniotomy
## Kilosort
### setting
 Cuda 11.1, Matlab 2021a, Visual studio 2019 16.11.8
 
Download kilosort code file from:
https://github.com/MouseLand/Kilosort
change directory to CUDA folder in code,

>>>mexGPUall
>>>
Both kilosort and kilosort2 were compiled without errors.
change directory to D:\’folder with code’,

>>>kilosort

### Run
type kilosort and load data in kilosrt program.
We use neuropixels phase 3B aligned.

Click Run all

<img src = "https://user-images.githubusercontent.com/90582481/156521571-bd84806e-0ece-4a7a-bd82-25f47d590aa8.png" width="20%"> <img src = "https://user-images.githubusercontent.com/90582481/156523136-02314c30-87cb-4c1b-9180-8fe53f38d26b.png" width="20%">


## Phy
### setting
Install Anaconda: Python is installed automatically.

(Install Phy: https://phy.readthedocs.io/en/latest/installation/)
=> Upgrade Phy to Phy 2.0b1 (Reference: phy · PyPI)

ImportError: cannot import name 'Selector' from 'phylib.io.array' · Issue #1110 · cortex-lab/phy · GitHub


Open Anaconda Prompt.
Type.

conda create -n phy2 python pip numpy matplotlib scipy h5py pyqt cython pillow -y
conda activate phy2
pip install phy --upgrade

Type.
Pip install phy==2.0b1



### Run

Open Anaconda prompt

Type 

conda activate phy2

Type the drive where the data is (Ex. E:, You have to type the drive before changing directory.)

Type

cd ‘where the data is/params.py is’

Type

phy template-gui params.py  *If you use linux , check the params.py because windows and linux is little different to load data (If data is located in other drive)

<img src = "https://user-images.githubusercontent.com/90582481/156524506-2cfb6a45-6167-45d6-83e0-4f41ca4bccaf.png" width="20%">



## Data acquisition

### 1.put the mouse in the VR rig and set details such as water port.
### 2.Remove kiwik-cast
### 3.Drop saline
### 4.Connect the neuropixels and the interface cable
### 5.Connect the ground pin
### 6.Connect Neuropixels probe
### 7.Run SpikeGLX
### 8.Detect the neuropixels
### 9. Run the data acquisition
### 10. Run the VR-training system (matlab)


## AP_histology
### setting

AP_hisology download
npy-matlab download
Allen ccf atlas download

error -> function ‘loadStructureTree’ is not define

-> allen CCF master download

error ->  'smooth' requires one of the following:
  Curve Fitting Toolbox
  Econometrics Toolbox
  Sensor Fusion and Tracking Toolbox
-> download these packages

error->'bwareaopen' requires Image Processing Toolbox.

-> download this package

### Run
<img src = "https://user-images.githubusercontent.com/90582481/156525714-007f731c-7ede-47d3-918a-3f97a715021f.png" width="20%"> <img src = "https://user-images.githubusercontent.com/90582481/156525746-0d76c685-d060-4580-ac5e-d01cd5bd955a.png" width="20%">

