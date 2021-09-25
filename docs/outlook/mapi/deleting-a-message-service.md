---
title: Löschen eines Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2ad38e1d5fb483956a387e3b6e001479d7153545
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605048"
---
# <a name="deleting-a-message-service"></a>Löschen eines Nachrichtendiensts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So löschen Sie einen Nachrichtendienst aus einem Profil**
  
1. Rufen Sie **IMAPISession::GetMsgServiceTable** auf, um auf die Nachrichtendiensttabelle zuzugreifen. 
    
2. Suchen Sie die Zeile für den Nachrichtendienst, und übergeben Sie die **spalte PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) im  _Parameter lpuid_ an [IMsgServiceAdmin::D eleteMsgService](imsgserviceadmin-deletemsgservice.md). 
    
 **DeleteMsgService** ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, wobei der  _ulContext-Parameter_ auf MSG_SERVICE_DELETE festgelegt ist. Nachrichtendienste führen zu diesem Zeitpunkt alle Bereinigungsaufgaben aus, bevor sie aus dem Profil entfernt werden. 
  

