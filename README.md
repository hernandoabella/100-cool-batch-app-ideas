# 100+ 😎 cool batch apps!
Collection of applications to practice Batch code

Get it on Amazon (SOON) ✅ 


## Batch Calculator
![FH8V08TFHEJ18S5](https://github.com/hernandoabella/100-cool-batch-apps/assets/24196857/84d6c538-cbd4-4241-a690-9e232923b935)

This is...well... a calculator.
just copy and paste into NOTEPAD and save as calculator.bat
the filename is not important but the extension MUST be saved as " .bat "

```
@echo off
title Batch Calculator by seJma
color 1f
:top
echo --------------------------------------------------------------
echo Welcome to Batch Calculator by seJma
echo --------------------------------------------------------------
echo.
set /p sum=
set /a ans=%sum%
echo.
echo = %ans%
echo --------------------------------------------------------------
pause
cls
echo Previous Answer: %ans%
goto top
pause
exit
```


## Folder Protector
This is pretty cool as it requests a password for a folder.
Once you copy it into notepad you must insert your own password and designated folder directory into the designated areas!
NB: THERE ARE TWO PLACES IN WHICH YOU MUST ENTER INFO!!!

```
@echo off
title Folder Password v1.5
color 0a
set /a tries=3
set password=***ENTER YOUR PASSWORD HERE***
:top
echo.
echo ----------------------------------------------
echo.
echo Folder Password
echo.
echo ----------------------------------------------
echo You have %tries% attempts left.
echo Enter password
echo ----------------------------------------------
set /p pass=
if %pass%==%password% (
goto correct
)
set /a tries=%tries -1
if %tries%==0 (
goto penalty
)
cls
goto top
:penalty
echo Sorry, too many incorrect passwords, initiating shutdown.
start shutdown -s -f -t 35 -c "SHUTDOWN INITIATED"
pause
exit
:correct
cls
echo ----------------------------------------------
echo Password Accepted!
echo.
echo Opening Folder...
echo ----------------------------------------------
explorer ***ENTER FOLDER PATH HERE***
pause
```

*NOTE: This is not an advanced piece of software, it does not hide or block the destination folder or anything like that so don't get your hopes up.
**Yes, it can now open files with spaces, just use a backslash (\) when typing your filepath.

## Guessing Game
This is a game in which the computer generates a random number, and you must try to guess it.

```
@echo off
color 0e
title Guessing Game by seJma
set /a guessnum=0
set /a answer=%RANDOM%
set variable1=surf33
echo -------------------------------------------------
echo Welcome to the Guessing Game!
echo.
echo Try and Guess my Number!
echo -------------------------------------------------
echo.
:top
echo.
set /p guess=
echo.
if %guess% GTR %answer% ECHO Lower!
if %guess% LSS %answer% ECHO Higher!
if %guess%==%answer% GOTO EQUAL
set /a guessnum=%guessnum% +1
if %guess%==%variable1% ECHO Found the backdoor hey?, the answer is: %answer%
goto top
:equal
echo Congratulations, You guessed right!!!
echo.
echo It took you %guessnum% guesses.
echo.
pause

```

*Note: For the backdoor, type "surf33"

## Site Selector
This is an application that lets you select from a list of sites.
Feel free to add some of your own sites.

```
@echo off
color 2f
title Site Selector by seJma
:top
echo ***************************************************************
echo.
echo Site Selector
echo.
echo ***************************************************************
echo.
echo Key: [1] Google - Search Engine
echo [2] Hotmail - Mail Server
echo [3] Yahoo - Search Engine/Mail Server
echo [4] Facebook - Social Networking
echo [5] Myspace - Social Networking
echo [6] CNN - News
echo [7] Weather - Weather
echo [8] WikiHow - A How-To Website
echo [9] Instructables - A How-To Website
echo [10] YouTube - Online Videos
echo [11] Answers - Online Encyclopedia
echo [12] Wikipedia - Online Encyclopedia
echo.
echo [e] Exit
echo.
echo ***************************************************************
echo Enter the number of the website which you would like to go to:
echo.
set /p udefine=
echo.
echo ***************************************************************
if %udefine%==1 start www.google.com
if %udefine%==2 start www.hotmail.com
if %udefine%==3 start www.yahoo.com
if %udefine%==4 start www.facebook.com
if %udefine%==5 start www.myspace.com
if %udefine%==6 start www.cnn.com
if %udefine%==7 start www.weather.com
if %udefine%==7 start www.wikihow.com
if %udefine%==9 start www.instructables.com
if %udefine%==10 start www.youtube.com
if %udefine%==11 start www.answers.com
if %udefine%==12 start www.wikipedia.com
if %udefine%==e goto exit

cls
echo ***************************************************************
echo.
echo Thank You for using Site Selector by seJma
echo.
echo ***************************************************************
echo Type [e] to exit or [b] to go back and select another site.
echo.
set /p udefine=
echo.
echo ***************************************************************
if %udefine%==b goto top
if %udefine%==e goto exit
:exit
cls
echo ***************************************************************
echo.
echo Thank You for using Site Selector by SEjMA
echo.
echo ***************************************************************
pause
exit
```

## Fake Virus
This is a fake virus that I designed, it looks pretty convincing if you put it in someone's startup folder.
NB: this batch starts a "60 second till shutdown" script when its done. to abort shutdown click START>RUN:shutdown -a
NB: this does not do anything harmful or destructive to your computer.

***NEW: I've added an extra command that disables themes to make it look more realistic.

```
@echo off
color 47
net stop themes >nul
title DEEP VIRAL INFECTION!
echo VIRAL INFECTION!!!
echo VIRAL INFECTION!!!
echo VIRAL INFECTION!!!
echo ERROR!!!
echo -
echo virus - TROJAN_DEMOLISHER code #45643676
echo -
echo FIREWALL - FAILED
echo -
echo ANTI-VIRUS - FAILED
echo -
echo IP ADDRESS BREACHED!
echo -
echo VIRUS ATTAINING: ****-****-****-8894
echo -

pause
cls
echo -
echo SCANNING INFECTED AREAS...
echo -

pause

set /a num=0
:repeat1
set /a num=%num% +1
echo %num%
if %num%==100 goto end
goto repeat1
:end
cls
echo -
echo 86.5 PERCENT OF MEMORY INFECTED
echo -
echo INFECTION FATAL!
echo -
echo DELETION OF ENTIRE CONTENTS OF LOCAL DISK C: REQUIRED
echo -

pause
cls
echo -
echo DELETING HARD-DRIVE C:
echo -
dir /s

pause
cls
echo -
echo CONTENTS OF HARD-DRIVE C: ERASED
echo -

pause
cls
echo -
echo SCANNING...
echo -

set /a num1=0
:repeat2
set /a num1=%num1% +1
echo %num1%
if %num1%==100 goto end1
goto repeat2
:end1
cls
echo -
echo 0.00 PERCENT OF HARD-DRIVE INFECTED
echo -
pause

echo ERROR
echo ERROR
echo ERROR
echo ERROR
echo ERROR
echo ERROR
echo ERROR
echo ERROR
echo ERROR
echo ERROR
echo ERROR
echo ERROR
echo ERROR
echo ERROR
echo ERROR
echo ERROR
echo ERROR
echo ERROR
echo ERROR

pause
cls
title SYSTEM FAILURE
color 17
echo ERROR!
echo -
echo VISUAL MEMORY LOST!
echo -
echo RAM LOST!
echo -
echo CORE PROCESSOR FAILING...
echo -
echo TOTAL SYSTEM CRASH IMMINENT!
echo -
echo -

pause
cls
echo -
echo -
echo -
echo SHUTDOWN COMPUTER NOW TO AVOID RISK OF FIRE!
echo -
echo -
echo -

pause
cls
echo -
echo -
echo -
echo SEEK PROFESSIONAL HELP IMMEDIATLY TO PREVENT FURTHER DAMAGE!
echo -
echo -
echo -
pause
start shutdown -s -t 60 -c "SYSTEM FAILURE<SHUTTING DOWN TO AVOID FURTHER DAMAGE!"
**NB: Type "shutdown -a" in your Run box to abort a system shutdown
***Type "net start themes" to in your Run box to get the themes service working
```

## Random Password Generator
This script generates a random password of a specified length (in this case, 12 characters). It uses a set of characters (uppercase letters, lowercase letters, numbers, and symbols) defined in the chars variable. The password is displayed on the screen and can be used for various purposes where a secure password is needed.
```
@echo off
setlocal enabledelayedexpansion

set "chars=ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*()_+-=[]{}|;:,.<>/?"
set "length=12"
set "password="

:generate
set /a rand=%random% %% 94
set "password=!password!!chars:~%rand%,1!"
set /a length-=1
if %length% gtr 0 goto generate

echo Generated Password: %password%
pause
exit

```

## Countdown Timer
This script will count down from a user-specified number of seconds.

```
@echo off
title Countdown Timer
color 4f
setlocal enabledelayedexpansion
:top
echo --------------------------------------------------------------
echo Welcome to Countdown Timer by seJma
echo --------------------------------------------------------------
echo.
set /p time=Enter the number of seconds to count down:
echo.
:countdown
if %time% LEQ 0 goto done
set /a time=%time% - 1
echo Time remaining: %time% seconds
timeout /t 1 >nul
goto countdown
:done
echo Time's up!
echo --------------------------------------------------------------
pause
cls
goto top
pause
exit

```

## To-Do List Manager
This script allows you to add, view, and remove tasks from a to-do list.
```
@echo off
title To-Do List Manager by seJma
color 2f
setlocal enabledelayedexpansion

set "file=todolist.txt"

:init
if not exist %file% echo.>%file%

:menu
cls
echo --------------------------------------------------------------
echo To-Do List Manager by seJma
echo --------------------------------------------------------------
echo [1] View To-Do List
echo [2] Add a Task
echo [3] Remove a Task
echo [4] Exit
echo --------------------------------------------------------------
set /p choice=Choose an option (1-4):

if %choice%==1 goto view
if %choice%==2 goto add
if %choice%==3 goto remove
if %choice%==4 goto exit
goto menu

:view
cls
echo --------------------------------------------------------------
echo To-Do List
echo --------------------------------------------------------------
type %file%
echo --------------------------------------------------------------
pause
goto menu

:add
cls
echo --------------------------------------------------------------
echo Add a Task
echo --------------------------------------------------------------
set /p task=Enter the task description:
echo %task%>>%file%
echo Task added!
pause
goto menu

:remove
cls
echo --------------------------------------------------------------
echo Remove a Task
echo --------------------------------------------------------------
type %file%
echo --------------------------------------------------------------
set /p linenum=Enter the line number of the task to remove:
set /a linenum=linenum-1

for /f "tokens=1* delims=:" %%a in ('findstr /n "^" %file%') do (
    if %%a neq %linenum% echo.%%b>>tempfile.txt
)

move tempfile.txt %file% >nul
echo Task removed!
pause
goto menu

:exit
exit
```

## Stopwatch
This script allows you to start, stop, and reset a stopwatch.

```
@echo off
title Stopwatch by seJma
color 5f
setlocal enabledelayedexpansion

set "starttime="
set "endtime="
set /a elapsed=0

:menu
cls
echo --------------------------------------------------------------
echo Stopwatch by seJma
echo --------------------------------------------------------------
echo [1] Start
echo [2] Stop
echo [3] Reset
echo [4] Exit
echo --------------------------------------------------------------
set /p choice=Choose an option (1-4):

if %choice%==1 goto start
if %choice%==2 goto stop
if %choice%==3 goto reset
if %choice%==4 goto exit
goto menu

:start
cls
echo --------------------------------------------------------------
echo Stopwatch Started
echo --------------------------------------------------------------
set "starttime=%time%"
echo Press any key to return to menu...
pause >nul
goto menu

:stop
cls
echo --------------------------------------------------------------
echo Stopwatch Stopped
echo --------------------------------------------------------------
set "endtime=%time%"

for /f "tokens=1-4 delims=:.," %%a in ("%starttime%") do (
    set /a st_hours=%%a
    set /a st_minutes=%%b
    set /a st_seconds=%%c
    set /a st_centiseconds=%%d
)

for /f "tokens=1-4 delims=:.," %%a in ("%endtime%") do (
    set /a et_hours=%%a
    set /a et_minutes=%%b
    set /a et_seconds=%%c
    set /a et_centiseconds=%%d
)

set /a elapsed_hours=et_hours - st_hours
set /a elapsed_minutes=et_minutes - st_minutes
set /a elapsed_seconds=et_seconds - st_seconds
set /a elapsed_centiseconds=et_centiseconds - st_centiseconds

if %elapsed_centiseconds% lss 0 (
    set /a elapsed_centiseconds+=100
    set /a elapsed_seconds-=1
)
if %elapsed_seconds% lss 0 (
    set /a elapsed_seconds+=60
    set /a elapsed_minutes-=1
)
if %elapsed_minutes% lss 0 (
    set /a elapsed_minutes+=60
    set /a elapsed_hours-=1
)

echo Elapsed Time: %elapsed_hours% hours, %elapsed_minutes% minutes, %elapsed_seconds% seconds, %elapsed_centiseconds% centiseconds
echo Press any key to return to menu...
pause >nul
goto menu

:reset
cls
set "starttime="
set "endtime="
set /a elapsed=0
echo Stopwatch Reset
echo Press any key to return to menu...
pause >nul
goto menu

:exit
exit

```

