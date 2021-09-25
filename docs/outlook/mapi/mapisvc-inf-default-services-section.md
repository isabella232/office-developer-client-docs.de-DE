---
title: Abschnitt "MapiSvc.inf [Default Services]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e99fec901bac6f72ac1ded4934896fd3869e89b6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595756"
---
# <a name="mapisvcinf-default-services-section"></a>Abschnitt "MapiSvc.inf [Default Services]

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Abschnitt **[Standarddienste]** listet alle Nachrichtendienste auf, die als Standardnachrichtendienste ausgewählt sind. Diese Standardnachrichtendienste sind eine Teilmenge der Nachrichtendienste, die im Abschnitt **[Dienste]** aufgeführt sind. Wenn ein Profilkonfigurationsprogramm ein Standardprofil erstellt, werden die Nachrichtendienste in diesem Abschnitt automatisch einbezogen. 
  
Die Einträge verwenden dasselbe Format wie einträge im Abschnitt **[Dienste]** wie folgt: 
  
 **[Standarddienste]**
  
 _Name des Nachrichtendienstabschnitts_  =   _Name des Nachrichtendiensts_
  
Die folgenden Einträge würden im Abschnitt **[Standarddienste]** für die in der vorherigen Abbildung dargestellte mapisvc.inf enthalten sein: 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


