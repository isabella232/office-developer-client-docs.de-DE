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
ms.openlocfilehash: 81d99b2bbe6ef7914a4b7d253a3472026872260d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350946"
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
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IMAPIForm::SetViewContext-Methode** auf, um einen bestimmten Formularansichtskontext als aktuell zu erstellen. Ein Formular kann immer nur einen Ansichtskontext haben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die meisten Formularserver implementieren **SetViewContext** mithilfe des folgenden Algorithmus: 
  
- Wenn bereits ein Ansichtskontext für das Formular vorhanden ist, brechen Sie die Registrierung des Formulars ab, indem Sie die [IMAPIViewContext::SetAdviseSink-Methode](imapiviewcontext-setadvisesink.md) mit **Null** im  _pmnvs-Parameter_ aufrufen und dann die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) des Ansichtskontexts aufrufen, um die Referenzanzahl zu dekrementieren. 
    
- Wenn der neue Ansichtskontext nicht **null** ist, rufen Sie **IMAPIViewContext::SetAdviseSink** auf, indem Sie den  _pViewContext-Parameter_ verwenden, um eine neue Ansichtssenke zu einrichten. 
    
- Wenn der neue Ansichtskontext nicht **null** ist, rufen Sie die [IMAPIViewContext::GetViewStatus-Methode](imapiviewcontext-getviewstatus.md) auf, um zu bestimmen, welche Statusflags festgelegt wurden. 
    
- Wenn der neue Ansichtskontext nicht **null** ist, speichern Sie ihn, und rufen Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) auf, um die Referenzanzahl zu erhöhen. 
    
- Aktualisieren Sie alle Benutzeroberflächenelemente, die vom Ansichtskontext abhängen. 
    
Abhängig von den status flags, die von **IMAPIViewContext::GetViewStatus** zurückgegeben werden, **kann SetViewContext** auch andere Aktionen ausführen. Wenn beispielsweise die VCSTATUS_NEXT und VCSTATUS_PREV zurückgegeben werden, kann **SetViewContext** die Schaltflächen **Next** und **Previous** für den neuen Ansichtskontext aktivieren. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI verwendet die **IMAPIForm::SetViewContext-Methode,** um den Ansichtskontext von MFCMAPI auf dem Formular vor dem Anzeigen des Formulars zu setzen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

