---
title: IMAPIViewContextGetViewStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewContext.GetViewStatus
api_type:
- COM
ms.assetid: 2e5ec914-7171-41ce-a6fe-78dd80ac32ff
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5b8549c2abbad33baf38312f0d803f1f6f3a8244
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579894"
---
# <a name="imapiviewcontextgetviewstatus"></a>IMAPIViewContext::GetViewStatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft den aktuellen Anzeigestatus ab. 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parameter

 _lpulStatus_
  
> [out] Zeiger auf eine Bitmaske mit Flags, die den Status des Viewers bereitstellen. Die folgenden Flags können festgelegt werden:
    
VCSTATUS_CATEGORY 
  
> Es gibt eine nächste oder vorherige Nachricht in einer anderen Kategorie. 
    
VCSTATUS_DELETE 
  
> Das Formular ermöglicht das Entfernen von Nachrichten. 
    
VCSTATUS_INTERACTIVE 
  
> Das Formular sollte eine Benutzeroberfläche anzeigen. Wenn dieses Kennzeichen nicht festgelegt ist, sollte das Formular die Anzeige einer Benutzeroberfläche auch als Reaktion auf ein Verb unterdrücken, das in der Regel bewirkt, dass eine Benutzeroberfläche angezeigt wird. 
    
VCSTATUS_MODAL 
  
> Das Formular ist für den Betrachter modal. 
    
VCSTATUS_NEXT 
  
> Es ist eine nächste Meldung in der Ansicht vorhanden. 
    
VCSTATUS_PREV 
  
> Es ist eine vorherige Meldung in der Ansicht vorhanden. 
    
VCSTATUS_READONLY 
  
> Die Nachricht soll im schreibgeschützten Modus geöffnet werden. Lösch-, Sende- und Verschiebungsvorgänge sollten deaktiviert werden. 
    
VCSTATUS_UNREAD 
  
> Es ist eine nächste oder vorherige ungelesene Nachricht in der Ansicht vorhanden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Status des Viewers wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularobjekte rufen die **IMAPIViewContext::GetViewStatus-Methode** auf, um zu bestimmen, ob in einer Formularansicht mehr Nachrichten in eine oder beide Richtungen aktiviert werden müssen, in der Richtung, in der ein **Next-Befehl** Nachrichten aktiviert, in der Richtung, in der ein **vorheriger** Befehl Nachrichten aktiviert, oder in beide Richtungen. Der Wert, auf den der  _Parameter lpulStatus_ verweist, wird verwendet, um zu bestimmen, ob die flags VCSTATUS_NEXT und VCSTATUS_PREV für [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)gültig sind. Wenn das VCSTATUS_DELETE Flag festgelegt ist, aber nicht das VCSTATUS_READONLY Flag, kann die Nachricht mithilfe der [IMAPIMessageSite::D eleteMessage-Methode](imapimessagesite-deletemessage.md) gelöscht werden. 
  
In der Regel deaktivieren Formulare Menübefehle und Schaltflächen, wenn sie nicht für den Kontext des Betrachters gültig sind. Ein Viewer kann ein Formular über eine Statusänderung benachrichtigen, indem er seine [IMAPIFormAdviseSink::OnChange-Methode](imapiformadvisesink-onchange.md) aufruft. 
  
Das VCSTATUS_MODAL Flag wird festgelegt, wenn das Formular an das Fenster gebunden werden muss, dessen Handle im vorherigen [IMAPIForm::D oVerb-Aufruf](imapiform-doverb.md) übergeben wird. Wenn VCSTATUS_MODAL festgelegt ist, kann das Formular den Thread verwenden, in dem der **DoVerb-Aufruf** ausgeführt wurde, bis das Formular geschlossen wird. Wenn VCSTATUS_MODAL nicht festgelegt ist, sollte das Formular nicht an dieses Fenster gebunden werden und darf nicht den Thread verwenden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetViewStatus  <br/> |MFCMAPI implementiert die **IMAPIViewContext::GetViewStatus-Methode** in dieser Funktion.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

