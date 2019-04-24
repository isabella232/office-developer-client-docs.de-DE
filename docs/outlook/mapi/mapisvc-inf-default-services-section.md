---
title: Abschnitt "MapiSvc. inf [Standarddienste]"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a7906a9a5e953332dba5c4776c63bb433a937a5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270070"
---
# <a name="mapisvcinf-default-services-section"></a>Abschnitt "MapiSvc. inf [Standarddienste]"

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Im Abschnitt **[Default Services]** werden alle Nachrichtendienste aufgelistet, die als Standardnachrichten Dienste ausgewählt werden. Diese Standardnachrichten Dienste sind eine Teilmenge der Nachrichtendienste, die im Abschnitt **[Dienste]** aufgeführt sind. Wenn ein Profil Konfigurationsprogramm ein Standardprofil erstellt, werden die Nachrichtendienste in diesem Abschnitt automatisch eingeschlossen. 
  
Die Einträge verwenden dasselbe Format wie Einträge im Abschnitt **[Dienste]** , wie nachfolgend gezeigt: 
  
 **[Standarddienste]**
  
 _Message-Service section Name_ =  _Message Service Name_
  
Die folgenden Einträge würden im Abschnitt **[Default Services]** für die in der vorherigen Abbildung gezeigte MAPISVC. inf enthalten sein: 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


