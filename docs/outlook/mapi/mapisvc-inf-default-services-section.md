---
title: MapiSvc.inf [Default Services] Section
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a7906a9a5e953332dba5c4776c63bb433a937a5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435320"
---
# <a name="mapisvcinf-default-services-section"></a>MapiSvc.inf [Default Services] Section

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Im **Abschnitt [Standarddienste]** werden alle Nachrichtendienste aufgeführt, die als Standardnachrichtendienste ausgewählt sind. Diese Standardnachrichtendienste sind eine Teilmenge der Nachrichtendienste, die im **Abschnitt [Dienste] aufgeführt** sind. Wenn ein Profilkonfigurationsprogramm ein Standardprofil erstellt, werden die Nachrichtendienste in diesem Abschnitt automatisch einbezogen. 
  
Die Einträge verwenden das gleiche Format wie Einträge im **Abschnitt [Dienste],** wie im Folgenden dargestellt: 
  
 **[Standarddienste]**
  
 _Name des Message-Service-Abschnitts_  =   _Name des Nachrichtendiensts_
  
Die folgenden Einträge würden im **Abschnitt [Standarddienste]** für mapisvc.inf in der früheren Abbildung enthalten sein: 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


