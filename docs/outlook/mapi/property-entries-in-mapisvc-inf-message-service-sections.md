---
title: Eigenschafteneinträge in den Nachrichtendienstabschnitten von MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 038c13d24f3d797f7a4f8f9b7692240ce8004b74
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580334"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a>Eigenschafteneinträge in den Nachrichtendienstabschnitten von MapiSvc.inf

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Verwenden Sie dieses Format Einträge, die Eigenschaften festlegen:
  
 **Eigenschafts-tag** **=** Eigenschaftswert 
  
Das Eigenschafts-Tag kann ein standard MAPI-Eigenschaftentag, wenn die Daten zur Konfiguration der Eigenschaften von MAPI vordefinierten darstellt, oder ein nicht standardmäßigen Tag sein, wenn die Daten keine MAPI-Eigenschaft darstellt. Das nicht standardmäßige Tag erfolgt durch den Wert für einen Eigenschaftenbezeichner mit einen Eigenschaftentyp kombinieren. Das Ergebnis ist eine hexadezimale Zahl 8 Ziffer. Der Eigenschaftswert kann den Inhalt für das Eigenschafts-Tag sinnvoll sein. 
  
Nachricht Service Abschnitte können eine Reihe von Einträgen je nach den konfigurierten Dienst enthalten. Die folgenden MAPI-Eigenschaften sind in der Regel in einer Nachricht im Abschnitt aufgelisteten Format enthalten:
  
 **PR_DISPLAY_NAME** =  _Zeichenfolge_
  
 **PR_SERVICE_DLL_NAME** =  _Name der DLL-Datei_
  
 **PR_SERVICE_ENTRY_NAME** =  _Name des Eintrags-Funktion_
  
 **PR_SERVICE_SUPPORT_FILES** =  _Liste der Dateien_
  
 **PR_SERVICE_DELETE_FILES** =  _Liste der Dateien_
  
 **PR_RESOURCE_FLAGS** =  _Bitmaske_
  
Die Zeichenfolge **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ist der Name des Diensts Nachricht, die in der Benutzeroberfläche, die den Namen angezeigt werden, der der Benutzer die Messagingdiensts zuordnet. Der Anzeigename ist ein optionaler Eintrag in mapisvc.inf. In einigen Fällen wird der Anzeigename aus zwei Teilen bestehen; eine durch den Dienst zugewiesen und einen Teil durch den Benutzer zugewiesen. Wenn der Benutzer für das Zuweisen einer der Teile zuständig ist, erfolgt dies in der Regel mit einem speziellen Dialogfenster bekannt als einem Eigenschaftenfenster bereitgestellt, die vom Nachrichtendienst von einer Clientanwendung aus gesteuert. 
  
Die enthaltenen Informationen für den Eintrag **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) ist der Name der DLL, die den Dienst enthält. Die enthaltenen Informationen für den Eintrag **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) ist der Name der Funktion Eintrag Punkt innerhalb dieser DLL, die MAPI-so konfigurieren Sie den Dienst aufrufen. 
  
Die Dateien in den Eintrag **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) sind Dateien, die mit dem Nachrichtendienst installiert werden müssen. Die Dateien in den Eintrag **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) müssen ebenso entfernt werden, wenn der Nachrichtendienst entfernt wird. 
  
Der Eintrag **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) ist eine Auflistung von Optionen für den Dienst definiert. Beispielsweise wird das Bit SERVICE_SINGLE_COPY festgelegt, wenn der Nachrichtendienst nur einmal in einem bestimmten Profil angezeigt werden kann. Das SERVICE_NO_PRIMARY_IDENTITY Bit ist festgelegt, wenn der Nachrichtendienst nicht Identitätsinformationen bereitstellt. 
  
Führen Sie die beiden Beispiele für nicht standardmäßigen Eigenschafteneinträge. Der erste Eintrag gibt den Pfad zu der Datei durch das Standard-Adressbuch als Wert der Eigenschaft verwendet. der zweite Eintrag gibt den Eigenschaftswert einer numerischen. Beide Einträge haben Bedeutung, die speziell für den Dienst AB.
  
```cpp
6600001e=full path to file
66040003=integer

```


