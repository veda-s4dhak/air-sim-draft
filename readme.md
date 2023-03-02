<h2> Development Environment Setup (macOS) </h2>

1) Download the Epic Games Launcher from https://www.unrealengine.com/en-US/download

2) Run the following commands to setup AirSim

```
cd git
git clone https://github.com/Microsoft/AirSim.git
cd AirSim
./setup.sh
./build.sh
cd AirSim/Unreal/Environments/Blocks
./GenerateProjectFiles.sh /Users/Shared/Epic\ Games/UE_4.27/
```

<h2> Select your XCode Command Line Tools Directory </h2>

1) Run the following command to set the command line tools directory

```
sudo xcode-select -s /Library/Developer/CommandLineTools
```

<h2> Start up your Simulation </h2>

1) Browse to AirSim/Unreal/Environments/Blocks.
2) Run ./GenerateProjectFiles.sh <UE_PATH> from the terminal, where UE_PATH is the path to the Unreal installation folder. (By default, this is /Users/Shared/Epic\ Games/UE_4.27/) The script creates an XCode workspace by the name Blocks.xcworkspace.
3) Open the XCode workspace, and press the Build and run button in the top left.
4) After Unreal Editor loads, press Play button.

<h2> Install Python Dependencies </h2>

1) Run the following command to install 

```
python3 -m pip install msgpack-rpc-python
python3 -m pip install airsim
```

<h1>Development Environment Setup (Windows 11)</h1>
<h2>Install Unreal Engine</h2>

1) Download the Epic Games Launcher. 
2) Run the Epic Games Launcher, open the Unreal Engine tab on the left pane. Click on the Install button on the top right, which should show the option to download **Unreal Engine >= 4.27**. 
3) Chose the install location to suit your needs.

<h2>Build AirSim</h2>

1) Install **Visual Studio 2022**. Make sure to select Desktop Development with C++ and Windows 10 SDK 10.0.19041 and select the latest .NET Framework SDK under the 'Individual Components' tab while installing VS 2022.
2) Start **Developer Command Prompt for VS 2022**.
3) Clone the repo: `git clone https://github.com/Microsoft/AirSim.git`, and go the AirSim directory by `cd AirSim`.
4) Run `build.cmd` from the command line. (This will create ready to use plugin bits in the Unreal\Plugins folder that can be dropped into any Unreal project.)

<h2>Build Unreal Project </h2>
Finally, you will need an Unreal project that hosts the environment for your vehicles. 

1) Make sure to close and re-open the Unreal Engine and the Epic Games Launcher before building your first environment
2) After restarting the Epic Games Launcher it will ask you to associate project file extensions with Unreal Engine, click on 'fix now' to fix it. 
2) AirSim comes with a built-in "Blocks Environment" which you can use, or you can create your own. 
3) 


<h2>How to Use AirSim </h2>

Once AirSim is set up by following above steps, you can :

1) Double click on .sln file to load the Blocks project in **Unreal\Environments\Blocks** (or .sln file in your own custom Unreal project). If you don't see .sln file then you probably haven't completed steps in Build Unreal Project section above.

Note: Unreal 4.27 will auto-generate the .sln file targetting Visual Studio 2019. Visual Studio 2022 will be able to load and run this .sln, but if you want full Visual Studio 2022 support, you will need to explicitly enable support by going to 'Edit->Editor Preferences->Source Code' and selecting 'Visual Studio 2022' for the 'Source Code Editor' setting.

2) Select your Unreal project as Start Up project (for example, Blocks project) and make sure Build config is set to "Develop Editor" and x64.
3) After Unreal Editor loads, press Play button.

<h2>Downloading the Simulation using Pre-Built Binaries</h2>
1) Visit this link : https://github.com/Microsoft/AirSim/releases/.  
2) Download and run the exe file.

> Note : These binaries will only run on Windows.

<h1> Reference </h1>

https://microsoft.github.io/AirSim

<h2> Setup drone-os </h2>

_Clone this repo beside the AirSim repo cloned above._
