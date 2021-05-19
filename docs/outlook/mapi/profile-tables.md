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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424350"
---
# <a name="profile-tables"></a>Profiltabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In der Profiltabelle sind Informationen zu allen Profilen aufgeführt, die einer bestimmten Clientanwendung zugeordnet sind. Es gibt eine Profiltabelle für jede Sitzung, die von MAPI zur Verwendung durch Clients implementiert wird. 
  
Clients greifen auf die Profiltabelle zu, indem sie die [IProfAdmin::GetProfileTable-Methode](iprofadmin-getprofiletable.md) aufrufen. 
  
Die Profiltabelle ist eine statische Tabelle. Profile, die zum Löschen markiert wurden, sind nicht in der Profiltabelle enthalten.
  
Wie bei den meisten Tabellenimplementierungen wird die Tabelle mit null Zeilen erstellt, wenn **GetProfileTable** aufgerufen wird und dem Client keine Profile zur Verfügung stehen. 
  
Die folgenden Eigenschaften sind die erforderlichen Spalten, die in Profiltabellen festgelegt sind:
  
 **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

