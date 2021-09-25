---
title: Abschnitt "Form Configuration File [Platforms]
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bda35253d091433fccc69de9b73fd58fa2b3b058
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621073"
---
# <a name="form-configuration-file-platforms-section"></a>Abschnitt "Form Configuration File [Platforms]

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Abschnitt **[Plattformen]** enthält den vollständigen Satz von Plattformen, die von diesem Formular unterstützt werden. Jeder Plattformeintrag besteht aus dem Präfix **"Plattform".** _zeichenfolge_, wobei  _Zeichenfolge_ ein beliebiger Zeichenfolgencode für die Plattform ist. Jede Zeichenfolge entspricht dem **CPU-Eintrag** eines einzelnen **[Platforms]-Abschnitts.** Jeder Eintrag in einem **[Platforms]-Abschnitt** definiert eine  _Plattformzeichenfolge,_ die auf eine nachfolgende **[Plattform] verweist.** _Platform string_ **]** section as shown here. 
  
Der Abschnitt **[Plattformen]** enthält den vollständigen Satz von Plattformen, die von diesem Formular unterstützt werden. Jeder Plattformeintrag besteht aus dem Präfix **"Plattform".** _zeichenfolge_, wobei  _Zeichenfolge_ ein beliebiger Zeichenfolgencode für die Plattform ist. Jede Zeichenfolge entspricht dem **CPU-Eintrag** eines einzelnen **[Platforms]-Abschnitts.** Jeder Eintrag in einem **[Platforms]-Abschnitt** definiert eine  _Plattformzeichenfolge,_ die auf eine nachfolgende **[Plattform] verweist.** _Platform string_ **]** section as shown here. 
  
**[Plattformen]**
  
**Plattform**. _zeichenfolge_  =   _Plattformzeichenfolge_
  
Nachfolgend sehen Sie ein Beispiel für einen **Abschnitt [Plattformen].** 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

Jede **[Plattform.** _Platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**. Der **CPU-Eintrag** gibt den Prozessor und der **OSVersion-Eintrag** das Betriebssystem an. Gültige **CPU-Werte** werden in der folgenden Tabelle beschrieben. 
  
|**CPU-Eintrag**|**Prozessor**|
|:-----|:-----|
|Ix86  <br/> |Prozessoren der Intel 80x86- und Derm-Serie sowie entsprechende Prozessoren von AMD, Cyrix, NextGen und anderen Anbietern.  <br/> |
|MIPS  <br/> |MiPS R4000-Prozessoren der Serie.  <br/> |
|AXP  <br/> |Digital Equipment Corporation Alpha AXP-Prozessor.  <br/> |
|PPC  <br/> |Prozessoren der Power PC-Serie  <br/> |
|M68  <br/> |Prozessoren der Serie "68x00".  <br/> |
   
Gültige **OSVersion-Werte** werden in der folgenden Tabelle beschrieben. 
  
|**OSVersion-Eintrag**|**Betriebssystem**|
|:-----|:-----|
|Win3.1  <br/> |Windows 3.1 und Windows für Arbeitsgruppen 3.11.  <br/> |
|WinNT3.5  <br/> |Windows NT 3.5 oder niedriger.  <br/> |
|Win95  <br/> |Windows 95.  <br/> |
|WinNT4.0  <br/> |Windows NT 4.0.  <br/> |
|Mac7  <br/> |Macintosh System 7.  <br/> |
   
Darüber hinaus die **[Plattform.** _Platform string_ **]** section must contain either a **File** or **LinkTo** entry. Der **Dateieintrag** listet die ausführbare Datei der Formularserveranwendung auf, die die Formularbibliothek verwaltet und beim Starten des Formulars in ein neues Unterverzeichnis im Datenträgercache lädt. Wenn stattdessen ein **LinkTo-Eintrag** verwendet wird, enthält er den Namen einer anderen Plattformzeichenfolge, aus der die **Dateiinformationen** entnommen werden. Dies ist nützlich, wenn eine Version eines Formulars mehrere Plattformen unterstützt. 
  
Der **Registrierungseintrag** wird immer dann verwendet, wenn der **Dateieintrag** verwendet wird, er identifiziert den Registrierungsschlüssel für die Formularbibliothek, in der die ausführbare Datei für die Formularserveranwendung gespeichert ist. Zeichenfolgen, denen ein umgekehrter Schrägstrich ( \ ) vorangestellt ist, werden im Stammverzeichnis der Registrierung platziert. Zeichenfolgen, denen kein umgekehrter Schrägstrich vorangestellt ist, werden im registrierungsschlüssel HKEY_CLASSES_ROOT\CLSID\  _GUID\_ platziert, wobei  _GUID_ die **GUID** des Formulars ist. Die Zeichen "%d" können verwendet werden, um den Pfadnamen des Verzeichnisses anzugeben, aus dem die Formularkonfigurationsdatei gelesen wurde. Dies ist nützlich, um andere Dateien mit Pfadnamen relativ zur Formularkonfigurationsdatei anzugeben. **Mehrere Datei-** oder **Registrierungseinträge** können mithilfe von Datei oder Registrierung als Präfix gefolgt von einem beliebigen anderen Text angegeben werden. Das Format für die **[Plattform.** _Plattformzeichenfolge_ **]** Abschnitt ist: 
  
- **[Plattform.** _Plattformzeichenfolge_ **]**
    
- **CPU**  =   _zeichenfolge_
    
- **OSVersion**  =   _zeichenfolge_
    
- **Datei**  =   _Pfad_
    
- **LinkTo**  =   _zeichenfolge_
    
- **Registrierung**  =   _zeichenfolge_
  
Im Folgenden sind zwei Beispiele **für [Platform.** _Platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry. 
  
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

Die **[Plattform.** _Platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files behandlungs the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry. 
  

