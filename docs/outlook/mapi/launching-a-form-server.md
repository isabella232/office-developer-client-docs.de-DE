---
title: Starten eines Formularservers
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
# <a name="launching-a-form-server"></a>Starten eines Formularservers

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Reihe von Interaktionen, die beim Laden eines Formulars aus dem beständigen Speicher (d. h. aus einer Formularbibliothek) zum Anzeigen einer Nachricht auftreten, lautet wie folgt:
  
1. Der Messagingclient ruft die Nachrichtenklasse, Nachrichtenflags und den Nachrichtenstatus der Nachricht ab. Dieser Schritt ist optional. Wenn diese Datenteile nicht in Schritt 2 bereitgestellt werden, ruft der Formular-Manager sie ab.
    
2. Der Messagingclient ruft [IMAPIFormMgr::LoadForm mit](imapiformmgr-loadform.md) der Zielnachricht auf. 
    
3. Der Formular-Manager lädt den Formularserver aus der entsprechenden Formularbibliothek. Wenn der Formularserver für die Zielnachricht nicht installiert ist, installiert der Formular-Manager auch die ausführbaren Dateien des Formulars.
    
4. Der Formular-Manager ruft [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) für das Formularobjekt auf, um die [IMAPIForm - IUnknown-](imapiformiunknown.md) und [IPersistMessage -Schnittstellen](ipersistmessageiunknown.md) des Formularobjekts zu erhalten. 
    
5. Der Formular-Manager ruft [IPersistMessage::Load](ipersistmessage-load.md) mit der Nachrichtenwebsite und nachrichtenschnittstellen aus dem Viewer-Objekt auf. 
    
6. Das Formularobjekt ruft die [IMAPIMessageSite::GetSiteStatus-Methode des Messagingclients](imapimessagesite-getsitestatus.md) zurück. 
    
7. Der Formular-Manager ruft die [IMAPIForm::SetViewContext-Methode](imapiform-setviewcontext.md) des Formularobjekts mit der Ansichtskontextschnittstelle vom Messagingclient auf. 
    
8. Das Formularobjekt ruft die [IMAPIViewContext::SetAdviseSink-Methode des Messagingclients zurück.](imapiviewcontext-setadvisesink.md) 
    
9. Das Formularobjekt ruft die [IMAPIViewContext::GetViewStatus-Methode des Messagingclients](imapiviewcontext-getviewstatus.md) zurück. 
    
10. Der Messagingclient ruft die [IMAPIForm::Advise-Methode](imapiform-advise.md) des Formularobjekts mit den Ansichtskontextschnittstellen des Viewerobjekts und des Nachrichtenwebsiteobjekts auf. 
    
11. Der Messagingclient ruft die [IMAPIForm::D oVerb-Methode des Formularobjekts](imapiform-doverb.md) auf. 
    
12. Das Formularobjekt erstellt bei Bedarf seine Benutzeroberfläche und interagiert mit dem Benutzer.
    
## <a name="see-also"></a>Siehe auch



[Formularserverinteraktionen](form-server-interactions.md)

