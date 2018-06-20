---
title: Abschnitt MapiSvc.inf [Default Services]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5d860135d846df8ef1ea0784d7430c71ad0fe64e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793149"
---
# <a name="mapisvcinf-default-services-section"></a>Abschnitt MapiSvc.inf [Default Services]

  
  
**Betrifft**: Outlook 
  
Der Abschnitt **[Default Services]** enthält eine Liste aller Message-Dienste, die als Standard-Nachrichtendienste ausgewählt sind. Diese Standard-Message-Dienste sind eine Teilmenge der Nachricht Dienstleistungen im Abschnitt **[Services]** . Wenn ein Profil Konfigurationsprogramm ein Standardprofil erstellt werden, sind die Message-Dienste in diesem Abschnitt automatisch enthalten. 
  
Die Einträge verwenden das gleiche Format als Einträge im Abschnitt **[Services]** wie folgt dargestellt: 
  
 **[Default Services]**
  
 _Message-Dienst im Abschnittsname_ =  _Dienstname Nachricht_
  
Die folgenden Einträge wären im Abschnitt **[Services Default]** für die in der vorherigen Abbildung gezeigten mapisvc.inf enthalten: 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


