---
title: Eigenschaftseinträge in den Abschnitten des MapiSvc.inf-Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8b6028e3c15f9c42f2fc8ad5672546d7fcf66b20
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599235"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a>Eigenschaftseinträge in den Abschnitten des MapiSvc.inf-Nachrichtendiensts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einträge, die Eigenschaften festlegen, verwenden dieses Format:
  
 **Property-Tag** **=** Eigenschaftswert 
  
Das Eigenschaftstag kann ein standardmäßiges MAPI-Eigenschaftstag sein, wenn die Konfigurationsdaten eine der von der MAPI vordefinierten Eigenschaften darstellen, oder ein nicht standardmäßiges Tag, wenn die Daten keine MAPI-Eigenschaft darstellen. Das nicht standardmäßige Tag wird erstellt, indem der Wert für einen Eigenschaftsbezeichner mit einem Eigenschaftstyp kombiniert wird. Das Ergebnis ist eine achtstellige Hexadezimalzahl. Der Eigenschaftswert kann für das Eigenschaftstag sinnvoll sein. 
  
Nachrichtendienstabschnitte können je nach konfigurierten Nachrichtendienst eine Vielzahl von Einträgen enthalten. Die folgenden MAPI-Eigenschaften sind in der Regel in einem Nachrichtendienstabschnitt im aufgeführten Format enthalten:
  
 **PR_DISPLAY_NAME**  =   _zeichenfolge_
  
 **PR_SERVICE_DLL_NAME**  =   _Name der DLL-Datei_
  
 **PR_SERVICE_ENTRY_NAME**  =   _Name der Einstiegspunktfunktion_
  
 **PR_SERVICE_SUPPORT_FILES**  =   _Liste der Dateien_
  
 **PR_SERVICE_DELETE_FILES**  =   _Liste der Dateien_
  
 **PR_RESOURCE_FLAGS**  =   _Bitmaske_
  
The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) string is the name of the message service that is shown in the user interface, the name that the user associates with the message service. Der Anzeigename ist ein optionaler Eintrag in mapisvc.inf. Manchmal besteht der Anzeigename aus zwei Teilen. ein vom Nachrichtendienst zugewiesener Und ein vom Benutzer zugewiesener Teil. Wenn der Benutzer für die Zuweisung eines der Teile verantwortlich ist, wird dies in der Regel mit einem speziellen Dialogfeld behandelt, das als Eigenschaftenblatt bezeichnet wird, das vom Nachrichtendienst unter der Kontrolle einer Clientanwendung bereitgestellt wird. 
  
Die Informationen für den **Eintrag PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) sind der Name der DLL, die den Nachrichtendienst enthält. Die Informationen für den **Eintrag PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) sind der Name der Einstiegspunktfunktion innerhalb dieser DLL, die MAPI aufruft, um den Nachrichtendienst zu konfigurieren. 
  
Die im **Eintrag PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) aufgeführten Dateien sind Dateien, die mit dem Nachrichtendienst installiert werden müssen. Ebenso müssen die Dateien im **Eintrag PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) entfernt werden, wenn der Nachrichtendienst entfernt wird. 
  
Der **eintrag PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) ist eine Sammlung von Optionen, die für den Nachrichtendienst definiert sind. Beispielsweise wird das SERVICE_SINGLE_COPY Bit festgelegt, wenn der Nachrichtendienst nur einmal in einem bestimmten Profil angezeigt werden kann. Das SERVICE_NO_PRIMARY_IDENTITY Bit wird festgelegt, wenn der Nachrichtendienst keine Identitätsinformationen bereitstellt. 
  
Es folgen zwei Beispiele für nicht standardmäßige Eigenschaftseinträge. Der erste Eintrag gibt den Pfad zu der Datei an, die vom Standardadressbuch als Eigenschaftswert verwendet wird. Der zweite Eintrag gibt einen numerischen Eigenschaftswert an. Beide Einträge haben eine spezifische Bedeutung für den AB-Nachrichtendienst.
  
```cpp
6600001e=full path to file
66040003=integer

```


