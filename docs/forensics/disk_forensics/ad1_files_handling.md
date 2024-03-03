# Obsługa plików AD1

Pliki te są obrazami dysku tworzonymi za pomocą programu [FTK Imager](https://www.exterro.com/digital-forensics-software/ftk-imager). Jest to ich własny format pliku. 

Takie pliki można otworzyć jako archiwum, np. za pomocą `7-zip` - potrzebny jest specjalny plugin (np. [Forensic7z](https://www.tc4shell.com/en/7zip/forensic7z/))

Aby można było zawartość takiego pliku przeanalizować np. programem `Autopsy` należy najpierw pliki te wypakować lub wykorzystać plugin [`AD1 Extractor`](https://github.com/markmckinnon/Autopsy-Plugins/tree/master/AD1_Extractor).

???+ warning
    Podczas wypakowywania obrazu dysku należy zachować szczególną ostrożność, ponieważ wiele obrazów dysków zawiera malware, który może zakazić komputer hosta!

Można dodatkowo wykorzystać podejście poprzez obejście problemu: