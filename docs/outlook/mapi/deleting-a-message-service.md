---
title: Löschen eines Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f39f721d434f4e54cbfa5d25a3ba626858f2b13e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583568"
---
# <a name="deleting-a-message-service"></a>Löschen eines Nachrichtendiensts

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
 **So löschen Sie eine Message Service aus einem Profil**
  
1. Rufen Sie **IMAPISession::GetMsgServiceTable** die Tabelle der Dienste für den Zugriff auf. 
    
2. Suchen Sie die Zeile für den Dienst, und übergeben Sie die Spalte **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) im Parameter _Lpuid_ an [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md). 
    
 **DeleteMsgService** Ruft die Messagingdiensts Eintrag Point-Funktion mit dem _UlContext_ -Parameter auf MSG_SERVICE_DELETE festgelegt. Message-Dienste Ausführen von Aufgaben zu diesem Zeitpunkt aus, bevor sie aus dem Profil entfernt werden. 
  

