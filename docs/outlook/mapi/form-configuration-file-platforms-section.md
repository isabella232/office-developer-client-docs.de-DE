---
title: Abschnitt [Platforms] in der Formularkonfigurationsdatei
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ddc6db2303d9d5f114fdb27b6e15e699a04e73f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791722"
---
# <a name="form-configuration-file-platforms-section"></a>Abschnitt [Platforms] in der Formularkonfigurationsdatei

**Betrifft**: Outlook 
  
Im Abschnitt **[Plattformen]** der vollständigen Satz von Plattformen, die von diesem Formular aufgelistet. Jeder Eintrag Plattform besteht aus dem Präfix **Plattform.** _Zeichenfolge_in der _Zeichenfolge_ eine beliebige Zeichenfolge Code für die Plattform ist. Jede Zeichenfolge entspricht dem Eintrag **CPU** , der eine einzelne Abschnitte **[Plattformen]** . Jeder Eintrag in einem Abschnitt **[Plattformen]** definiert eine _Plattformzeichenfolge_ , die eine nachfolgende verweist auf **[Plattform.** _Plattformzeichenfolge_ **]** Abschnitt wie hier gezeigt. 
  
Im Abschnitt **[Plattformen]** der vollständigen Satz von Plattformen, die von diesem Formular aufgelistet. Jeder Eintrag Plattform besteht aus dem Präfix **Plattform.** _Zeichenfolge_in der _Zeichenfolge_ eine beliebige Zeichenfolge Code für die Plattform ist. Jede Zeichenfolge entspricht dem Eintrag **CPU** , der eine einzelne Abschnitte **[Plattformen]** . Jeder Eintrag in einem Abschnitt **[Plattformen]** definiert eine _Plattformzeichenfolge_ , die eine nachfolgende verweist auf **[Plattform.** _Plattformzeichenfolge_ **]** Abschnitt wie hier gezeigt. 
  
**[Plattformen]**
  
**Plattform**. _Zeichenfolge_ =  _Plattformzeichenfolge_
  
Es folgt ein Beispiel für einen Abschnitt **[Plattformen]** . 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

Jede **[Plattform.** _Plattformzeichenfolge_ **]** Abschnitt enthält zwei erforderliche Einträge **CPU-** und **OSVersion**. Der **CPU** -Eintrag gibt den Prozessor und der Eintrag **OSVersion** gibt das Betriebssystem. Gültige **CPU** -Werte werden in der folgenden Tabelle beschrieben. 
  
|**CPU-Eintrag**|**Prozessor**|
|:-----|:-----|
|Ix86  <br/> |Intel 80 x 86- und Pentium Prozessoren sowie entsprechende Prozessoren von AMD, Cyrix, NextGen und anderer Hersteller.  <br/> |
|MIPS  <br/> |MIPS R4000 Prozessoren.  <br/> |
|AXP  <br/> |Digital Equipment Corporation Alpha AXP Prozessor.  <br/> |
|PPC  <br/> |Motorola Power PC Prozessoren.  <br/> |
|M68  <br/> |Mororola 68 x 00 Prozessoren.  <br/> |
   
Gültige Werte für **OSVersion** werden in der folgenden Tabelle beschrieben. 
  
|**OSVersion-Eintrag**|**Betriebssystem**|
|:-----|:-----|
|Win3.1  <br/> |Windows 3.1 und Windows für Arbeitsgruppen 3.11.  <br/> |
|WinNT3.5  <br/> |Windows NT 3.5 oder unten.  <br/> |
|Windows 95  <br/> |Windows 95.  <br/> |
|WinNT4.0  <br/> |Windows NT 4.0.  <br/> |
|Mac7  <br/> |Macintosh System 7.  <br/> |
   
Darüber hinaus die **[Plattform.** _Plattformzeichenfolge_ **]** Abschnitt muss entweder eine **Datei** oder ein **VerknüpfungMit** Eintrag enthalten. **Der Eintrag in der** listet Formular Server ausführbare Datei der Anwendung, die die Formularbibliothek verwaltet und in ein neues Unterverzeichnis im Datenträgercache geladen, wenn das Formular geöffnet wird. Wenn Sie ein Eintrag **VerknüpfungMit** stattdessen verwendet wird, enthält den Namen einer anderen Plattform-Zeichenfolge, aus der **die Dateiinformationen** entnommen wird. Dies ist nützlich, wenn eine Version eines Formulars mehrere Plattformen unterstützt. 
  
**Der Registrierungseintrag** wird verwendet, wenn **der Eintrag in der** verwendet wird, identifiziert den Registrierungsschlüssel für die Formularbibliothek, in dem die ausführbare Datei für die Server-Anwendung Formular gespeichert ist. Zeichenfolgen, die durch einen umgekehrten Schrägstrich (\) vorangestellt werden am Stamm der Registrierung gespeichert. Zeichenfolgen, die nicht mit einem umgekehrten Schrägstrich vorangestellten befinden sich in der HKEY_CLASSES_ROOT\CLSID\ _GUID_\ Registrierungsschlüssel, wobei _GUID_ die **GUID** des Formulars ist. Die Zeichen "%d" können verwendet werden, an der Pfadname des Verzeichnisses, aus dem Lesen der Konfigurationsdatei Formular. Dies ist hilfreich für andere Dateien mit Pfadnamen relativ zum Formular Konfigurationsdatei angeben. **Mehrere Datei** oder einen **Registrierungsschlüssel** Einträge können mithilfe der Datei oder einen Registrierungsschlüssel als Präfix gefolgt von beliebigen anderen Text angegeben werden. Das Format für die **[Plattform.** _Plattformzeichenfolge_ **]** Abschnitt ist: 
  
- **[-Plattform.** _Plattformzeichenfolge_ **]**
    
- **CPU** =  _Zeichenfolge_
    
- **OSVersion** =  _Zeichenfolge_
    
- **Datei** =  _Pfad_
    
- **VerknüpfungMit** =  _Zeichenfolge_
    
- **Registrierung** =  _Zeichenfolge_
  
Im folgenden werden die beiden Beispiel **[Plattform.** _Plattformzeichenfolge_ **]** Abschnitte, einen **Eintrag in der** Verwendung und mit den Eintrag **VerknüpfungMit** . 
  
```cpp
[Platform.NTx86]
CPU = ix86
OSVersion = WinNT3.5
File = \helpdesk.exe
Registry = Local Server = %d\helpdesk.exe
[Platform.Win95]
CPU = ix86
OSVersion = Win95
LinkTo = NTx86

```

Die **[Plattform.** _Plattformzeichenfolge_ Abschnitt **]** wird ignoriert, wenn ein Formular in der lokalen Formularbibliothek hinzufügen, wenn angenommen wird, dass das Installationsprogramm hat die Dateien in den lokalen Speicher verfügbar den Message-Handler-Klasse darstellt, wie im Abschnitt in der OLE-Registrierung der Ereignishandler mit dem Namen, und wurde ausgeführt die OLE-Registrierung in der Registrierung des Systems. 
  

