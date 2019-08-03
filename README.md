## Flamingo - Awesome Keyboard Remapper for macOS High Sierra 10.13 / Sierra 10.12, Replacement for Karabiner

Flamingo is an keyboard remap tool for macOS. Also supports mouse remap, keyboard macro, define shell script hotkey, or event Apple Script.  

[中文介绍请点我](https://openfibers.github.io/flamingo/README_cn)

### [Download 1.2.0](https://github.com/OpenFibers/flamingo/raw/master/Apps/Flamingo.app_1.2.0.zip)

### Remap Keys or Mouse Buttons
For example: you may want to press middle mouse key to open Mission Control. Just make a map: mouse button 2 to control + up in Flamingo preferences.  
Configuration is in JSON format, which is easy to learn:  

```
{
  "map" : [
    {
      "from" : "mouse2",
      "to" : "control up"
    }
  ]
}
```

### Key Macros

Make working easier. Press only one key to auto type some text. For example, press option + ], enter `[[ alloc] init];`:  
<img src="https://github.com/OpenFibers/flamingo/raw/master/Images/autotype.gif" alt="auto_type" style="width: 430px;"/>

Add configuration below, and that's it:  

```
{
  "map" : [
    {
      "alias" : "Create New Object",
      "from" : "option ]",
      "to" : "[ [ space a l l o c ] space i n i t ] ; left left left left left left left left left left left left left left "
    }
  ]
}
```

Make gaming easier. Perform amazing gaming actions with simple human actions:  
<img src="https://github.com/OpenFibers/flamingo/raw/master/Images/dota2_kael.gif" alt="dota2_kael" style="width: 390px;"/>


### Shell Script Hotkey

For example: press control + escape to open terminal, and change to project directory, and do git pull:  

```
{
  "from" : "control escape",
  "script" : "cd ~/projects/flamingo&&git pull"
}
```

### AppleScript Hotkey

AppleScript is a powerful scripting language that allows users to directly control scriptable Macintosh applications, as well as parts of macOS itself. For example: using option + F to close all Finder window:  

```
{
  "from" : "option F",
  "AppleScript" : "tell application \"Finder\" to close every window"
}
```

Or using option + P to pause iTunes :  

```
{
  "from" : "option P",
  "AppleScript" : "if application \"iTunes\" is running \n tell application \"iTunes\" to pause \n end if"
}
```

Check [Introduction to AppleScript Language Guide](https://developer.apple.com/library/content/documentation/AppleScript/Conceptual/AppleScriptLangGuide/introduction/ASLR_intro.html) for more infomation about AppleScript.  

[Full Usage and All Key Definations, Click Here](https://openfibers.github.io/flamingo/help)

### Cannot map keys? Add Flamingo to Accessability

1. Open System Preferences.app  
2. Go to "Security & Privacy -> Privacy -> Accessability"  
3. Add Flamingo.app to allowed list   
* You can still map mouse button to any key without doing this.  

<img src="https://github.com/OpenFibers/flamingo/raw/master/Images/privacy_en.png" alt="privacy_cn" style="width: 668px;"/>

### Safety
Though it's not an open source software (like Karabiner), Flamingo never use any network or record what you tap, Which makes ti to be safe to use.  
But never download Flamingo from website other than current page.  

[中文介绍请点我](https://openfibers.github.io/flamingo/README_cn)

### [Download 1.2.0](https://github.com/OpenFibers/flamingo/raw/master/Apps/Flamingo.app_1.2.0.zip)

Any questions? Mail to [openfibers@gmail.com](mailto://openfibers@gmail.com).  
