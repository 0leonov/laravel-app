## Kas ir API?
API (Application Programming Interface) ir noteikumu, protokolu un rīku kopums, kas ļauj dažādām programmatūrām savstarpēji sazināties. API var būt web serviss, bibliotēka vai jebkāda cita forma, kas ļauj vienai programmatūrai pieprasīt un apmainīties ar datiem ar citu programmatūru. API sniedz standartizētu veidu, kā integrēt ārējas funkcijas vai datus, nerakstot visu funkcionalitāti no jauna.

  

## Kā deklarēt mainīgo PHP valodā?
PHP valodā mainīgais tiek deklarēts, sākot ar "$", aiz kuras seko mainīgā nosaukums. Mainīgā nosaukums nevar sākties ar ciparu un var ietvert burtus, ciparus un apakšsvītras. PHP ir "loosely typed" valoda, kas nozīmē, ka mainīgā tipu nav jādefinē ekspliciti. Mainīgā tipu nosaka tā vērtība piešķiršanas brīdī.

  

##  Kādu arhitektūru izmanto Laravel, paskaidro kā tā strādā.
Laravel izmanto MVC (Model-View-Controller) arhitektūru. MVC ir dizaina modelis, kas nodala aplikācijas datu loģiku (Model), lietotāja interfeisu (View) un kontroles loģiku (Controller), veicinot koda organizāciju un atkārtotu izmantošanu.

  

- Model - pārstāv aplikācijas datu struktūru, parasti mijiedarbojas ar datu bāzi un satur funkcijas datu saglabāšanai, izgūšanai, atjaunināšanai un dzēšanai.

- View - atbild par datu vizualizāciju un lietotāja saskarni. Skatā tiek attēlots informācija, ko nosūtījis kontrolieris.

- Controller - apstrādā lietotāja pieprasījumus, saņem datus no modeļiem, veic nepieciešamās apstrādes un nosūta datus uz skatiem.

  

## Kas ir ORM, kāpēc to izmanto tīra SQL vietā?
ORM (Object-Relational Mapping) ir programmēšanas tehnikas, kas ļauj kartēt objektu orientētās programmēšanas valodas klases uz datubāzes tabulām. ORM ļauj izstrādātājiem strādāt ar datiem kā ar objektiem, un tā automātiski rūpējas par SQL pieprasījumu izveidi, izpildi un rezultātu konvertēšanu atpakaļ objektos.

Laravel izmanto Eloquent kā savu ORM sistēmu, kas ļauj viegli mijiedarboties ar datu bāzēm, izmantojot objektu metodes un īpašības.

ORM izmantošanas ieguvumi salīdzinājumā ar tīra SQL izmantošanu ietver:

- Produktivitāte un Ātrums
- Drošība
- Uzturamība
- Datubāzes neatkarība
- Objektu un relāciju atspoguļojums
- Automatizācija

## Uzraksti Eloquent ORM pieprasījumu modelim User, kur nepieciešams iegūt visus lietotājus kuriem reitings ir lielāks par 4.
```php
$users = User::where('rating', '>', 4)->get();
```