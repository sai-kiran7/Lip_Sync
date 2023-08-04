#Google Colab Link


#Prerequisites
-------------
- `Python 3.6` 
- ffmpeg: `sudo apt-get install ffmpeg`
- Install necessary packages using `pip install -r requirements.txt`. Alternatively, instructions for using a docker image is provided [here](https://gist.github.com/xenogenesi/e62d3d13dadbc164124c830e9c453668). Have a look at [this comment](https://github.com/Rudrabha/Wav2Lip/issues/131#issuecomment-725478562) and comment on [the gist](https://gist.github.com/xenogenesi/e62d3d13dadbc164124c830e9c453668) if you encounter any issues. 
- Face detection [pre-trained model](https://www.adrianbulat.com/downloads/python-fan/s3fd-619a316812.pth) should be downloaded to `face_detection/detection/sfd/s3fd.pth`. Alternative [link](https://iiitaphyd-my.sharepoint.com/:u:/g/personal/prajwal_k_research_iiit_ac_in/EZsy6qWuivtDnANIG73iHjIBjMSoojcIV0NULXV-yiuiIg?e=qTasa8) if the above does not work.




# Steps to run the Notebook:


 - Step 1: First create two folders in your google drive that follows naming conventions as Wavlip and WavLip.
 - Step 2: Download the weights of the model from the links provided below and drop the downloaded file into Wavlip folder in Google Drive .
Getting the weights

----------

| Model  | Description |  Link to the model | 
| :-------------: | :---------------: | :---------------: |
| Wav2Lip  | Highly accurate lip-sync | [Link](https://iiitaphyd-my.sharepoint.com/:u:/g/personal/radrabha_m_research_iiit_ac_in/Eb3LEzbfuKlJiR600lQWRxgBIY27JZg80f7V9jtMfbNDaQ?e=TBFBVW)  |
| Wav2Lip + GAN  | Slightly inferior lip-sync, but better visual quality | [Link](https://iiitaphyd-my.sharepoint.com/:u:/g/personal/radrabha_m_research_iiit_ac_in/EdjI7bZlgApMqsVoEUUXpLsBxqXbn5z8VTmoxp55YNDcIA?e=n9ljGW) |
| Expert Discriminator  | Weights of the expert discriminator | [Link](https://iiitaphyd-my.sharepoint.com/:u:/g/personal/radrabha_m_research_iiit_ac_in/EQRvmiZg-HRAjvI6zqN9eTEBP74KefynCwPWVmF57l-AYA?e=ZRPHKP) |
| Visual Quality Discriminator  | Weights of the visual disc trained in a GAN setup | [Link](https://iiitaphyd-my.sharepoint.com/:u:/g/personal/radrabha_m_research_iiit_ac_in/EQVqH88dTm1HjlK11eNba5gBbn15WMS0B0EZbDBttqrqkg?e=ic0ljo) |

Lip-syncing videos using the pre-trained models (Inference)

----------

 - Step 3: Upload the audio(Eg .wav file) and the video file(Eg  .mp4 file) that you want to LipSync into the "WavLip" folder.  
 - Step 4: Open this google colab as mentioned on the top of this page.

--------
**Note**
--------
Ensure that while uninstalling the tensorflow-gpu in google colab it asks for permission to proceed you need to type "y" in the rectangular box while the cell is running.

---------

 - Step 5: Try to run the dependencies in order specified in the colab notebook.
 - Step 6: While running the colab notenooks make sure that the names of the audio and video files name match exactly the same that are uploaded in the "WavLip" folder.Otherwise you will encounter an error.Also ensure that therer are no spaces in the file names.

 - Step 7: After passing both the audio and video files through the model we can obtain the resultant video in the results/result_voice folder
 - Step 8: Download the video and observe the LipSync video
 - Step 9: To observe the evaluation of the model go tp the results/ dirstory in the colab notebook
 - Step 10: I have provided other alternative 2 ways of inferencing the model one adjusts the chin movement better as we have applieed padding and the other reduces the video resolution if the resolution is too high it is performed to ensure that therer would be no resolution incompatibility..
 

