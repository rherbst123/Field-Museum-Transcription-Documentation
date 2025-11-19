# Transcriber-CLI Setup

## Setup for Linux
- Download the following repository either by using GitHub Desktop (reccomended) or cli (Whatever floats your boat). https://desktop.github.com/download/
- You will need to have completed the AWS CLI setup and enter your credentials, a guide for doing this can be found here **ADD INSTRUCTIONS**

- Once downloaded, navigate to the correct repository filepath, GitHub desktop usually downloads to your documents folder so the following command should bring you there if defaults are chosen.
```
cd Documents/GitHub/Transcriber-CLI-V2/
```

- Your filepath should now look like the following if you are in the correct folder
![image](../Instruction%20Images/Navigate.png)

- We will now need to create a virtual environment to download our packages to run the Transcriber.
- The following command will create a virtual environment
```
python3 -m venv Transcriber
```

- The "Transcriber" can be named anything you desire it is just named Transcriber in this case for example-sake 
- Here is a before and after seeing how your files should look after creating a the venv
![image](../Instruction%20Images/VirtualEnv.png)

- By Default the virtual environment will not be enabled so you will need to activate it with the following command
```
source Transcriber/bin/activate
```

- Entering this command puts you into a virtual enviroment. When entered correctly a prefix for your command line will be present. See the following for a visual.

![image](../Instruction%20Images/venv.png)

- **NOTE: you only need to create the environment ONCE**
- The following commands will get you into the repository and into the environment, Just copy and paste!
```
cd Documents/GitHub/Transcriber-CLI-V2
source Transcriber/bin/activate
```
- We will now need to install the required packages to run the program!
- From the main folder you will need to go one folder deeper into the next folder named **Transcriber-CLI-V2**. The following command will do this for you
```
cd Transcriber-CLI-V2
```
- Once in this next folder you should have a setup that looks like so...
![image](../Instruction%20Images/IntheFolder.png)

- Now you can install your required packages with the command
```
pip3 install -r requirements.txt
```
- You will see a bunch of text appear and loading bars go, this means you are doing the right thing!
 
![image](../Instruction%20Images/Loading.png)


- For the segmentation pipeline, Tesseract-OCR is required, For linux the following command is used to download it.
```
sudo apt install tesseract-ocr
```
- Enter in your sudo password and you will have completed the setup process!


## Final command once setup is complete
```
cd Documents/GitHub/Transcriber-CLI-V2
source Transcriber/bin/activate
cd Transcriber-CLI-V2
```

## Run The Transcriber
- Once all the previous requiremnts have been met, you can run the transcriber software by using the following command
```
python Transcriber_CLI.py
```
- The following screen will be displayed and you will be good to go!

![image](../Instruction%20Images/LandingPage.png)
#
### To see how to configure and run the CLI please refer to this page
[Transcriber User Guide](TranscriberConfiguration.md)

- Happy Transcribing!