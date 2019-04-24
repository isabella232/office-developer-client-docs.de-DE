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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328185"
---
# <a name="adding-a-message-service"></a>Hinzufügen eines Nachrichtendiensts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So fügen Sie einem Profil einen neuen Nachrichtendienst hinzu und greifen auf den neuen Nachrichtendienst zu**
  
Rufen Sie [IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md)auf. **CreateMsgServiceEx** führt die folgenden Aufgaben aus: 
  
1. Kopiert alle relevanten Informationen für den Nachrichtendienst, der sich in der MAPISVC befindet. INF-Datei, Erstellen eines Profil Abschnitts für jeden Anbieterabschnitt.
    
2. Ruft die Einstiegspunktfunktion des Nachrichtendiensts **MSGSERVICEENTRY**auf, wobei der Parameter _ulContext_ auf MSG_SERVICE_CREATE festgelegt ist. 
    
3. Legt die **PR_SERVICE_UID** ([pidtagserviceuid (](pidtagserviceuid-canonical-property.md))-Eigenschaft des Nachrichtendiensts fest und ruft Sie ab.
    
 **So greifen Sie auf einen neu hinzugefügten Nachrichtendienst zu**
  
1. Rufen Sie [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) auf, um die Nachrichtendienst Tabelle abzurufen. 
    
2. Rufen Sie die [IMAPITable:: Advise](imapitable-advise.md) -Methode der Nachrichtendienst Tabelle auf, um Tabellen Benachrichtigungen zu registrieren. 
    
3. Wenn MAPI eine TABLE_ROW_ADDED-Benachrichtigung sendet, suchen Sie den Eintragsbezeichner des neu hinzugefügten Nachrichtendiensts in der [SRow](srow.md) -Struktur, die in der [TABLE_NOTIFICATION](table_notification.md) -Struktur enthalten ist. 
    

