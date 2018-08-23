---
title: Abschnitt [Default Services] in MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a7270bce12f6d91dbb5632f739f4644df866924d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573145"
---
# <a name="mapisvcinf-default-services-section"></a>Abschnitt [Default Services] in MapiSvc.inf

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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


