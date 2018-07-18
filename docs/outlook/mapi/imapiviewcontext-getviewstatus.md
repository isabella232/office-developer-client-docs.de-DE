---
title: IMAPIViewContextGetViewStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetViewStatus
api_type:
- COM
ms.assetid: 2e5ec914-7171-41ce-a6fe-78dd80ac32ff
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fb543f4188578483333614cb5768f903c9f243d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792524"
---
# <a name="imapiviewcontextgetviewstatus"></a>IMAPIViewContext::GetViewStatus

  
  
**Betrifft**: Outlook 
  
Ruft den aktuellen Status der Viewer ab. 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parameter

 _lpulStatus_
  
> [out] Zeiger auf eine Bitmaske aus Flags, die den Status der Viewer bereitstellen. Die folgenden Kennzeichen können festgelegt werden:
    
VCSTATUS_CATEGORY 
  
> Es ist eine Nachricht nächste oder vorherige in einer anderen Kategorie. 
    
VCSTATUS_DELETE 
  
> Das Formular ermöglicht Nachrichten entfernt werden soll. 
    
VCSTATUS_INTERACTIVE 
  
> Das Formular sollte eine Benutzeroberfläche angezeigt werden. Wenn dieses Flag nicht festgelegt ist, sollte das Formular unterdrückt werden, auch als Antwort auf ein Verb an, die in der Regel eine Benutzeroberfläche anzuzeigende bewirkt, dass eine Benutzeroberfläche anzuzeigen. 
    
VCSTATUS_MODAL 
  
> Das Formular ist für den Betrachter modal. 
    
VCSTATUS_NEXT 
  
> Es ist eine nächste Nachricht in der Ansicht. 
    
VCSTATUS_PREV 
  
> Es ist eine vorherige Nachricht in der Ansicht. 
    
VCSTATUS_READONLY 
  
> Die Nachricht ist im schreibgeschützten Modus geöffnet werden. Löschen Sie, senden Sie, und verschieben Sie Vorgänge deaktiviert werden soll. 
    
VCSTATUS_UNREAD 
  
> Es ist eine nächste oder Vorherige ungelesene Nachricht in der Ansicht.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Zeichnungsanzeige Status wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Formular-Objekte aufrufen, die **IMAPIViewContext::GetViewStatus** -Methode, um zu bestimmen, ob es sind weitere Nachrichten an, die in einer Ansicht des Formulars in einem aktiviert werden, oder beide Richtungen d. h., in die Richtung, in dem ein Befehl **Weiter** aktiviert, Nachrichten in der Richtung, in dem ein **Vorherige** Befehl Nachrichten, aktiviert, oder in beide Richtungen. Der Wert, der auf den durch den Parameter _LpulStatus_ wird verwendet, um festzustellen, ob die Flags VCSTATUS_NEXT und VCSTATUS_PREV für [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)gültig sind. Wenn das Flag VCSTATUS_DELETE Set, aber nicht das Flag VCSTATUS_READONLY ist, kann die Nachricht mit der [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) -Methode gelöscht werden. 
  
Formulare deaktivieren in der Regel Menübefehle und Schaltflächen, wenn sie nicht für den Viewer Kontext gültig sind. Ein Viewer kann ein Formular auf eine Änderung im Status durch Aufrufen der [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) -Methode benachrichtigen. 
  
Das Flag VCSTATUS_MODAL festgelegt ist, wenn das Formular in das Fenster gebunden sein muss, dessen Handle übergeben wird, in den früheren [IMAPIForm::DoVerb](imapiform-doverb.md) -Aufruf. Wenn VCSTATUS_MODAL festgelegt ist, können das Formular Threads auf dem der **DoVerb** -Anruf getätigt wurde, bis das Formular geschlossen wird. Wenn VCSTATUS_MODAL nicht festgelegt ist, wird das Formular nicht modal in diesem Fenster werden und muss nicht den Thread verwenden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetViewStatus  <br/> |MFCMAPI (engl.) implementiert die **IMAPIViewContext::GetViewStatus** -Methode in dieser Funktion.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

