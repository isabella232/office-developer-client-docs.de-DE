---
title: Starten eines Formularservers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a439e75a-92b3-4830-9dfc-e723d046be7b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f5f76dd0e17abe53b3666f3f00580cc6af1cdcf0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610377"
---
# <a name="launching-a-form-server"></a>Starten eines Formularservers

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Serie von Interaktionen, die ausgeführt wird, wenn ein Formular aus einem beständigen Speicher (d. a. aus einer Formularbibliothek) geladen wird, um eine Nachricht anzuzeigen, lautet wie folgt:
  
1. Der Messaging-Client ruft die Nachrichtenklasse, die Nachrichtenflags und den Nachrichtenstatus der Nachricht ab. Dieser Schritt ist optional. Wenn diese Datenteile in Schritt 2 nicht bereitgestellt werden, ruft der Formular-Manager sie ab.
    
2. Der Messagingclient ruft [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) mit der Zielnachricht auf. 
    
3. Der Formular-Manager lädt den Formularserver aus der entsprechenden Formularbibliothek. Wenn der Formularserver für die Zielnachricht nicht installiert ist, installiert der Formular-Manager auch die ausführbaren Dateien des Formulars.
    
4. Der Formular-Manager ruft [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) für das Formularobjekt auf, um die [IMAPIForm : IUnknown-](imapiformiunknown.md) und [IPersistMessage : IUnknown-Schnittstellen](ipersistmessageiunknown.md) des Formularobjekts abzurufen. 
    
5. Der Formular-Manager ruft [IPersistMessage::Load](ipersistmessage-load.md) mit der Nachrichtenwebsite und nachrichtenschnittstellen aus dem Viewer-Objekt auf. 
    
6. Das Formularobjekt ruft die [IMAPIMessageSite::GetSiteStatus-Methode](imapimessagesite-getsitestatus.md) des Messagingclients auf. 
    
7. Der Formular-Manager ruft die [IMAPIForm::SetViewContext-Methode](imapiform-setviewcontext.md) des Formularobjekts mit der Ansichtskontextschnittstelle vom Messagingclient auf. 
    
8. Das Formularobjekt ruft die [IMAPIViewContext::SetAdviseSink-Methode](imapiviewcontext-setadvisesink.md) des Messagingclients zurück. 
    
9. Das Formularobjekt ruft die [IMAPIViewContext::GetViewStatus-Methode](imapiviewcontext-getviewstatus.md) des Messagingclients auf. 
    
10. Der Messagingclient ruft die [IMAPIForm::Advise-Methode](imapiform-advise.md) des Formularobjekts mit den Ansichtskontextschnittstellen aus dem Viewer-Objekt und dem Nachrichtenwebsiteobjekt auf. 
    
11. Der Messagingclient ruft die [IMAPIForm::D oVerb-Methode](imapiform-doverb.md) des Formularobjekts auf. 
    
12. Das Formularobjekt erstellt bei Bedarf seine Benutzeroberfläche und interagiert mit dem Benutzer.
    
## <a name="see-also"></a>Siehe auch



[Formularserverinteraktionen](form-server-interactions.md)

