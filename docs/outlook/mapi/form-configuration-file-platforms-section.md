---
title: Abschnitt "Formularkonfigurationsdatei [Plattformen]
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7439de5b91cefe89eba2f9395595d4a7c8ca3ec5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419128"
---
# <a name="form-configuration-file-platforms-section"></a>Abschnitt "Formularkonfigurationsdatei [Plattformen]

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Im **Abschnitt [Plattformen]** wird der vollständige Satz von Plattformen aufgeführt, die von diesem Formular unterstützt werden. Jeder Plattformeintrag besteht aus dem Präfix **Plattform.** _string_, wobei  _string_ ein beliebiger Zeichenfolgencode für die Plattform ist. Jede Zeichenfolge entspricht dem **CPU-Eintrag** eines einzelnen **[Platforms]-Abschnitts.** Jeder Eintrag in einem **Abschnitt [Plattformen]** definiert eine  _Plattformzeichenfolge,_ die auf eine nachfolgende **[Plattform] verweist.** _Platform string_ **]** section, wie hier gezeigt. 
  
Im **Abschnitt [Plattformen]** wird der vollständige Satz von Plattformen aufgeführt, die von diesem Formular unterstützt werden. Jeder Plattformeintrag besteht aus dem Präfix **Plattform.** _string_, wobei  _string_ ein beliebiger Zeichenfolgencode für die Plattform ist. Jede Zeichenfolge entspricht dem **CPU-Eintrag** eines einzelnen **[Platforms]-Abschnitts.** Jeder Eintrag in einem **Abschnitt [Plattformen]** definiert eine  _Plattformzeichenfolge,_ die auf eine nachfolgende **[Plattform] verweist.** _Platform string_ **]** section, wie hier gezeigt. 
  
**[Plattformen]**
  
**Plattform**. _string_  =   _Plattformzeichenfolge_
  
Im Folgenden finden Sie ein Beispiel für einen **Abschnitt [Plattformen].** 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

Jede **[Plattform.** _Platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**. Der **CPU-Eintrag** gibt den Prozessor an, und der **OSVersion-Eintrag** gibt das Betriebssystem an. Gültige **CPU-Werte** werden in der folgenden Tabelle beschrieben. 
  
|**CPU-Eintrag**|**Prozessor**|
|:-----|:-----|
|Ix86  <br/> |Intel 80x86- und Pentium-Prozessoren sowie gleichwertige Prozessoren von AMD, Cyrix, NextGen und anderen Herstellern.  <br/> |
|MIPS  <br/> |MIPS R4000-Prozessorreihe.  <br/> |
|AXP  <br/> |Digital Equipment Corporation Alpha AXP-Prozessor.  <br/> |
|PPC  <br/> |Prozessoren der Power -PC-Serie von Motorola.  <br/> |
|M68  <br/> |Prozessoren der Serie "68x00" von "68x00".  <br/> |
   
Gültige **OSVersion-Werte** werden in der folgenden Tabelle beschrieben. 
  
|**OSVersion-Eintrag**|**Betriebssystem**|
|:-----|:-----|
|Win3.1  <br/> |Windows 3.1 und Windows workgroups 3.11.  <br/> |
|WinNT3.5  <br/> |Windows NT 3.5 oder niedriger.  <br/> |
|Win95  <br/> |Windows 95.  <br/> |
|WinNT4.0  <br/> |Windows NT 4.0.  <br/> |
|Mac7  <br/> |Macintosh System 7.  <br/> |
   
Darüber hinaus die **[Plattform.** _platform string_ **]** section must contain either a **File** or **LinkTo** entry. Der **Eintrag Datei** listet die ausführbare Datei der Formularserveranwendung auf, die von der Formularbibliothek verwaltet und beim Starten des Formulars in ein neues Unterverzeichnis im Datenträgercache geladen wird. Wenn stattdessen **ein LinkTo-Eintrag** verwendet wird, enthält er den Namen einer anderen Plattformzeichenfolge, aus der die **Dateiinformationen** übernommen werden. Dies ist hilfreich, wenn eine Version eines Formulars mehrere Plattformen unterstützt. 
  
Der **Registrierungseintrag** wird immer dann verwendet, wenn der Eintrag **Datei** verwendet wird. Er identifiziert den Registrierungsschlüssel für die Formularbibliothek, in der die ausführbare Datei für die Formularserveranwendung gespeichert ist. Zeichenfolgen, denen ein umgekehrter Schrägstrich ( \ ) vorangehen, werden am Stamm der Registrierung platziert. Zeichenfolgen, denen kein umgekehrter Schrägstrich vorangegangen ist, werden im HKEY_CLASSES_ROOT\CLSID\  _GUID_\ Registrierungsschlüssel platziert, wobei  _GUID_ die **GUID** des Formulars ist. Die Zeichen "%d" können verwendet werden, um den Pfadnamen des Verzeichnisses anzugeben, aus dem die Formularkonfigurationsdatei gelesen wurde. Dies ist hilfreich, um andere Dateien mit Pfadnamen relativ zur Formularkonfigurationsdatei anzugeben. **Mehrere Datei-** **oder Registrierungseinträge** können mithilfe von Datei oder Registrierung als Präfix gefolgt von einem beliebigen anderen Text angegeben werden. Das Format für **die [Plattform.** _platform string_ **]** section is: 
  
- **[Plattform.** _Plattformzeichenfolge_ **]**
    
- **CPU**  =   _string_
    
- **OSVersion**  =   _string_
    
- **Datei**  =   _path_
    
- **LinkTo**  =   _string_
    
- **Registrierung**  =   _string_
  
Im Folgenden finden Sie zwei Beispiele **[Plattform.** _Platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry. 
  
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

Die **[Plattform.** _Der_ Abschnitt plattformzeichenfolge **]** wird beim Hinzufügen eines Formulars zur lokalen Formularbibliothek ignoriert, wenn davon ausgegangen wird, dass das Installationsprogramm die Dateien, die den Nachrichtenklassenhandler bilden, in den verfügbaren lokalen Speicher wie im Abschnitt des Handlers in der OLE-Registrierung benannt platziert hat und die OLE-Registrierung in der Registrierung des Systems durchgeführt hat. 
  

