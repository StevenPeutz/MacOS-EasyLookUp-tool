# Shortcutting manually translating in Mac OS Catalina (regardless of browser) #

### How to set it up; ###
The Google translate part</br>

1. Open up 'Automator' (open spotlight (⌘+ Spacebar) and then search for 'automator')</br>

2. Select 'Quick Action' in the opening screen, and click 'Choose': </br>
This should look like this: [step 1 screenshot](/Images/Step1-screenshot.png)</br>

3. Now use the search field above the second column on the left, use it to search for 'run applescript'. Once found drag 'run applescript' to the empty canvas on the right.</br> 
It should look like this: [step 2 screenshot](/Images/Step2-screenshot.png)</br>

4. Do the same again but instead of 'run applescript' search for 'website popup' and drag it underneath your 'run applescript' on the canvas.</br> 
It should like like this: [step 3 screenshot](/Images/Step3-screenshot.png)</br>

5. Now replace the code in the 'run applescript' with the following;

```
on run {input, parameters}
 set output to "http://translate.google.com/translate_t?sl=auto&tl=en&text=" & urldecode(input as string)
 return output
end run
on urldecode(x)
 set cmd to "'require \"cgi\"; puts CGI.escape(STDIN.read.chomp)'"
 do shell script "echo " & quoted form of x & " | ruby -e " & cmd
end urldecode
```

Change 'Workflow receives current' from 'nothing/default' to 'text'.
The parameter 'tl' is here set to 'en' (english) but this can be replaced to language of choice (just look up the google translate language code [find here](https://cloud.google.com/translate/docs/languages). Do not change the 'sl' parameter value though!</br>
Also you probably want to decrease the size of the popup for convenience (just change 'Site Size' from Large to Medium with the drop down menu in the Website popup widget in the canvas)

Go to 'file' and 'save' (in the menu bar) and then you can give your workflow script a name (e.g. OuiOuiBaguette.workflow) and save it.</br>

You should have the following: [step 4 screenshot](/Images/Step4-screenshot.png)</br>
*(The green checkmarks come after running the script. If you have a red one for 'Workflow completed', run the script again and use 'close' instead of 'cancel' in the website popup (or just ignore it all together).*</br>


6. Go to System Preferences > Keyboard</br>
Under Keyboard click the tab named 'shortcuts' and in the left column select 'services'.
Now in the right under the subheader 'text' you should have your script listed there un the name you have given it (OuiOuiBaguette in my case).</br>
Make sure the box for the script is ticked and create a shortcut (where it says 'none') . Surprisingly much shortcuts (especially within chrome) are reserved already which will overrule the one you create here, making it not work! I know ⇧⌘Z (Shift+Command+Z) is free in chrome and safari and MacOS itself. Choosing ⇧⌘Z would allow you to use the one next to it (⇧⌘X) for slang (urban dictionary) and the one next to that (⇧⌘C ) for both in sequence.

It should look more or less like this: [step 5 screenshot](/Images/Step5-screenshot.png)
</br>
**And you are done!**</br>
You can test your new tool by selecting (i.e. 'highlighting') some text and pressing ⇧⌘Z 
</br>
# done #
</br>


## The Urban Dictionary part *(optional)* ##
1. Same as above, repeat step 1, 2,3, 4 and 5.
But the code for step 5 is:

```
on run {input, parameters}
set output to "https://www.urbandictionary.com/define.php?term=" & urldecode(input as string)
return output
end run
on urldecode(x)
set cmd to "'require \"cgi\"; puts CGI.escape(STDIN.read.chomp)'"
do shell script "echo " & quoted form of x & " | ruby -e " & cmd
end urldecode
```

Go to 'file' and 'save' (in the menu bar) and then you can give your workflow script a name (e.g. Cardi_B_said.workflow) and save it.</br>
It should look like this: [step 6 screenshot](/Images/Step6-optional.png)</br>

2. repeat step 6 to create the (⇧⌘X) shortkey for your urban dictionary loopup script.</br>
</br>
---


## Creating a sequence *(optional)* ##
creating a combination (sequence) of both;
Now you can also create a script now that invokes both these scripts in a sequence, for when you do not know if it is a slang a just a different language, and assign this to ⇧⌘C.

Repeat 1 and 2 -again- but now find and pull your two existing scripts (OuiOuiBaguette.workflow and Cardi_B_said.workflow from the left column to the right (where before we put the 'run applescript' and the 'website popup')</br>
This should look like this: [step 7 screenshot](/Images/Step7-optional.png)

 Go to 'file' and 'save' (in the menu bar) and then you can give this 3rd workflow script a name (e.g. BabelFish.workflow (because one should always use a hitchhiker's guide reference when even somewhat possible :P )) and save it.</br>
</br>
</br>

## Done ##

- highlight text + ⇧⌘Z = google translate</br>
- highlight text + ⇧⌘X = urban dictionary</br>
- highlight text + ⇧⌘C = google translate followed by urban dictionary (while remembering original highlight as input)</br>
</br>
</br>
</br>
---
</br>


## FAQ ##

**Where are the script located after saving etc?**</br>
Finder > Home > Library > Services. (If there is no 'Library' folder within your 'Home' folder, go to your home folder and fo to 'view' in the menubar and click 'show view options' and select the option to display the Library folder.)

**I want the google translation to be in some other language than English.**</br>
The parameter 'tl' is here set to 'en' (english) but this can be replaced to language of choice (just look up the google translate language code (find here)) and change it in the script.</br>
 set output to "http://translate.google.com/translate_t?sl=auto&tl=en&text=".....
