---
title: Hinzufügen eines Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 30cbe49eae7b4a232efb544c7a508a36b326c6b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407235"
---
# <a name="adding-a-message-service"></a>Hinzufügen eines Nachrichtendiensts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So fügen Sie einem Profil einen neuen Nachrichtendienst hinzu und greifen auf den neuen Nachrichtendienst zu**
  
Rufen [Sie IMsgServiceAdmin2::CreateMsgServiceEx auf.](imsgserviceadmin2-createmsgserviceex.md) **CreateMsgServiceEx** führt die folgenden Aufgaben aus: 
  
1. Kopiert alle relevanten Informationen für den Nachrichtendienst, der sich im MAPISVC befindet. INF-Datei, erstellen Sie einen Profilabschnitt für jeden Anbieterabschnitt.
    
2. Ruft die Einstiegspunktfunktion des Nachrichtendiensts **MSGSERVICEENTRY** auf, und der  _ulContext-Parameter_ ist auf MSG_SERVICE_CREATE. 
    
3. Legt die #A0 des Nachrichtendiensts **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) fest und ruft sie ab.
    
 **So greifen Sie auf einen neu hinzugefügten Nachrichtendienst zu**
  
1. Rufen [Sie IMsgServiceAdmin::GetMsgServiceTable auf,](imsgserviceadmin-getmsgservicetable.md) um die Nachrichtendiensttabelle abzurufen. 
    
2. Rufen Sie die [IMAPITable::Advise-Methode](imapitable-advise.md) der Nachrichtendiensttabelle auf, um sich für Tabellenbenachrichtigungen zu registrieren. 
    
3. Wenn MAPI eine TABLE_ROW_ADDED sendet, suchen Sie den Eintragsbezeichner des neu hinzugefügten Nachrichtendiensts in der [SRow-Struktur,](srow.md) die in der TABLE_NOTIFICATION [ist.](table_notification.md) 
    

