# Transcriber User Guide
- **IF you have NOT setup the transcriber please go back and use the following guide to setup the Transcriber.** [Transcriber Setup](README.md)
#


- Once you setup 
    - 1. AWS-cli
    - 2. GitHub repository
    - 3. Create a virtual environment 
    - 4. Download Tesseract and necessary packages
- You can now Transcribe Images as you please!

#### Quick Command to starting the Transcriber
##### Linux Command
```
cd Documents/GitHub/Transcriber-CLI-V2
source Transcriber/bin/activate
cd Transcriber-CLI-V2
python Transcriber_CLI.py
```
##### Windows Command
```
cd Documents/GitHub/Transcriber-CLI-V2
Transcriber\Scripts\activate
cd Transcriber-CLI-V2
python Transcriber_CLI.py
```

- Once all configured the commands will lead you to the landing page!
![image](../Instruction%20Images/LandingPage.png)


# The Starting Page
- Once at the starting page you will be greeted with 3 options. **Start Transcription Process, Confgure Validation Settings and Exit**
- **Start Transcription Process:** Brings you to the next step of getting Transcriptions
- **Configure Validation Settings:** Brings you to the validation configuration where you can choose to enable or disable tiers of validation
- **Exit:** Exits and kills the program

## Confgure Validation Settings
![image](../Instruction%20Images/Configuration.png)
- All choices are a boolean (on or off)
- **Scientific Names**: Global names verifier using Tropicos (gives a near match along with type of match and who entered the source)
- **Duplicate Records:** Search on the Barcode in the Symbiota Portal (Returns a full record if entry is found)
- **Duplicate Entries:** Search on Collector, Record Number and Date collected (Returns a full record entry is found)



## Transcription Process
-  After selecting configuration settings you can enter to start transcribing.
- After selecting option **1** you will be prompted to select a name for this run (if left blank a time stamp will be as a default)

![image](../Instruction%20Images/StartPage.png)

-  After a name for the run is entered you will be asked if you want to use segmentation
    - 1 for yes and 2 for no

-  After selecting if segmentation is going to be used you will be asked if you want to do one or two shots:
    - **1 Shot:**  Image + Prompt sent to LLM a single .csv is returned 
    - **2 Shot:**  1st Shot + image + prompt + secondary prompt: two .csv files are returned 

- After selecting the shot count, you can choose a prompt. 
    - **as of 12/12025 prompt_1.5.8 is the most stable** 

- After selecting a prompt you can choose how to access the images: 
    - Local Image: Images in a folder, just copy and paste the file path to the folder
    - Image URL's: Enter the path to a .txt file containing all image urls's (Make sure to have .txt at the end)

- After entering in your images, Segmentation will take place. Depending on how many images and how strong your computer is. This process can vary in time. 

- After segmentation has competed, You can choose models for your shots
    - **As of 12/1/2025**
    - From findings, our team has found that AWS Nova Premire for the first shot and LLama-3.2 90b for a second shot returns good results

- Let the transcriber do it's thing!
    - A folder named "Finished Transcriptions" will be made on your desktop. All results will be here
