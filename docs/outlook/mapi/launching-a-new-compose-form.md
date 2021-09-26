---
title: Starten eines neuen Formulars zum Verfassen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 29ad3393340d356a043f5df5115b9112d8e3b3df
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610356"
---
# <a name="launching-a-new-compose-form"></a>Starten eines neuen Formulars zum Verfassen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Formularserver implementers should expect the following sequence of method calls to their form server and form objects when a client application opens a new message for composing:
  
1. Die Clientanwendung ruft die [IMAPIFormMgr::ResolveMessageClass-Methode](imapiformmgr-resolvemessageclass.md) auf, um Klasseninformationen zur Nachrichtenklasse des Formularservers abzurufen. 
    
2. Die Clientanwendung ruft [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) auf, um ein neues Formularobjekt abzurufen. 
    
3. Der MAPI-Formular-Manager lädt den Formularserver, wenn er sich noch nicht im Arbeitsspeicher befindet, und ruft eine [IMAPIForm-Schnittstelle](imapiformiunknown.md) vom Formularserver ab. 
    
4. Die Clientanwendung verwendet die resultierende **IMAPIForm-Schnittstelle** und ruft die [IUnknown::QueryInterface-Methode](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) auf, um die [IPersistMessage-Schnittstelle](ipersistmessageiunknown.md) des Objekts abzurufen. 
    
5. Die Clientanwendung ruft die [IPersistMessage::InitNew-Methode](ipersistmessage-initnew.md) auf, um das Formularobjekt [IMessage-,](imessageimapiprop.md)Ansichtskontext- und Empfehlungssenkenobjekten zuzuordnen.
    
6. Die Clientanwendung ruft die [IMAPIForm::D oVerb-Methode](imapiform-doverb.md) auf, um das geöffnete Verb aufzurufen. 
    
## <a name="see-also"></a>Siehe auch



[Formularserverinteraktionen](form-server-interactions.md)

