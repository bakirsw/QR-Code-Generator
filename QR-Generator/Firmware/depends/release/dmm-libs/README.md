# Peripheriebibliothek für das DMM Board
 
Siehe [DMM-Demo](https://teach.emg.ing.tu-bs.de/git/dmm/dmm-demo) für Beispiele
sowie Bootloader und Board-Konfiguration.
 
## PlatformIO
Um die Bibliothek in das Projekt einbinden füge Referenz ins `platformio.ini` 
des Projektes wie folgt ein:
```
[env]
...
lib_deps = 
  git@teach.emg.ing.tu-bs.de:dmm/dmm-libs.git

```

Bei der nächsten Kompilierung mit `pio run` wird die Bibliothek automatisch 
heruntergeladen. Eine Aktualisierung kann mit `pio lib update` erzwungen werden.

Standardmäßig werden die Bibliotheken in einen versteckten Workspace-Ordner 
abgelegt. Will man sich den Quellcode im Projektordner ansehen können 
(empfohlen!), kann ein Ordner innerhalb des Projektes vorgegeben werden:
```
[platformio]
default_envs = release
libdeps_dir = depends
```
In diesem Fall sollte man davon absehen, die automatisch vom PIO 
heruntergeladenen Bibliotheken ins Git des eigenen Projektes einzuchecken.
Es empfiehlt sich in dem Fall `depends` ins `.gitignore` einzufügen.
