---
title: IMAPIFormGetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.GetViewContext
api_type:
- COM
ms.assetid: c6938986-a9f9-4ef4-9655-ded55b7357db
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9f09f29d67bff6588c826b92d93aead491510cef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574818"
---
# <a name="imapiformgetviewcontext"></a>IMAPIForm::GetViewContext

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt den aktuellen Ansichtskontext für das Formular zurück. 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>Parameter

 _ppViewContext_
  
> [out] Ein Zeiger auf einen Zeiger auf das Formular Ansichtskontext.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Formular aktuellen Ansichtskontext wurde erfolgreich zurückgegeben. 
    
S_FALSE 
  
> Es ist keine Ansichtskontext für das Formular.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formular Viewer aufrufen **GetViewContext** um einen Zeiger auf die in einem vorherigen Aufruf von [IMAPIForm::SetViewContext](imapiform-setviewcontext.md)hergestellt Ansichtskontext zu erhalten. Falls keine vorherigen Aufruf **SetViewContext**vorgenommen wurden, legt **GetViewContext** _PpViewContext_ auf NULL fest. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Kopieren des Formulars Ansicht Kontext Zeiger in der durch den aufrufenden Formular Viewer im _PpViewContext_ -Parameter übergebene Zeiger. Wenn das Formular nicht über ein Ansichtskontext verfügt, _PpViewContext_ auf NULL festgelegt wurde. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI (engl.) verwendet die **IMAPIForm::GetViewContext** -Methode überprüfen, ob ein Formular ein Ansichtskontext aufweist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

