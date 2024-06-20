A mellékelt munkafüzet egy kis segédeszköz audió adatkészlet egyszerűbb előállításához. 
Az alap ötlet a PIPER TTS modellek finomhangolásához a piper-recording-studio-nál egyszerűbb megoldás keresése volt.
A piper-recording-studio nagyon jó eszköz, de a műkődése azaz az, hogy 1150 mondatot kell felolvasni egy jó hang
adatbázis elkészítéséhez, magában hordozza a hibát is, ami az elkészült hangmodelleket, 
illetve azok intonációját természetellenessé teszi. A felolvasás a legtöbb esetben nem a természetes beszéd jegyeit hordozza.

Erre megoldásként arra gondoltam, hogy egy nagyobb, összefüggő hanganyagot kellene feldarabolni. LJSpeech formába önteni.

Használat:
A munkafüzet magában is tartalmazza a Transript str elkészítését, de azt vettem észre, hogy ugyan jó a faster-whisper, 
de az a megvalósítás (https://github.com/Purfview/whisper-standalone-win) pontosabb eredményt ad az alábbi parancscsal:
```
whisper-faster "work_directory" --language=hu --model=large-v2 --beam_size=5 --print_progress --batch_recursive --output_format str
```
Ettől eltekintve csak click click click...

A riport_2_speaker_separator.ipynb használatához a huugingfacen el kell fogadni a pyannote model használatának licensz feltételeit. (első indításnál hibaüzenetben feldobja a konkrét modell elérhetőségét.)
