# EasyLookUp Descripion and Installation Guide.

## **Easier and faster translation, slang and people lookup without tab-switching.
**

[Image: image.png]

## How does it work when installed?

When installed, the EasyLookUp tool works by;

* highlighting the desired text and pressing  **⌃⌘Z**  will get you the  google translate translation and language.
* highlighting the desired text/slang and pressing **⌃⌘X**  will get you urban dictionary’s explanation of the slang
* highlighting the desired name and pressing **⌃⌘C**  will get you wikipedia and SoMe results for the individual

*(****⌃ ****= control key,**** ⌘ ****= the command key****)***

**The EasyLookUp tool works within SRT, ALR, bouncer, CENTRA, google docs, Quip, Notes and some other applications**





# Installation guide



## Step 1: download scripts

Download the ‘EasyLoopUp’  zip file from [_here_](https://drive.google.com/drive/u/1/folders/1VSRcoWuLXcwQnatvIkt1eKBb6IpSafQe) (google drive) 
*  ..or from *[*_here_*](https://www.dropbox.com/s/qgzajlmolhplhss/EasyLookUp.zip?dl=0)* (dropbox), if google drive doesn’t work for you.*

# *
**//This location has to change to a fb wiki location!***



## Step 2:  unzip and install each file

Go to your downloaded file and unzip it (unzipping is done by double clicking). 
The unzipped file should contain 4 files:


* ‘ELU_*OuiOuiBaguette.worfklow*’ (this one queries Google Translate)
* ‘ELU_*Cardi_b_said.workflow*' (this one queries Urban Dictionary)
* ‘ELU_*WhoThis.workflow*’ (this one queries duckduckgo with wikipedia and SoMe parameters
* *Optional (Spanish language reps):  ‘ELU_AsiHablamos’ (Queries asihablamos)*


(1) Double click each file (non Spanish reps can skip ‘ELU_AsiHablamos’) and  click ‘Install’ on the prompted window.
[Image: image.png]
(2) Then click the x-out in the following window
[Image: image.png]



Repeat this this for the remaining files. *(double click  the file, click install, click x-out)*




## Final Step:  linking the scripts to shortcuts

Go to **Keyboard **(‘system preferences’ > keyboard) or go there directly by typing ‘keyboard’ in spotlight.

Under ‘Keyboard’ click the tab named '**shortcuts**', then in the left column select '**services**'.

Now in the right (under the subheader '*text*') you should find all the scripts starting with 'ELU_'.
[Image: image.png]
Make sure the blue box for each of the scripts starting with ‘ELU_’ is ticked and click where it says ‘none’ to **create the shortcut **as seen in the screenshot above. 
*Surprisingly much shortcuts (especially within chrome) are reserved already which will overrule the one you create here, preventing it from working. To prevent this use the ones listed below:*

* **⌃⌘Z** (Control+Command+Z) is free in chrome and safari and MacOS itself and can be pressed with one hand. I suggest using this combination for ‘ELU_OuiOuiBaguette’
* Similarly, set **⌃⌘X** (Control+Command+X) for ‘ELU_Cardi_b_said’
* Similarly, set **⌃⌘C** (Control+Command+C) for ‘ELU_WhoThis’
* *Optional (Spanish language):  set ****⌃⌘V**** (Control+Command+V) for ‘ELU_AsiHablamos’*






# You Are Done! 

**Congratulations! **You have set up a convenient lookup tool that will work not only within SRT, but also in ALR, CRT, bouncer, CENTRA, Layton, User Admin, escalations, Quip and notes 

Take it for a spin now or just try it when working queues;
[Image: image.png]
* highlight text and press **⌃⌘Z**  = google translate
* highlight text and press **⌃⌘X**  = urban dictionary
* highlight text and press **⌃⌘C**  = duckduckgo search some SoMe and wiki parameters
* *highlight text and press ****⌃⌘V****  = asihablamos (Spanish reps)*




* * *
***Hi!

If you enjoy using this, if this setup guide has helped you, or if you have tips how to make it better please send me an email with your feedback or questions!
I would appreciate it greatly ***


***Thanks!    Steven Peutz***

[Image: image]* * *




# FAQ:


**For who is this?**
This can be used by all facebook FTE’s, but this first version was designed for Market Specialists. 

**Where are the script located after saving etc?**
Finder > Home > Library > Services. (If there is no 'Library' folder within your 'Home' folder, go to your home folder and fo to 'view' in the menubar and click 'show view options' and select the option to display the Library folder.)

**I want the google translation to be in some other language than English.**
The parameter 'tl' is here set to 'en' (english) but this can be replaced to language of choice (just look up the google translate language code ([find here](https://cloud.google.com/translate/docs/languages))) and change it in the script.

```
  set output to "http://translate.google.com/translate_t?sl=auto&tl=en&text=".....
```

(or just walk by my desk and I’ll change it for you)

**For the google translate part why not use the ‘translate page’ option in the chrome browser menu?**
This option will be blocked or taken out of our chrome implementation because of privacy concerns from facebooks end. This functionality seems to take in the while page and this will also include sensitive (e.g. PII) information we shouldn’t be sharing like this. This EasyLookUp tool will only take the manually selected content to be translated.

**The scripts (after clicking install) do still not all show up under ‘shortcuts’ > ‘services’ (step 3.)**
If this is the case you should right click the file (see question above for location of scripts) in finder and choose ‘open with atom’. This  should open a folder with two scripts, go to the second one (named inf.plist) and check whether the name used in that script is exactly the same as the name of the workflow file itself. (Or just come by my desk and I’ll try to fix it).

**Are we expanding this to contractors or OS reps as well?**
We want to start small with market specialists and BI analysts and first evaluate the UX and time save estimates of this first group. Depending on these results we will look at options for rolling out to contractors and OS reps. Where a couple of seconds saved per SRT/ALR job will add up to large time saves quickly.
To support this evaluation please fill out this 1 minute survey: [**https://forms.gle/kBeGt1vVB63NC9wh7**](https://forms.gle/kBeGt1vVB63NC9wh7)** **

**Source code and further details:
**[**https://fburl.com/ikzr3hcr**](https://fburl.com/ikzr3hcr)**  (**quip) or contact me ([stevenpeutz@fb.com](mailto:stevenpeutz@fb.com))


*Please fill in this 1 minute survey to estimate UX and to find way to improve it: ** *https://forms.gle/kBeGt1vVB63NC9wh7 


