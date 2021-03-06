---
title: "Evidence obalů"
author: Autocont
ms.custom: na
ms.date: 02/26/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: dynamics-nav-2018
ms.translationtype: Human Translation
ms.sourcegitcommit: 
ms.openlocfilehash: 
ms.contentlocale: cs-cz
ms.lasthandoff: 03/27/2018

---

# <a name="ac-fp-pack-tracking-basic"></a>Evidence obalů

Modul Evidence obalů je rozšířením modulu Zásoby.
Modul Evidence obalů zakládá samostatnou evidenci obalů svázanou s oblastí zásob a standardními pohyby zboží (nákup, prodej, příjem, výdej, transfer, spotřeba a výroba). 
Modul obsahuje klasifikaci druhů obalů. Umožňuje spravovat libovolný počet podkladů pro potřeby obalového výkaznictví požadovaného interně firmou nebo legislativou (základní parametrizace výkazu EKO-KOM pro potřeby výkaznictví příslušnými osobami dle Zákona o obalech č. 477/2001 Sb. je součástí). 
Položky obalů se vyrovnávají automaticky na pozadí při pohybech zboží, a proto zpracování podkladů pro evidenci obalů uživatele nijak nezatěžuje. Výstupem modulu je tisková sestava Podklad pro výkaz obalů, která poskytuje podklady pro vyplnění vyžadovaných tiskopisů.

## Instalace

**Objekty modulu**

Objekty add-on modulu Evidence obalů jsou označeny verzí **OB4.10** resp. pouze **OB**.
Seznam konkrétních objektů modulu je uveden v dokumentaci k aktuálnímu buildu add-on modulů.

**Další součásti instalace**

Součástí dodávky add-on modulu Evidence obalů je TXT soubor „EKOKOM.txt“ obsahující parametrizaci pro Výkaz obalů EKO-KOM. Textový souboru s parametrizací lze do systému nahrát standardním postupem dataportem 4003500.

## Nastavení

### Nastavení výkazu obalů

Po importu objektů je třeba provést nastavení evidence obalů.
Nastavení se provede v  menu Oblasti/proFINANCE/Evidence obalů.
Pro správnou funkci je nutné při nastavení Evidence obalů provést tyto kroky:
* Založit Výkaz obalů
* Definovat prvky výkazu obalu (definovat strukturu výkazu)
* Založit prvky ve výkazu obalů (definovat vlastní výkaz)
* Založit výjimky ve výkazu obalů
* Na Kartách zboží přiřadit prvky Výkazu obalů
* Zařadit report Podklad pro výkaz obalů do menu Sestavy zboží

V systému lze založit potřebný počet různých Výkazů obalů. Výkazy se založí v menu Oblasti/proFINANCE/Evidence obalů/Výkazy obalů.
Pro každý založený Výkaz obalů je nutno nadefinovat Prvky výkazu obalů. Prvky ve výkazu lze seskupovat do Pozic na výkazu. Celkem lze definovat 10 Pozic (seskupení prvků). Prvky v rámci jedné Pozice mají dále přiřazený Kód.

Pole formuláře Definice prvků výkazu obalů:
* Kód výkazu – kód výkazu založeného v předchozím kroku
* Pozice – uživatelem určená skupina prvků výkazu
* Kód – kód prvku v rámci Pozice
* Popis – popis prvku výkazu
* Umístění ve výkazu – textová popisná informace

Definice vlastního Výkazu se provádí založením prvků výkazu obalů. Ve formuláři se definují jednotlivé řádky výkazu tak, že se vybírají z dříve definovaných Prvků pro jednotlivé pozice výkazu. Pole Kód je systémem dopočítáváno v závislosti na plnění polí Kód pozice.

V každém založeném Výkazu obalů lze definovat výjimky, které nebudou do Výkazu zahrnuty. Výjimka je definována údaji zadanými do polí Číslo pole, Hodnota pole, Pozice (ve výkazu) a Kód prvku.

### Vzorová parametrizace výkazu EKO-KOM

Součástí distribuce modulu je TXT soubor obsahující parametrizaci pro Výkaz obalů EKO-KOM. Textový souboru s parametrizací lze do systému nahrát standardním postupem dataportem 4003500.

### Nastavení karet zboží

Po nastavení Výkazu obalů je nutno na Kartách zboží přiřadit prvky Výkazu obalů.
Přiřazení se provede na příslušných Kartách zboží, tlačítko Prvky výkazu obalů.

Pro každé zboží a jeho měrnou jednotku lze přiřadit libovolný počet prvků výkazů obalů (zařadit zboží do několika výkazů). Přiřazení prvku je vázáno na Kód výkazu a Typ pohybu. Kombinaci těchto hodnot doplňuje Kód určující pozici ve výkazu. Pole Hmotnost je vztaženo k měrné jednotce na řádku výkazu.

## Použití

### Tvorba podkladu pro výkaz obalů

Report Podklad pro výkaz obalů se nachází v nabídce menu Oblasti/proFINANCE/Evidence obalů/Podklad pro výkaz obalů. Slouží jako podklad pro výkaz o produkci obalů pro společnost EKO-KOM, a. s. Uvedená sestava zobrazí podklady pro vyplnění výkazu obalů.
Pokud chceme označit položky jako vykázané, je nutno zatrhnout pole Označit položky a vyplnit pole Číslo výkazu.

## <a name="see-also"></a>Viz také  
[AC Financial Pack](ac-fp-financial-pack.md)