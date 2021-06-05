# FreeCad-3D-Design-2020
FreeCad 3D design kursus i 2020
# Klargør din Ubuntu PC til FreeCAD undervisning
## Biblioteks struktur
### Biblioteks struktur for AppImage
```bash
~/.local/  
~/.local/bin/*.AppImage    
~/.local/share/  
~/.local/share/applications/*.desktop  
~/.local/share/icons/*.png  
```  

### Biblioteks struktur for Arbejdsområde
```  
~/Dokumenter/FreeCad/
~/Dokumenter/FreeCad/FreeCad-Seniorhus-2019-2
```  
## Opret manglende bibliteker
Har du en frisk installation af Ubuntu er to biblioteker som mangler:
* ~/.local/bin
* ~/.local/share/icons  

kopier og kør kommandolinierne her nedenunder, en linje ad gangen, i et terminalvindue.
```bash
mkdir -p ~/.local/bin # -p, no error if existing, make parent directories as needed
PATH="$PATH:$HOME/bin"
mkdir -p ~/.local/share/icons
```  

## Hent Filer
Vi skal hente to filer 
 * AppImage af FreeCad:
   * kilk på denne link:  https://github.com/FreeCAD/FreeCAD/releases/tag/0.19_pre 
   * koppier link som ser ud som denne link:  FreeCAD_0.19-xxxxx-Linux-Conda_glibc2.12-x86_64.AppImage hvor xxxxx er det nyeste release nr.
   * kopier linkadressen
   * åben nu et terninal vindue og indsæt din link som her 
```      
wget https://github.com/FreeCAD/FreeCAD/releases/download/0.19_pre/FreeCAD_0.19-xxxxx-Linux-Conda_glibc2.12-x86_64.AppImage -O ~/.local/bin/FreeCAD_0.19-xxxxx-Linux-Conda_glibc2.12-x86_64.AppImage
```  

 * Icon for til FreeCad
   * wget https://www.norwegiancreations.com/wp-content/uploads/2016/02/2000px-FreeCAD-logo.svg_-350x350.png -O FreeCad_0.19.png

```  
```  


## Føj den aktive brugerkonto til en gruppe dialout
For at have adgang til tty porte skal din bruger konto være medlem af gruppen dialout, det opnås som vist herunder.

```bash
sudo usermod -a -G dialout $USER
```