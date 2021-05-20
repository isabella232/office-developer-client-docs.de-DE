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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bb8699746b3f4207ee70edd4e56d0ec6041beac2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429016"
---
# <a name="imapiviewcontextgetviewstatus"></a>IMAPIViewContext::GetViewStatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft den aktuellen Viewerstatus ab. 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parameter

 _lpulStatus_
  
> [out] Zeiger auf eine Bitmaske mit Flags, die den Status des Viewers bereitstellen. Die folgenden Kennzeichen können festgelegt werden:
    
VCSTATUS_CATEGORY 
  
> Es gibt eine nächste oder vorherige Nachricht in einer anderen Kategorie. 
    
VCSTATUS_DELETE 
  
> Das Formular ermöglicht das Entfernen von Nachrichten. 
    
VCSTATUS_INTERACTIVE 
  
> Das Formular sollte eine Benutzeroberfläche anzeigen. Wenn dieses Kennzeichen nicht festgelegt ist, sollte das Formular die Anzeige einer Benutzeroberfläche auch als Reaktion auf ein Verb unterdrücken, das normalerweise dazu führt, dass eine Benutzeroberfläche angezeigt wird. 
    
VCSTATUS_MODAL 
  
> Das Formular ist modal für den Viewer. 
    
VCSTATUS_NEXT 
  
> Es gibt eine nächste Nachricht in der Ansicht. 
    
VCSTATUS_PREV 
  
> In der Ansicht befindet sich eine vorherige Nachricht. 
    
VCSTATUS_READONLY 
  
> Die Nachricht soll im schreibgeschützten Modus geöffnet werden. Lösch-, Absenden- und Verschiebevorgänge sollten deaktiviert sein. 
    
VCSTATUS_UNREAD 
  
> In der Ansicht befindet sich eine nächste oder vorherige ungelesene Nachricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Status des Viewers wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Form-Objekte rufen die **IMAPIViewContext::GetViewStatus-Methode** auf, um zu bestimmen, ob in einer Formularansicht mehr Nachrichten in einer oder beiden Richtungen aktiviert  werden sollen, d. h. in der Richtung, in der ein **Next-Befehl** Nachrichten aktiviert, in der Richtung, in der ein Vorheriger Befehl Nachrichten aktiviert, oder in beide Richtungen. Der Wert, auf den der _lpulStatus-Parameter_ verweist, wird verwendet, um zu bestimmen, ob die Flags VCSTATUS_NEXT und VCSTATUS_PREV für [IMAPIViewContext::ActivateNext gültig sind.](imapiviewcontext-activatenext.md) Wenn das VCSTATUS_DELETE- und nicht das VCSTATUS_READONLY-Flag festgelegt ist, kann die Nachricht mit der [IMAPIMessageSite::D eleteMessage-Methode](imapimessagesite-deletemessage.md) gelöscht werden. 
  
In der Regel deaktivieren Formulare Menübefehle und Schaltflächen, wenn sie nicht für den Kontext des Betrachters gültig sind. Ein Benutzer kann ein Formular auf eine Statusänderung aufmerksam machen, indem er seine [IMAPIFormAdviseSink::OnChange-Methode](imapiformadvisesink-onchange.md) aufruft. 
  
Das VCSTATUS_MODAL wird festgelegt, wenn das Formular modal zu dem Fenster sein muss, dessen Handle im früheren [IMAPIForm::D oVerb-Aufruf](imapiform-doverb.md) übergeben wurde. Wenn VCSTATUS_MODAL festgelegt ist, kann das Formular den Thread verwenden, in dem der **DoVerb-Aufruf** ausgeführt wurde, bis das Formular geschlossen wurde. Wenn VCSTATUS_MODAL nicht festgelegt ist, sollte das Formular nicht modal zu diesem Fenster sein und den Thread nicht verwenden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetViewStatus  <br/> |MFCMAPI implementiert die **IMAPIViewContext::GetViewStatus-Methode** in dieser Funktion.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

