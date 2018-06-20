---
title: Starten eines Formulars-Servers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a439e75a-92b3-4830-9dfc-e723d046be7b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c70fd9eb771268db4030cefdf2f27b75ae5963b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792896"
---
# <a name="launching-a-form-server"></a>Starten eines Formulars-Servers

  
  
**Betrifft**: Outlook 
  
Die Reihe von Interaktionen, das auftritt, wenn ein Formular aus dem permanenten Speicher geladen wird (d. h., aus einer Formularbibliothek) zum Anzeigen einer Meldung lautet wie folgt:
  
1. Der messaging-Client Ruft die Nachrichtenklasse, Nachrichtenflags und Nachricht den Status der Nachricht ab. Dieser Schritt ist optional. Wenn dieser Datenelemente nicht in Schritt 2 angegeben werden, wird der Formular-Manager diese abzurufen.
    
2. Der messaging-Client ruft [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) mit der Nachrichten-Ziel. 
    
3. Der Formular-Manager lädt der Formular-Server aus der entsprechenden Formularbibliothek. Wenn der Formular Server für die Zielnachricht nicht installiert ist, wird der Formular-Manager des Formulars ausführbare Dateien als auch installiert.
    
4. Der Formular-Manager ruft [QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) für das Formularobjekt, des Form-Objekts abgerufen [IMAPIForm: IUnknown](imapiformiunknown.md) und [IPersistMessage: IUnknown](ipersistmessageiunknown.md) Schnittstellen. 
    
5. Der Formular-Manager ruft [IPersistMessage::Load](ipersistmessage-load.md) mit der Nachrichten-Website und die Nachricht Schnittstellen aus dem Viewer-Objekt. 
    
6. Das Form-Objekt einen Rückruf an die messaging-Client [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) -Methode. 
    
7. Der Formular-Manager Ruft das Formularobjekt [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) -Methode mit der Ansicht Kontext-Schnittstelle von der messaging-Client. 
    
8. Das Form-Objekt einen Rückruf an die messaging-Client [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) -Methode. 
    
9. Das Form-Objekt einen Rückruf an die messaging-Client [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) -Methode. 
    
10. Der messaging-Client Ruft das Formularobjekt [IMAPIForm::Advise](imapiform-advise.md) -Methode mit der Ansicht Kontext Schnittstellen aus dem Viewer-Objekt und das Objekt "Message" Website. 
    
11. Der messaging-Client Ruft das Formularobjekt [IMAPIForm::DoVerb](imapiform-doverb.md) -Methode. 
    
12. Das Form-Objekt die Benutzeroberfläche erstellt, bei Bedarf, und interagiert mit dem Benutzer.
    
## <a name="see-also"></a>Siehe auch



[Formular Server Interaktionen](form-server-interactions.md)

