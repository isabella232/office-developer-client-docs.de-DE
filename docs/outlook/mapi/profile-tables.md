---
title: Profiltabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c1cbba4892f571f93aeaeed6d58e11f9b5757686
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591318"
---
# <a name="profile-tables"></a>Profiltabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In der Profiltabelle sind Informationen zu allen Profilen aufgeführt, die einer bestimmten Clientanwendung zugeordnet sind. Es gibt eine Profiltabelle für jede Sitzung, die von der MAPI für die Verwendung durch Clients implementiert wird. 
  
Clients greifen auf die Profiltabelle zu, indem sie die [IProfAdmin::GetProfileTable-Methode](iprofadmin-getprofiletable.md) aufrufen. 
  
Die Profiltabelle ist eine statische Tabelle. Profile, die zum Löschen markiert wurden, sind nicht in der Profiltabelle enthalten.
  
Wie bei den meisten Tabellenimplementierungen wird die Tabelle mit null Zeilen erstellt, wenn **GetProfileTable** aufgerufen wird und dem Client keine Profile zur Verfügung stehen. 
  
Die folgenden Eigenschaften bilden den erforderlichen Spaltensatz in Profiltabellen:
  
 **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

