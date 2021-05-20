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
ms.openlocfilehash: 27c20242417e51886ab184b1cc87d6ebb185e4bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428123"
---
# <a name="deleting-a-message-service"></a>Löschen eines Nachrichtendiensts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So löschen Sie einen Nachrichtendienst aus einem Profil**
  
1. Rufen **Sie IMAPISession::GetMsgServiceTable auf,** um auf die Nachrichtendiensttabelle zu zugreifen. 
    
2. Suchen Sie die Zeile für den **Nachrichtendienst, und** übergeben Sie die spalte PR_SERVICE_UID ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) im  _lpuid-Parameter_ an [IMsgServiceAdmin::D eleteMsgService](imsgserviceadmin-deletemsgservice.md). 
    
 **DeleteMsgService** ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, der  _ulContext-Parameter_ ist auf MSG_SERVICE_DELETE. Nachrichtendienste führen zu diesem Zeitpunkt alle Bereinigungsaufgaben aus, bevor sie aus dem Profil entfernt werden. 
  

