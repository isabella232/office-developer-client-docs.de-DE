---
title: IMAPIFormSetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.SetViewContext
api_type:
- COM
ms.assetid: a7b10007-42d8-4755-8362-f8ad9a8dad68
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 26ca126603ac1e695bd14a10cd8d9e637382b2e9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584303"
---
# <a name="imapiformsetviewcontext"></a>IMAPIForm::SetViewContext

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Stellt ein Ansichtskontext für das Formular her. 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a>Parameter

 _pViewContext_
  
> [in] Ein Zeiger auf den neuen Ansichtskontext für das Formular.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Ansichtskontext wurde erfolgreich festgelegt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formular Viewer rufen Sie die **IMAPIForm::SetViewContext** -Methode, um ein bestimmtes Formular Ansichtskontext als aktuelle einzurichten. Ein Formular kann jeweils nur ein Ansichtskontext haben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die meisten Formular Server implementieren **SetViewContext** mithilfe des folgenden Algorithmus: 
  
- Wenn ein Ansichtskontext für das Formular bereits vorhanden ist, brechen Sie Registrierung für das Formular durch Aufrufen der [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) -Methode mit **null** im Parameter _Pmnvs ab_ , und rufen Sie dann dem Ansichtskontext [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) -Methode, um die verringert den Referenzzähler. 
    
- Wenn der neue Ansichtskontext ungleich **null**ist, Anruf **IMAPIViewContext::SetAdviseSink** mithilfe des _pViewContext_ -Parameters So richten Sie eine neue Ansicht ein advise-Empfänger. 
    
- Wenn der neue Ansichtskontext ungleich **null**ist, rufen Sie die [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) -Methode, um zu bestimmen, welche Status-Flags festgelegt wurden. 
    
- Wenn der neue Ansichtskontext ungleich **null**ist, speichern Sie sie, und rufen Sie dessen [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) -Methode, um den Referenzzähler erhöhen. 
    
- Aktualisieren Sie alle Elemente der Benutzeroberfläche, die von dem Ansichtskontext abhängen. 
    
**SetViewContext** können auch andere Aktionen durchführen, je nach den Statusflags für von **IMAPIViewContext::GetViewStatus**zurückgegeben. Wenn die Flags VCSTATUS_NEXT und VCSTATUS_PREV zurückgegeben werden, können beispielsweise **SetViewContext** die **nächsten** oder **vorherigen** Schaltflächen für die neue Ansichtskontext aktivieren. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI (engl.) mithilfe die **IMAPIForm::SetViewContext** -Methode Ansichtskontext MFCMAPI des (engl.) auf dem Formular festgelegt werden, bevor das Formular angezeigt wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

