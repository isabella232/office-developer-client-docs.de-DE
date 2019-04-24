---
title: Profiltabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 15c07c05af82389bce697c300cd9b1d504e98736
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328560"
---
# <a name="profile-tables"></a>Profiltabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In der Profiltabelle werden Informationen zu allen Profilen aufgelistet, die einer bestimmten Clientanwendung zugeordnet sind. Es gibt eine Profiltabelle für jede Sitzung, die von MAPI zur Verwendung durch Clients implementiert wird. 
  
Clients greifen auf die Profiltabelle zu, indem Sie die [IProfAdmin::](iprofadmin-getprofiletable.md) getprofilable-Methode aufrufen. 
  
Die Profiltabelle ist eine statische Tabelle. Profile, die zum Löschen markiert wurden, sind nicht in der Profiltabelle enthalten.
  
Wie bei den meisten Tabellen Implementierungen **** wird die Tabelle mit null Zeilen erstellt, wenn getprofilable aufgerufen wird und keine Profile für den Client verfügbar sind. 
  
Die folgenden Eigenschaften bilden den erforderlichen Spaltensatz in Profiltabellen:
  
 **PR_DEFAULT_PROFILE** ([Pidtagdefaultprofile (](pidtagdefaultprofile-canonical-property.md)) 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

