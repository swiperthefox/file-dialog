file-dialog
===========

A firefox addon module that exports some functions of nsIFilePicker.

##The module exports:##

* ###Constants for the mode of dialog:###

    - modeOpen
    - modeSave
    - modeGetFolder
    - modeOpenMultiple
    
* ###Constants for the predefined file type filters:###

    - filterAll:  	Corresponds to the *.* filter for file extensions. All files will pass through the filter.
    - filterHTML:  	Corresponds to the *.html, *.htm, *.shtml and *.xhtml filters for file extensions.
    - filterText:  	Corresponds to the *.txt and *.text filter for file extensions.
    - filterImages:  	Corresponds to the *.jpe, *.jpg, *.jpeg, *.gif, *.png, *.bmp, *.ico, *.svg, *.svgz, *.tif, *.tiff, *.ai, *.drw, *.pct, *.psp, *.xcf, *.psd and *.raw filters for file extensions.
    - filterXML:  	Corresponds to the *.xml filter for file extensions.
    - filterXUL:  	Corresponds to the *.xul filter for file extensions.
    - filterApps:  	Corresponds to the platform specific application filter for file extensions. Application files for the user's platform will pass through the filter.
    - filterAllowURLs:  	Allow URLs. Requires Gecko 1.9
    - filterAudio:  	Corresponds to the *.aac, *.aif, *.flac, *.iff, *.m4a, *.m4b, *.mid, *.midi, *.mp3, *.mpa, *.mpc, *.oga, *.ogg, *.ra, *.ram, *.snd, *.wav and *.wma filters for file extensions. Requires Gecko 2.0
    - filterVideo:  	Corresponds to the *.avi, *.divx, *.flv, *.m4v, *.mkv, *.mov, *.mp4, *.mpeg, *.mpg, *.ogm, *.ogv, *.ogx, *.rm, *.rmvb, *.smil, *.webm, *.wmv and *.xvid filters for file extensions. Requires Gecko 2.0
    
* ###A function to open a file dialog:###

    *openModalFileDialog*(mode, filters, title)

    **Parameters:**
    
    - mode: one of the mode constants
    - filters: (optional) file type filters, it can be presented in any of the following forms:
      1. an integer: OR value of some of the predefined filters constants
      2. ["description", "ext"]: a specific type where "ext" is the file extension
       and "description" is a desciption of the type
      3. [f1, f2..]: an array of items, each item has one of above two forms
    - title: (optional) The title for the dialog.
   
   **Return value:**
    
    An array of paths. Will return [] if the user canceled the dialog.
   
