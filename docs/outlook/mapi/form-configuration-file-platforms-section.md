---
title: Abschnitt "Formular Konfigurationsdatei [Plattformen]"
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7439de5b91cefe89eba2f9395595d4a7c8ca3ec5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327510"
---
# <a name="form-configuration-file-platforms-section"></a>Abschnitt "Formular Konfigurationsdatei [Plattformen]"

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Im Abschnitt **[Plattformen]** wird der vollständige Satz von Plattformen aufgelistet, die von diesem Formular unterstützt werden. Jeder Platt Form Eintrag besteht aus der Präfix **Plattform.** _String_, wobei _String_ ein beliebiger Zeichenfolgen Code für die Plattform ist. Jede Zeichenfolge entspricht dem **CPU** -Eintrag eines einzelnen Abschnitts **[Plattformen]** . Jeder Eintrag in einem Abschnitt **[Plattformen]** definiert eine _Plattformzeichenfolge_ , die auf eine nachfolgende **[Plattform verweist.** _Plattformzeichenfolge_ **]** -Abschnitt wie hier gezeigt. 
  
Im Abschnitt **[Plattformen]** wird der vollständige Satz von Plattformen aufgelistet, die von diesem Formular unterstützt werden. Jeder Platt Form Eintrag besteht aus der Präfix **Plattform.** _String_, wobei _String_ ein beliebiger Zeichenfolgen Code für die Plattform ist. Jede Zeichenfolge entspricht dem **CPU** -Eintrag eines einzelnen Abschnitts **[Plattformen]** . Jeder Eintrag in einem Abschnitt **[Plattformen]** definiert eine _Plattformzeichenfolge_ , die auf eine nachfolgende **[Plattform verweist.** _Plattformzeichenfolge_ **]** -Abschnitt wie hier gezeigt. 
  
**Plattformen**
  
**Plattform**. _Zeichenfolgen_ =  -_Plattformzeichenfolge_
  
Es folgt ein Beispiel für einen Abschnitt **[Plattformen]** . 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

**[Platform.** _Plattformzeichenfolge_ **]** section enthält die beiden erforderlichen Einträge, **CPU** und **OSVersion**. Der **CPU** -Eintrag gibt den Prozessor an, und der **OSVersion** -Eintrag gibt das Betriebssystem an. Gültige **CPU** -Werte werden in der folgenden Tabelle beschrieben. 
  
|**CPU-Eintrag**|**Prozessor**|
|:-----|:-----|
|Ix86  <br/> |Prozessoren der Intel 80x86-und Pentium-Serie sowie äquivalente Prozessoren von AMD, Cyrix, NextGen und anderen Herstellern.  <br/> |
|MIPS  <br/> |MIPS-R4000 Series-Prozessoren.  <br/> |
|AXP  <br/> |Alpha-AXP-Prozessor für digitale Geräte Corporation.  <br/> |
|PPC  <br/> |Motorola Power PC Series-Prozessoren.  <br/> |
|M68  <br/> |Prozessoren der Mororola-68x00-Serie.  <br/> |
   
Gültige **OSVersion** -Werte werden in der folgenden Tabelle beschrieben. 
  
|**OSVersion-Eintrag**|**Betriebssystem**|
|:-----|:-----|
|Win 3.1  <br/> |Windows 3,1 und Windows für Workgroups 3,11.  <br/> |
|WinNT 3.5  <br/> |Windows NT 3,5 oder niedriger.  <br/> |
|Win95  <br/> |Windows 95.  <br/> |
|WinNT 4.0  <br/> |Windows NT 4,0.  <br/> |
|Mac7  <br/> |Macintosh System 7.  <br/> |
   
Darüber hinaus wird die **[-Plattform.** _Plattformzeichenfolge_ **]** -Abschnitt muss entweder einen **Datei** -oder **LinkTo** -Eintrag enthalten. Der **Datei** Eintrag listet die ausführbare Datei der Formularserver Anwendung auf, die von der Formularbibliothek verwaltet und in ein neues Unterverzeichnis im Datenträgercache geladen wird, wenn das Formular gestartet wird. Wenn stattdessen ein **LinkTo** -Eintrag verwendet wird, enthält er den Namen einer anderen Plattformzeichenfolge, von der die **Datei** Informationen entnommen werden. Dies ist nützlich, wenn eine Version eines Formulars mehrere Plattformen unterstützt. 
  
Der **Registrierungs** Eintrag wird verwendet, wenn der **Datei** Eintrag verwendet wird, er identifiziert den Registrierungsschlüssel für die Formularbibliothek, in der die ausführbare Datei für die Formularserver Anwendung gespeichert ist. Zeichenfolgen, denen ein umgekehrter Schrägstrich (\) vorangestellt wird, werden im Stammverzeichnis der Registrierung gespeichert. Zeichenfolgen, denen kein umgekehrter Schrägstrich vorangestellt wird, werden im HKEY_CLASSES_ROOT\CLSID\- _GUID_\-Registrierungsschlüssel gespeichert, wobei _GUID_ die **GUID** des Formulars ist. Die Zeichen "% d" können verwendet werden, um den Pfadnamen des Verzeichnisses anzugeben, aus dem die Formular Konfigurationsdatei gelesen wurde. Dies ist hilfreich, um andere Dateien mit Pfadnamen relativ zur Formular Konfigurationsdatei anzugeben. **Mehrere Datei** -oder **Registrierungs** Einträge können mithilfe von File oder Registry als Präfix gefolgt von einem anderen Text angegeben werden. Das Format für die **[-Plattform.** _Plattformzeichenfolge_ **]** section ist: 
  
- **Plattform.** _Plattformzeichenfolge_ **]**
    
- **CPU** =  -_Zeichenfolge_
    
- **OSVersion** =  -_Zeichenfolge_
    
- **** =  Dateipfad__
    
- **LinkTo** =  -_Zeichenfolge_
    
- **Registrierungs** =  _Zeichenfolge_
  
Es folgen zwei Beispiele **[Platform.** _Plattformzeichenfolge_ **]** Abschnitte, eine mit dem **Datei** Eintrag und einen mithilfe des **LinkTo** -Eintrags. 
  
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

**[Platform.** _Plattformzeichenfolge_ **]** section wird beim Hinzufügen eines Formulars zur lokalen Formularbibliothek ignoriert, wenn davon ausgegangen wird, dass das Installationsprogramm die Dateien, die den Nachrichtenklassen Handler konstituieren, in verfügbaren lokalen Speicher, wie im Handler-Abschnitt in der OLE-Registrierung benannt, gespeichert hat und die OLE-Registrierung in der Systemregistrierung. 
  

