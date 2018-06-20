---
title: Profil Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 84c2d02da840dfcad077462954cb10894ba153d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795309"
---
# <a name="profile-tables"></a>Profil Tabellen

  
  
**Betrifft**: Outlook 
  
Die Benutzerprofildienst-Tabelle enthält Informationen über alle Profile, die mit einer bestimmten Clientanwendung verknüpft ist. Es wird eine Profiltabelle für jede Sitzung für die Verwendung durch Clients von MAPI implementiert. 
  
Clientzugriff durch Aufrufen der [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) -Methode die Benutzerprofildienst-Tabelle. 
  
Die Benutzerprofildienst-Tabelle ist eine statische Tabelle. Profile, die zum Löschen gekennzeichnet wurden, sind nicht in der Profiltabelle enthalten.
  
Als wird mit den meisten Tabelle Implementierungen, wenn **"GetProfileTable"** aufgerufen wird und es keine Profile an den Client sind, die Tabelle mit null Zeilen erstellt. 
  
Die folgenden Eigenschaften bilden die erforderliche Spalte im Profil Tabellen festzulegen:
  
 **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

