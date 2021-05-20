---
title: Eigenschaftseinträge in MapiSvc.inf-Nachrichtendienstabschnitten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ad2732f2f8dba4f506318a1b6faefb617a60584a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427997"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a>Eigenschaftseinträge in MapiSvc.inf-Nachrichtendienstabschnitten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einträge, die Eigenschaften festlegen, verwenden dieses Format:
  
 **Property-Tag** **=** Eigenschaftswert 
  
Das Eigenschaftstag kann ein standardmäßiges MAPI-Eigenschaftstag sein, wenn die Konfigurationsdaten eine der von MAPI vordefinierten Eigenschaften oder ein nicht standardmäßiges Tag darstellen, wenn die Daten keine MAPI-Eigenschaft darstellen. Das nicht standardmäßige Tag wird durch Kombinieren des Werts für einen Eigenschaftenbezeichner mit einem Eigenschaftentyp hergestellt. Das Ergebnis ist eine 8-stellige Hexadezimalzahl. Der Eigenschaftswert kann für das Eigenschaftstag sinnvoll sein. 
  
Nachrichtendienstabschnitte können je nach konfigurierten Nachrichtendienst eine Vielzahl von Einträgen enthalten. Die folgenden MAPI-Eigenschaften sind in der Regel in einem Nachrichtendienstabschnitt im aufgeführten Format enthalten:
  
 **PR_DISPLAY_NAME**  =   _string_
  
 **PR_SERVICE_DLL_NAME**  =   _Name der DLL-Datei_
  
 **PR_SERVICE_ENTRY_NAME**  =   _Name der Einstiegspunktfunktion_
  
 **PR_SERVICE_SUPPORT_FILES**  =   _Liste der Dateien_
  
 **PR_SERVICE_DELETE_FILES**  =   _Liste der Dateien_
  
 **PR_RESOURCE_FLAGS**  =   _bitmask_
  
Die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Zeichenfolge ist der Name des Nachrichtendiensts, der auf der Benutzeroberfläche angezeigt wird, der Name, den der Benutzer dem Nachrichtendienst zuzeigt. Der Anzeigename ist ein optionaler Eintrag in mapisvc.inf. Manchmal besteht der Anzeigename aus zwei Teilen. ein vom Nachrichtendienst zugewiesener Teil und ein vom Benutzer zugewiesener Teil. Wenn der Benutzer für die Zuweisung eines der Teile verantwortlich ist, wird dies in der Regel mit einem speziellen Dialogfeld behandelt, das als Eigenschaftenblatt bezeichnet wird, das vom Nachrichtendienst unter der Kontrolle einer Clientanwendung bereitgestellt wird. 
  
Die Für den Eintrag PR_SERVICE_DLL_NAME **(** [PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) bereitgestellten Informationen ist der Name der DLL, die den Nachrichtendienst enthält. Die informationen für den **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) -Eintrag ist der Name der Einstiegspunktfunktion innerhalb dieser DLL, die MAPI aufruft, um den Nachrichtendienst zu konfigurieren. 
  
Die im Eintrag PR_SERVICE_SUPPORT_FILES **(** [PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) aufgeführten Dateien sind Dateien, die mit dem Nachrichtendienst installiert werden müssen. Ebenso müssen die Dateien im **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) entfernt werden, wenn der Nachrichtendienst entfernt wird. 
  
Der **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) ist eine Auflistung von Optionen, die für den Nachrichtendienst definiert sind. Beispielsweise wird das SERVICE_SINGLE_COPY festgelegt, wenn der Nachrichtendienst nur einmal in einem bestimmten Profil angezeigt werden kann. Das SERVICE_NO_PRIMARY_IDENTITY bit wird festgelegt, wenn der Nachrichtendienst keine Identitätsinformationen zur Verfügung stellt. 
  
Es folgen zwei Beispiele für nicht standardmäßige Eigenschaftseinträge. Der erste Eintrag gibt den Pfad zu der Datei an, die vom Standardadressenbuch als Eigenschaftswert verwendet wird. Der zweite Eintrag gibt einen numerischen Eigenschaftswert an. Beide Einträge haben eine bedeutungsspezifische Bedeutung für den Ab-Nachrichtendienst.
  
```cpp
6600001e=full path to file
66040003=integer

```


