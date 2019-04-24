---
title: Starten eines Formular Servers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a439e75a-92b3-4830-9dfc-e723d046be7b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: dec8706ba00356660ec82c25e0213ef3e638691d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270049"
---
# <a name="launching-a-form-server"></a>Starten eines Formular Servers

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Reihe von Interaktionen, die auftreten, wenn ein Formular aus einem persistenten Speicher (also aus einer Formularbibliothek) geladen wird, um eine Meldung anzuzeigen, lautet wie folgt:
  
1. Der Messaging-Client ruft Nachrichtenklasse, Nachrichtenkennzeichen und Nachrichtenstatus der Nachricht ab. Dieser Schritt ist optional; Wenn diese Datenteile in Schritt 2 nicht bereitgestellt werden, werden Sie vom Formular-Manager abgerufen.
    
2. Der Messaging Client ruft [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) mit der Zielnachricht auf. 
    
3. Der Formular-Manager lädt den Formularserver aus der entsprechenden Formularbibliothek. Wenn der Formularserver für die Zielnachricht nicht installiert ist, werden auch die ausführbaren Dateien des Formulars vom Formular-Manager installiert.
    
4. Der Formular-Manager ruft [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) für das Form-Objekt auf, um die Schnittstellen [IMAPIForm: IUnknown](imapiformiunknown.md) und [IPersistMessage: IUnknown](ipersistmessageiunknown.md) des Form-Objekts abzurufen. 
    
5. Der Formular-Manager ruft [IPersistMessage:: Laden](ipersistmessage-load.md) mit dem Nachrichten Standort und den Nachrichten Schnittstellen vom Viewer-Objekt auf. 
    
6. Das Form-Objekt ruft zurück zur [IMAPIMessageSite:: GetSiteStatus](imapimessagesite-getsitestatus.md) -Methode des Messagingclients auf. 
    
7. Der Formular-Manager ruft die [IMAPIForm::](imapiform-setviewcontext.md) setviewcontext-Methode des Form-Objekts mit der Kontext Schnittstelle View des Messagingclients auf. 
    
8. Das Form-Objekt ruft zurück zur [IMAPIViewContext:: SetAdviseSink](imapiviewcontext-setadvisesink.md) -Methode des Messagingclients auf. 
    
9. Das Form-Objekt ruft zurück zur [IMAPIViewContext:: GetViewStatus](imapiviewcontext-getviewstatus.md) -Methode des Messagingclients auf. 
    
10. Der Messaging-Client ruft die [IMAPIForm:: Advise](imapiform-advise.md) -Methode des Form-Objekts mit den Ansichtskontext Schnittstellen des Viewer-Objekts und des Message-websiteobjekts auf. 
    
11. Der Messaging Client ruft die [IMAPIForm::D overb](imapiform-doverb.md) -Methode des Form-Objekts auf. 
    
12. Das Form-Objekt erstellt die Benutzeroberfläche, falls erforderlich, und interagiert mit dem Benutzer.
    
## <a name="see-also"></a>Siehe auch



[Formular Server interAktionen](form-server-interactions.md)

