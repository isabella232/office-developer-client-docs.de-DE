---
title: Hinzufügen eines Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 90f34379517d8464ce72c8829892f0eb73f321ea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556966"
---
# <a name="adding-a-message-service"></a>Hinzufügen eines Nachrichtendiensts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So fügen Sie einem Profil einen neuen Nachrichtendienst hinzu und greifen auf den neuen Nachrichtendienst zu**
  
Aufrufen [von IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md). **CreateMsgServiceEx** führt die folgenden Aufgaben aus: 
  
1. Kopiert alle relevanten Informationen für den Nachrichtendienst, der sich in MAPISVC befindet. INF-Datei, Erstellen eines Profilabschnitts für jeden Anbieterabschnitt.
    
2. Ruft die Einstiegspunktfunktion des Nachrichtendiensts, **MSGSERVICEENTRY,** auf, wobei der  _ulContext-Parameter_ auf MSG_SERVICE_CREATE festgelegt ist. 
    
3. Legt die **eigenschaft PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) des Nachrichtendiensts fest und ruft sie ab.
    
 **So greifen Sie auf einen neu hinzugefügten Nachrichtendienst zu**
  
1. Rufen [Sie IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) auf, um die Nachrichtendiensttabelle abzurufen. 
    
2. Rufen Sie die [IMAPITable::Advise-Methode](imapitable-advise.md) der Nachrichtendiensttabelle auf, um sich für Tabellenbenachrichtigungen zu registrieren. 
    
3. Wenn MAPI eine TABLE_ROW_ADDED Benachrichtigung sendet, suchen Sie den Eintragsbezeichner des neu hinzugefügten Nachrichtendiensts in der [SRow-Struktur,](srow.md) die in der [TABLE_NOTIFICATION-Struktur](table_notification.md) enthalten ist. 
    

