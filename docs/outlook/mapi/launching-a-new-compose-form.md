---
title: Starten eines neuen Formulars zum Verfassen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8d1b94c70e4de6310d2e84cf002c4e3199fced2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792908"
---
# <a name="launching-a-new-compose-form"></a>Starten eines neuen Formulars zum Verfassen

  
  
**Betrifft**: Outlook 
  
Formular Server Implementierer erwarten, dass die folgende Sequenz von Methode von Anrufen an ihre Server Formular und Formularobjekte, wenn eine Clientanwendung öffnet eine neue Nachricht zum Verfassen:
  
1. Die Clientanwendung ruft die [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) -Methode, um die Klasseninformationen zu dem Formular Server Nachrichtenklasse zu erhalten. 
    
2. Die Clientanwendung ruft [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) zum Abrufen eines neuen Formulars-Objekts. 
    
3. MAPI-Formular-Manager lädt der Formular-Server, wenn es nicht bereits im Arbeitsspeicher, und eine [IMAPIForm](imapiformiunknown.md) Schnittstelle aus dem Formular Server ruft. 
    
4. Die Client-Anwendung die resultierende **IMAPIForm** -Schnittstelle und ruft die [QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) -Methode, um das Objekt [IPersistMessage](ipersistmessageiunknown.md) Schnittstelle abrufen. 
    
5. Die Clientanwendung ruft die [IPersistMessage::InitNew](ipersistmessage-initnew.md) -Methode, um das Formularobjekt [IMessage](imessageimapiprop.md), Ansichtskontext, zuordnen und beraten der Empfängerobjekten.
    
6. Die Clientanwendung ruft die [IMAPIForm::DoVerb](imapiform-doverb.md) -Methode, um das Öffnen Verb aufzurufen. 
    
## <a name="see-also"></a>Siehe auch



[Formularserverinteraktionen](form-server-interactions.md)

