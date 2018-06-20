---
title: Löschen einer Nachricht-Dienstes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 34d9d6d428f39765e739ce856f3666d07b457d52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791523"
---
# <a name="deleting-a-message-service"></a>Löschen einer Nachricht-Dienstes

  
  
**Betrifft**: Outlook 
  
 **So löschen Sie eine Message Service aus einem Profil**
  
1. Rufen Sie **IMAPISession::GetMsgServiceTable** die Tabelle der Dienste für den Zugriff auf. 
    
2. Suchen Sie die Zeile für den Dienst, und übergeben Sie die Spalte **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) im Parameter _Lpuid_ an [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md). 
    
 **DeleteMsgService** Ruft die Messagingdiensts Eintrag Point-Funktion mit dem _UlContext_ -Parameter auf MSG_SERVICE_DELETE festgelegt. Message-Dienste Ausführen von Aufgaben zu diesem Zeitpunkt aus, bevor sie aus dem Profil entfernt werden. 
  

