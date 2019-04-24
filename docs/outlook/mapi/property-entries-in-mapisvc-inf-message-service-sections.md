---
title: Eigenschafts Einträge in den Nachrichtendienst Abschnitten von MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ad2732f2f8dba4f506318a1b6faefb617a60584a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328518"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a>Eigenschafts Einträge in den Nachrichtendienst Abschnitten von MapiSvc. inf

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einträge, die Eigenschaften festlegen, verwenden dieses Format:
  
 **Property-Tag** **=** Eigenschaftswert 
  
Bei dem Property-Tag kann es sich um ein Standardmäßiges MAPI-Eigenschafts handeln, wenn die Konfigurationsdaten eine der von MAPI vordefinierten Eigenschaften darstellen, oder ein nicht standardmäßiges Tag, wenn die Daten keine MAPI-Eigenschaft darstellt. Das Nonstandard-Tag wird durch Kombinieren des Werts für einen Eigenschaftenbezeichner mit einem Eigenschaftentyp erstellt. Das Ergebnis ist eine achtstellige Hexadezimalzahl. Der Eigenschaftswert kann für das Property-Tag sinnvoll sein. 
  
Nachrichtendienst Abschnitte können eine Vielzahl von Einträgen in Abhängigkeit vom konfigurierten Nachrichtendienst enthalten. Die folgenden MAPI-Eigenschaften sind in der Regel in einem Abschnitt für Nachrichtendienste im aufgeführten Format enthalten:
  
 **PR_DISPLAY_NAME** =  -_Zeichenfolge_
  
 **PR_SERVICE_DLL_NAME** =  _Name der DLL-Datei_
  
 **PR_SERVICE_ENTRY_NAME** =  _Name der Einstiegspunktfunktion_
  
 **PR_SERVICE_SUPPORT_FILES** =  _-Liste der Dateien_
  
 **PR_SERVICE_DELETE_FILES** =  _-Liste der Dateien_
  
 **PR_RESOURCE_FLAGS** =  __ -Bitmaske
  
Die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Zeichenfolge ist der Name des Nachrichtendiensts, der auf der Benutzeroberfläche angezeigt wird, der Name, den der Benutzer dem Nachrichtendienst zuordnet. Der Anzeigename ist ein optionaler Eintrag in MAPISVC. inf. Manchmal besteht der Anzeigename aus zwei Teilen; ein vom Nachrichtendienst zugewiesenes Teil und ein vom Benutzer zugewiesenes Teil. Wenn der Benutzer für die Zuweisung eines der Teile verantwortlich ist, wird dies in der Regel mit einem speziellen Dialogfeld behandelt, das als Eigenschaftenblatt bezeichnet wird, das vom Nachrichtendienst unter der Steuerung einer Clientanwendung bereitgestellt wird. 
  
Die für den **PR_SERVICE_DLL_NAME** ([pidtagservicedllname (](pidtagservicedllname-canonical-property.md)) bereitgestellten Informationen sind der Name der dll, die den Nachrichtendienst enthält. Die Informationen für den **PR_SERVICE_ENTRY_NAME** ([pidtagserviceentryname (](pidtagserviceentryname-canonical-property.md)) sind der Name der Einstiegspunktfunktion innerhalb der dll, die MAPI zum Konfigurieren des Nachrichtendiensts aufruft. 
  
Bei den im **PR_SERVICE_SUPPORT_FILES** ([pidtagservicesupportfiles (](pidtagservicesupportfiles-canonical-property.md)) aufgeführten Dateien handelt es sich um Dateien, die mit dem Nachrichtendienst installiert werden müssen. Entsprechend müssen die Dateien im **PR_SERVICE_DELETE_FILES** ([pidtagservicedeletefiles (](pidtagservicedeletefiles-canonical-property.md))-Eintrag entfernt werden, wenn der Nachrichtendienst entfernt wird. 
  
Der **PR_RESOURCE_FLAGS** ([pidtagresourceflags (](pidtagresourceflags-canonical-property.md))-Eintrag ist eine Sammlung von Optionen, die für den Nachrichtendienst definiert sind. Beispielsweise wird das SERVICE_SINGLE_COPY-Bit festgelegt, wenn der Nachrichtendienst nur einmal in einem bestimmten Profil angezeigt werden kann. Das SERVICE_NO_PRIMARY_IDENTITY-Bit wird festgelegt, wenn der Nachrichtendienst keine Identitätsinformationen bereitstellt. 
  
Es folgen zwei Beispiele für nicht standardmäßige Eigenschafts Einträge. Der erste Eintrag gibt den Pfad zu der Datei an, die vom Standardadressbuch als Eigenschaftswert verwendet wird. der zweite Eintrag gibt einen numerischen Eigenschaftswert an. Beide Einträge haben eine bestimmte Bedeutung für den AB-Nachrichtendienst.
  
```cpp
6600001e=full path to file
66040003=integer

```


