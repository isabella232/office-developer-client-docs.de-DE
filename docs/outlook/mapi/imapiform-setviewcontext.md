---
title: IMAPIFormSetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIForm.SetViewContext
api_type:
- COM
ms.assetid: a7b10007-42d8-4755-8362-f8ad9a8dad68
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ae2e03464ec60392d6d8afaf008f6f38d46cf9a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579999"
---
# <a name="imapiformsetviewcontext"></a>IMAPIForm::SetViewContext

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Richtet einen Ansichtskontext für das Formular ein. 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a>Parameter

 _pViewContext_
  
> [in] Ein Zeiger auf den neuen Ansichtskontext für das Formular.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Ansichtskontext wurde erfolgreich festgelegt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen die **IMAPIForm::SetViewContext-Methode** auf, um einen bestimmten Formularansichtskontext als aktuell einzurichten. Ein Formular kann jeweils nur einen Ansichtskontext aufweisen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die meisten Formularserver implementieren **SetViewContext** mithilfe des folgenden Algorithmus: 
  
- Wenn bereits ein Ansichtskontext für das Formular vorhanden ist, brechen Sie die Registrierung des Formulars ab, indem Sie die [IMAPIViewContext::SetAdviseSink-Methode](imapiviewcontext-setadvisesink.md) mit **NULL** im  _parameter pmnvs_ aufrufen, und rufen Sie dann die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) des Ansichtskontexts auf, um die Anzahl der Verweise zu dekrementieren. 
    
- Wenn der neue Ansichtskontext nicht **NULL** ist, rufen **Sie IMAPIViewContext::SetAdviseSink** mithilfe des  _pViewContext-Parameters_ auf, um eine neue Empfehlungssenke für die Ansicht einzurichten. 
    
- Wenn der neue Ansichtskontext nicht **NULL** ist, rufen Sie die [IMAPIViewContext::GetViewStatus-Methode](imapiviewcontext-getviewstatus.md) auf, um zu bestimmen, welche Statusflags festgelegt wurden. 
    
- Wenn der neue Ansichtskontext nicht **NULL** ist, speichern Sie ihn, und rufen Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) auf, um die Referenzanzahl zu erhöhen. 
    
- Aktualisieren Sie alle Benutzeroberflächenelemente, die vom Ansichtskontext abhängen. 
    
Abhängig von den von **IMAPIViewContext::GetViewStatus** zurückgegebenen Statusflags kann **SetViewContext** auch andere Aktionen ausführen. Wenn beispielsweise die Flags VCSTATUS_NEXT und VCSTATUS_PREV zurückgegeben werden, kann **SetViewContext** die Schaltflächen **"Weiter"** und **"Zurück"** für den neuen Ansichtskontext aktivieren. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI verwendet die **IMAPIForm::SetViewContext-Methode,** um den Ansichtskontext von MFCMAPI auf dem Formular festzulegen, bevor das Formular angezeigt wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

