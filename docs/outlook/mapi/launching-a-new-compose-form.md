---
title: Starten eines neuen Verfassenformulars
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 29d53ba1242014a501a01d161c19dade164f393a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270056"
---
# <a name="launching-a-new-compose-form"></a>Starten eines neuen Verfassenformulars

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Implementierung von Formularservern sollte die folgende Abfolge von Methodenaufrufen an ihre Formularserver und Formularobjekte erwarten, wenn eine Clientanwendung eine neue Nachricht zum Verfassen öffnet:
  
1. Die Clientanwendung ruft die [IMAPIFormMgr::ResolveMessageClass-Methode](imapiformmgr-resolvemessageclass.md) auf, um Klasseninformationen zur Nachrichtenklasse des Formularservers zu erhalten. 
    
2. Die Clientanwendung ruft [IMAPIFormMgr::CreateForm auf,](imapiformmgr-createform.md) um ein neues Formularobjekt zu erhalten. 
    
3. Der MAPI-Formular-Manager lädt den Formularserver, sofern er sich nicht bereits im Arbeitsspeicher befindet, und ruft eine [IMAPIForm-Schnittstelle](imapiformiunknown.md) vom Formularserver ab. 
    
4. Die Clientanwendung verwendet die resultierende **IMAPIForm-Schnittstelle** und ruft die [IUnknown::QueryInterface-Methode](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) auf, um die [IPersistMessage-Schnittstelle](ipersistmessageiunknown.md) des Objekts zu erhalten. 
    
5. Die Clientanwendung ruft die [IPersistMessage::InitNew-Methode](ipersistmessage-initnew.md) auf, um das Formularobjekt [IMessage-](imessageimapiprop.md), Ansichtskontext- und Ratensenkenobjekten zuzuordnen.
    
6. Die Clientanwendung ruft die [IMAPIForm::D oVerb-Methode](imapiform-doverb.md) auf, um das offene Verb auf aufruft. 
    
## <a name="see-also"></a>Siehe auch



[Formularserverinteraktionen](form-server-interactions.md)

