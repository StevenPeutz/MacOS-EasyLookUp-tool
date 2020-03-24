# EasyLookUp Descripion and Installation Guide.

## **Easier and faster to Google Translate, Urban dictionary and wikipedia (through duckduckgo) without tab-switching.**

![MacOS_GoogleTranslate_shortcut tool](/Images/MacOS_GoogleTranslate_shortcut.png)

## How does it work when installed?

When installed, the EasyLookUp tool works by;

* highlighting the desired text and pressing  **⌃⌘Z**  will get you the  google translate translation and language.
* highlighting the desired text/slang and pressing **⌃⌘X**  will get you urban dictionary’s explanation of the slang
* highlighting the desired name and pressing **⌃⌘C**  will get you wikipedia and SoMe results for the individual
</br>
</br>
**The EasyLookUp tool works within Chrome, Safari, Firefox, Brave, google docs, Quip, Notes and some other applications**  





# Installation guide



## Step 1: download scripts

Download the ‘EasyLoopUp’ zip file from this github

</br>
</br>

## Step 2:  unzip and install each file

Go to your downloaded file and unzip it. 
The unzipped file should contain 4 files:


* ‘ELU_*OuiOuiBaguette.worfklow*’ (this one queries Google Translate)
* ‘ELU_*Cardi_b_said.workflow*' (this one queries Urban Dictionary)
* ‘ELU_*WhoThis.workflow*’ (this one queries duckduckgo with wikipedia and SoMe parameters
* *Optional (for Spanish language slangs):  ‘ELU_AsiHablamos’ (Queries asihablamos)*
</br>
</br>
(1) Double click each file (non Spanish should skip ‘ELU_AsiHablamos’) and  click ‘Install’ on the prompted window.</br>  
![Mac_OS_Shortcuts_EasyLookUp](/Images/MacOS_translate_shortcut_step1.png) </br>
(2) Then click the x-out in the following window</br>
![Mac_OS_Shortcuts_EasyLookUp_2](/Images/MacOS_translate_shortcut_step2.png) </br>



Repeat this this for the remaining files. *(double click  the file, click install, click x-out)*</br>

</br>


## Final Step:  linking the scripts to shortcuts

Go to **Keyboard **(‘system preferences’ > keyboard) or go there directly by typing ‘keyboard’ in spotlight.

Under ‘Keyboard’ click the tab named '**shortcuts**', then in the left column select '**services**'.

Now in the right (under the subheader '*text*') you should find all the scripts starting with 'ELU_'.</br>
![Mac_OS_Shortcuts_EasyLookUp_3](/Images/MacOS_translate_shortcut_step3.png)</br>
Make sure the blue box for each of the scripts starting with ‘ELU_’ is ticked and click where it says ‘none’ to **create the shortcut **as seen in the screenshot above. 
*Surprisingly much shortcuts (especially within chrome) are reserved already which will overrule the one you create here, preventing it from working. </br>
To prevent this use the ones listed below:*

* **⌃⌘Z** (Control+Command+Z) is free in chrome and safari and MacOS itself and can be pressed with one hand. I suggest using this combination for ‘ELU_OuiOuiBaguette’
* Similarly, set **⌃⌘X** (Control+Command+X) for ‘ELU_Cardi_b_said’
* Similarly, set **⌃⌘C** (Control+Command+C) for ‘ELU_WhoThis’
* *Optional (Spanish language):  set ****⌃⌘V**** (Control+Command+V) for ‘ELU_AsiHablamos’*
</br>
</br>




# You Are Done! 

**Congratulations! **You have set up a convenient lookup tool that will work in any browser and most other applications as preview, Google Docs, Quip, Notes etc.

Take it for a spin now or just try it when working queues;
![4](/Images/MacOS_GoogleTranslate_shortcut.png)
* highlight text and press **⌃⌘Z**  = google translate
* highlight text and press **⌃⌘X**  = urban dictionary
* highlight text and press **⌃⌘C**  = duckduckgo search some SoMe and wiki parameters
* *highlight text and press ****⌃⌘V****  = asihablamos (for Spanish slangs/urban speak)*




* * *
***Hi!

If you enjoy using this, if these scripts and setup guide has helped you, or if you have tips how to make it better please send me an email with your feedback or questions!
I would appreciate it greatly ***


***Thanks!    Steven Peutz***</br>

![5](/Images/Cat.png)  </br>

</br>
</br>

# FAQ:


**For who is this?**
Anyone who uses MacOS and is tired of copy pasting in new tabs in their browser to go to google translate or urban dictionary.
</br>
**Where are the script located after saving etc?**
Finder > Home > Library > Services. (If there is no 'Library' folder within your 'Home' folder, go to your home folder and fo to 'view' in the menubar and click 'show view options' and select the option to display the Library folder.)
</br>
**I want the google translation to be in some other language than English.**
The parameter 'tl' is here set to 'en' (english) but this can be replaced to language of choice (just look up the google translate language code ([find here](https://cloud.google.com/translate/docs/languages))) and change it in the script.

```
  set output to "http://translate.google.com/translate_t?sl=auto&tl=en&text=".....
```

</br>
**The scripts (after clicking install) do still not all show up under ‘shortcuts’ > ‘services’ (step 3.)**
If this is the case you should right click the file (see question above for location of scripts) in finder and choose ‘open with atom’. This  should open a folder with two scripts, go to the second one (named inf.plist) and check whether the name used in that script is exactly the same as the name of the workflow file itself.
</br>


