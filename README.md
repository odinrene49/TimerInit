# TimerInit
#include &lt;Sound.au3> Global $count = 0  $aSound = _SoundOpen(@ScriptDir &amp; "\Voorbeeld.mp4") $time = _SoundLength($aSound, 2) _SoundPlay($aSound) $count = TimerInit()  HotKeySet("{esc}", "quit")  While 1     Sleep(10)     If TimerDiff($count) > $time Then         _SoundPlay($aSound)         $count = TimerInit()     EndIf WEnd  Func quit()     Exit EndFunc   ;==>quit
