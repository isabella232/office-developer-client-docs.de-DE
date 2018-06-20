---
title: Hinzufügen eines Dienstes Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a7735be5cfb8ff0716b6bd6eba4951563bb938ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791249"
---
# <a name="adding-a-message-service"></a>Hinzufügen eines Dienstes Nachricht

  
  
**Betrifft**: Outlook 
  
 **Zum Hinzufügen eines neuen Nachricht-Diensts zu einem Profil und Zugreifen auf den neuen Dienst**
  
Rufen Sie [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md). **CreateMsgServiceEx** führt die folgenden Aufgaben: 
  
1. Kopiert alle relevanten Informationen für den Dienst, der in die Datei MAPISVC ist. INF-Datei, Erstellen eines Profils Abschnitts für jede Anbieterabschnitt.
    
2. Ruft die Messagingdiensts Eintrag Punktfunktion **MSGSERVICEENTRY**, mit dem _UlContext_ -Parameter auf MSG_SERVICE_CREATE festgelegt. 
    
3. Legt fest, und die Messagingdiensts **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))-Eigenschaft abruft.
    
 **Greifen Sie auf alle Dienste neu hinzugefügte Nachricht**
  
1. Rufen Sie [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) zum Abrufen der Tabelle der Dienste. 
    
2. Rufen Sie die Nachricht Service Tabelle [IMAPITable::Advise](imapitable-advise.md) -Methode für die Tabelle Benachrichtigungen registriert. 
    
3. Wenn MAPI TABLE_ROW_ADDED Benachrichtigung sendet, suchen Sie die Eintrags-ID des neu hinzugefügten Nachricht-Diensts in der [SRow](srow.md) -Struktur, die in der Struktur [TABLE_NOTIFICATION](table_notification.md) enthalten. 
    

