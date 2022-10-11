# utl_classic_sas_editor_display_manager_commands_improved
Classic SAS editor display manager commands. Keywords: sas sql join merge big data analytics macros oracle teradata mysql sas communities stackoverflow statistics artificial inteligence AI Python R Java Javascript WPS Matlab SPSS Scala Perl C C# Excel MS Access JSON graphics maps NLP natural language processing machine learning igraph DOSUBL DOW loop stackoverfl SAS community.


    Classic SAS editor display manager commands
    
     Youtube
    https://www.youtube.com/playlist?list=PLS2pNYD0QwbdHoSnn3p0_xSYDt1y1iDze

    for this post
    https://goo.gl/xXYQ3d
    https://github.com/rogerjdeangelis/utl_classic_sas_editor_display_manager_commands_improved

    github
    https://github.com/rogerjdeangelis
    click on repositories and search 'classic'

    Yotube video on debug macro.
    https://www.youtube.com/edit?o=U&video_id=JrxooHTx0c8

    You can put the tools below on mouse actions, function keys or command lines(log/program/output/note).
    I have no idea why SAS massively markets 'paint your screen editors' (ie SAS studio)
    Why not maintain and enhance this editor

      Needed enhancements and fixes

       1.  Add prefix commands X XX and flip
       2.  Add command history of commands in stead of just '?' prevcmd
       3.  c roger mary in lines signature * test under condition (c roger mary in 1:10/)
       4.  Also fix the 'ignore valuable data' setting
       5.  More stable sasuser.profile
       6. Fix the inconsistent :tf command (trxt flow)
       7. Bring bacl the cursor and curpos command

      Example command line functionality

        X
        STORE  * purposely disabled in all subsequent editors?
               * Store highlighted text in clipbrd.
               * You can  operate on text saved in clipboard using commands like 'debugHighlightedMacro'
               * or use a function key
               * same as ctl-c but it is programmable!!!!

        GSUBMIT    put on function key  "store;gsubmit '%debugHighlighedMacro;'
        NOTESUBMIT  note;notesubmit ''%printLastDataset;'

        dlgrun * Opens a dialog box where you can enter an application to run 'excel.exe'
        dlgopen * opens windows explorer so you can look and view files
        dlgsave * opend the save as dialog box
        dlgprtpreview * print preview window in focus (log/output/program/note)
        wsave all; * save your mutiscreen setup



        see end of this message fir more W and DLG commands


      THIS SHOULD SUBSTANTIALLY IMPROVE YOUR PERFORMANCE

       Very fast point and shoot editing and code submit classic SAS editor.

       suppose you want to submit highlighted code using just the right mouse key.
       (extremely fast becase left had is over alt key and right is on mouse)

       Use the ALT key as you hold down the mouse button and drag the mouse
       to select a rectangular block (or column) to submit

       After the highlighted  hit the right mouse button and the highlighted code will
       be executed.

       type change x y on the command line

       then x will be changed to y only in the highlighted area.

       Simple actions like typing '860' on the command line will take move cursor
       to line 860. On long programs I sometimes jot down the location of
       key lines.


     USEFUL EDITIING COMMANDS
     *************************

      The prefix area  Many of these commands can be put on function keys using a ':', ie :ts.
      SAS is slowly removing some of these functions from theclassic editor?

      D        Delete current line
      I        Insert a line here
      C        Copy current line
      D99----  Delete next 99 lines (also could cut with mouse)
      I999---  Insert 999 blank lines useful when autoadd is set
      IB55---  Insert 55 lines before
      C3-----  Copy next three lines to some target
      A000102  Target for line copy or include file (copy after)
      B000102  Target for line copy or include file (copy before)
      M------  Move this line somewhere
      M3-----  Move next 3 lines somewhere
      O3-----  Move source lines over these lines
      R3-----  Replicate the next 3 lines

      DD00103  Block delete   CC00103  Block Copy    MM00103  Block Move
      0000104                 0000104                0000104
      DD-----                 CC-----                MM-----

      OO00103  Target Over    RR3----  Block Replicate
      0000104                 0000104
      OO-----                 RR-----

      (4-----  Shift left first 4 columns into bit bucket (distructive shift)
      )4-----  Shift right first 4 columns (distructive shift)
      >5-----  Nondistructive shift right
      <5-----  Nondistructive shift left
      >>5----  Non distructive shift right of a block of commands
      0000101
      0000102
      >>-----
      <<,)),(( Similar to single character versions
      UC----- Upper case line  - more useful on function key as :UC
      UC26--- Upper case next 26 lines
      LC----- Lower case line
      LC26    Lower case next 26 lines
      LLC---- Block of lines -lower caSE
      UUC
      TF----- Text flow lines until blank line
      TS----- Text split at cursor better on function key as :tf
      MASK - BUILD TEMPLATE FOR ENTERING DATA


       no need to look up a P-Value or probit
       put this on any command line
       %put %sysfunc(probnorm(1.96)); /* try this on command line  0.975 */
       %put %sysfunc(probit(.95)); /* 1.64 */


       ?          - previous command history IMPORTANT - asked SAS many years ago to add history

       subtop     - submit top line of editor
       subtop n   -submit top n lines
       bounds 1 64 -
       icon
       rchange    - change on function key hit
       rfind      - find on function key hit
       save  prg       /# save program in your profile  ie pgm.source #/
       copy  prg       /# recalls program from your profile #/
       change     - c today yesterday ic all   ( ignore case all)
       cols
       reset
       keys
       top
       bot
       n           - go to line n
       left  n
       right  n
       spell all - check spelling of all words in editor
       autoadd   - add aline at a time to editor ( usewith mask and bounds )
       vscroll 25 - set scroll amounts for forward and backward
       hscroll 10
       backward max n
       forward max  n
       bounds
       mask
       copy
       paste
       find - f 'data' first last next prev prefix suffix word
       find 'Mac' prefix
       change - c todat yesterday ic all
       rchange - change on function key hit
       rfind   - find on function key hit
       mark - highlight string, lines for submit or edit
       mark block - highlight rectangle within editor
                    does not have to be full lines
       JR
       JL
       JJR
       JJL
       JJC

    Mastering a few more commands greatly increases the complexity of what you can do within the text editor.
    Several commands enable you to justify text. Specify the JL (justify left) command to
    left justify, the JR (justify right) command to right justify, and the JC (justify center)
    command to center text. To justify blocks of text, use the JJL, JJR, and JJC commands. For example, if you want to center the following text,

    scripting

       store    * disabled in all future editors (load and store are critical instructions)
       zoom z
       up 2
       down 4
       CAPS on/off
       home
       cursor
       curpos
       nums on/off
       %let
       vt
       pmenu off /# functon key #/
       pmenu on
       end
       print
       submit
       unmark unmark all
       tabs
       redo
       undo cntrl z
       nums on/off
       keys
       fse
       fsv sashelp.class
       fsb

       libn
       filen
       dir
       vt
       print
       copy profile.it.source profile.it1.source

    If you have classic SAS then you have an operating system
    (enhanced and super enhanced editors do not an operating system)

       Interative proc and UIs

       %input
       %window
       window
       proc pmenu
       proc fslist
       proc fsprowse
       proc fsletter
       proc fsedit




       Example 1 -- Just a dumb script
       --------------------------------

       1;F ' ';MARK;HOME;2;HOME;MARK;HOME;STORE;HOME;UNMARK;

       If the first line in active editor contains

       000001 %Macro MyLongMacroName

       This script will put MyLongMacroName into the paste buffer.
       You can then paste MyLongMacroName anywhere you want.
       (This only works on windows). Try it, just copy
       the one line script to the command line.
       
    CHINSERT     Toggles insert mode.                                                                 
    CURSORDOWN   Moves the cursor down.                                                               
    CURSORLEFT   Moves the cursor left.                                                               
    CURSORRIGHT  Moves the cursor right.                                                              
    CURSORUP     Moves the cursor up.                                                                 
    DELCHAR      Deletes the character at the cursor location.                                        
    DELLINE      Deletes all characters on the current line.                                          
    DELPCHAR     Deletes the character to the left of the cursor.                                     
    DELTOEOL     Deletes all characters to the end of the line.                                       
    DELWORD      Deletes the word under the cursor.                                                   
                 KP_NUMERIC Puts the application keypad into numeric mode.                            
                 Numeric mode is convenient to use in data entry where numbers are involved.          
                 The KP_APPLICATION command returns the keypad to application mode,                   
                 so that the keypad keys resume their functionality listed in the KEYS window.        
                 You can issue this command from the command line.                                    
    MOVEBOL      Moves to the beginning of the line.                                                  
    MOVEEOL      Moves to the end of the line.                                                        
    NEWLINE      If there is a command on the command line, NEWLINE executes it;                      
                 otherwise, the cursor moves to the beginning of the next line                        
                 (equivalent to a carriage return).                                                   
    NEXTFIELD    Moves to the next field. This command does not move the cursor                       
                 from the command line; use the HOME (CTRL-F) command to move from the command line.  
    NEXTWORD     Moves to the next word.                                                              
    PREVFIELD    Moves to the previous field. This command does not move the cursor from              
                 the command line; use the HOME (CTRL-F) command to move from the command line.       
    PREVWORD      Moves to the previous word.                                                         


    ADDITIONAL COMMANDS


    AUTOSCROLL
    AWSMAXIMIZE
    AWSMINIMIZE
    AWSRESTORE
    CAPS
    COLOR
    COMMAND
    CUT
    DLGABOUT
    DLGCDIR
    DLGCOLUMNSIZE
    DLGCOLUMNSORT
    DLGCONVERT
    DLGENDR
    DLGFIND
    DLGFONT
    DLGLIB
    DLGLINKS
    DLGOPEN
    DLGPAGESETUP
    DLGPREF
    DLGPRT
    DLGPRTPREVIEW
    DLGPRTSETUP
    DLGREPLACE
    DLGRUN


    DLGSAVE
    DLGSMAIL
    FILE
    FILEOPEN
    FILL
    GSUBMIT
    HOME
    ICON
    INCLUDE
    PMENU
    STORE
    SUBTOP
    TOOLCLOSE
    TOOLEDIT
    TOOLLARGE
    TOOLLOAD
    TOOLSWITCH
    TOOLTIPS
    WATTACH
    WATTENTION
    WAUTOSAVE
    WBROWSE
    WCOPY
    WCUT
    WDOCKVIEW
    WDOCKVIEWMINIMIZE


    WDOCKVIEWRESIZE
    WDOCKVIEWRESTORE
    WEDIT
    WEMAILFMT
    WEXITSAVE
    WFILE
    WHIDECURSOR
    WHSBAR
    WINSERT
    WMENUPOP
    WMRU
    WNAVKEYUNMARK
    WNEWTITLE
    WNEXTEDIT
    WPASTE
    WPGM
    WPOPUP
    WRTFSAVE
    WSCREENTIPS
    WSTATUSLN
    WUNDO
    WVSBAR
    WWINDOWBAR
    ZOOM



    MY FUNCTION KEYS (REQUIRES MX310 MOUSE WITH OVER 20 ACTIONS)
    (there is a newer $29 'logitech mouse' with the same functionality)

    Obs    KEY        LEN    VAL

      1    F1          71    pgm;file &pgm..sas;file c:\ver\&pgm.&_q..sas;%let _q=%eval(0&_q +1);
      2    F2          30    store;note;notesubmit '%avgha'
      3    F3           6    left 3
      4    F4           7    right 3
      5    F5          30    store;note;notesubmit '%dmpa;'
      6    F6          31    store;note;notesubmit '%dmpha;'
      7    F7          67    log;file "./&pgm..log";note zx;notesubmit "%utl_logcurchk(./&pgm);"
      8    F8           5    rfind
      9    F9           7    rchange
     10    F11         33    store;note;notesubmit '%debugha;'
     11    F12         73    ~;;;;/*'*/ *);*};*];*/;/*"*/;%mend;run;quit;%end;end;run;endcomp;%utlfix;
     12    SHF F1      24    note;notesubmit '%dmpa;'
     13    SHF F2      25    note;notesubmit '%lsala;'
     14    SHF F6      67    ~n ? "hil";n=*"PFil Mason";n gt:"Phil";n le:"Phim"; sql - eqt    */
     15    SHF F7      67    ~libname x excel ".xls";proc sql;update x;set y=2;where n="Roger"*/
     16    SHF F8      12    :a;copy box;
     17    SHF F9      12    :a:copy hdr;
     18    SHF F10     70    ~options minoperator;%macro t(x=a)/minoperator;%if &x in (a b c) %then
     19    SHF F11     24    note;notesubmit '%cona;'
     20    SHF F12     31    store;note;notesubmit '%frqva;'
     21    CTL F1      31    store;note;notesubmit '%dmpha;'
     22    CTL F2      32    store;note;notesubmit '%lsalha;'
     23    CTL F3      10    ~available
     24    CTL F11     31    store;note;notesubmit '%conha;'
     25    CTL F12     31    store;note;notesubmit '%cntva;'
     26    ALT F1      30    store;note;notesubmit '%vuha;'
     27    ALT F2      28    vt _last_ colheading=names;"
     28    ALT F3      64    ~proc report data=c nowd named list wrap;columns _all_;run;quit;
     29    ALT F11     31    store;note;notesubmit '%xlsha;'
     30    ALT F12     30    store;note;notesubmit '%unva;'
     31    CTL B        3    :tf
     32    CTL D       10    ~available
     33    CTL E       10    ~available
     34    CTL G        8    note g.g
     35    CTL H        8    note h.h
     36    CTL I        3    :lc
     37    CTL J        3    :uc
     38    CTL K        4    :mcu
     39    CTL L        4    :mcl
     40    CTL M       79    ~proc format;value $a;proc catalog cat=work.formats;modify a.formatc(desc=dea);
     41    CTL Q        9    ~aailable
     42    CTL R       11    wattention;
     43    CTL T       73    ~proc tabulate data=class;class sex age;table age,sex*(n pctn<age>)/rts=8
     44    CTL U       80    ~do until(last.s);set c;by s;a+ag;end;do until(last.s);set c;by s;output;end;a=0
     45    CTL W       10    ~available
     46    CTL Y       34    ~where name like "B_B" "%B%" "B%B"
     47    RMB         53    log;clear;out;clear;pgm;submit;home;rec;home;log;z;z;
     48    SHF RMB     25    note;notesubmit '%ls40a;'
     49    CTL RMB     32    store;note;notesubmit '%ls40ha;'
     50    MMB         13    ~mapped to F1
     51    SHF MMB     17    ~mapped to shf F1
     52    CTL MMB     17    ~mapped to ctl F1


