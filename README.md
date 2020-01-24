# MacOS EasyLookUp
Script and instructions to create **google translate shortkey for MacOS** that works on High-Sierra and Catalina. </br>
No more copy pasting, opening a browser tab , going to google translate etc etc. </br>MacOS Automator script (worklfow) + google translate(+urban dictionary) + shortkey binding.</br>
</br>
Easy as pie :)
</br>
</br>
See ['Instructions'](/Instructions.md) for</br>
- how to get started and set everything up in Mac OS automator (with screenshots)
- the actual code and what parameters to change (if any)
- how to link it to the shortkey combinations (with screenshots)
</br>
</br>
</br>


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

</br>
*Works in Chrome, Safari, Firefox and Brave (and most other non-browser applications depending on reserved keybindings)*
