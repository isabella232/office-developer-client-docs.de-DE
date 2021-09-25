---
title: Abschnitt "MapiSvc.inf [Services] "
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 226465baa7b66e8d3453435b62c70445d66420a8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604740"
---
# <a name="mapisvcinf-services-section"></a>Abschnitt "MapiSvc.inf [Services] "

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Abschnitt **[Dienste]** listet die Nachrichtendienste auf, die auf einem Computer installiert sind. Die Einträge in diesem Abschnitt verwenden das folgende Format: 
  
 **[Dienste]**
  
 _Name des Nachrichtendienstabschnitts_  =   _Name des Nachrichtendiensts_
  
Der Name des Nachrichtendienstabschnitts ist eine vom Nachrichtendienst definierte Zeichenfolge, die diesen Eintrag mit einem entsprechenden Abschnitt für den Dienst an anderer Stelle in mapisvc.inf verknüpft. Der Name des Nachrichtendiensts ist der Name des installierten Diensts. Der folgende Abschnitt zeigt drei Nachrichtendienste: das Standardadressbuch, "My Own Service" und den Nachrichten-Store-Dienst. Diese Dienste sind nur zu Veranschaulichungszwecken fiktiver Art. Jeder Nachrichtendienst-Implementierer ersetzt den entsprechenden Eintrag für seinen Nachrichtendienst in diesem Abschnitt.
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

Jeder Eintrag in diesem Abschnitt verfügt über einen eigenen Abschnitt, in dem Informationen für den Nachrichtendienst gespeichert werden. Der entsprechende Abschnitt für das Standardadressbuch heißt z. B. [AB].
  

