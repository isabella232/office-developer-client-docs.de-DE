---
title: IMAPIFormGetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIForm.GetViewContext
api_type:
- COM
ms.assetid: c6938986-a9f9-4ef4-9655-ded55b7357db
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a727173aa1a607e878170fb4f29374cdf3fb52ff
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551393"
---
# <a name="imapiformgetviewcontext"></a>IMAPIForm::GetViewContext

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den aktuellen Ansichtskontext für das Formular zurück. 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>Parameter

 _ppViewContext_
  
> [out] Ein Zeiger auf einen Zeiger auf den Ansichtskontext des Formulars.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der aktuelle Ansichtskontext des Formulars wurde erfolgreich zurückgegeben. 
    
S_FALSE 
  
> Es gibt keinen Ansichtskontext für das Formular.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen **GetViewContext** auf, um einen Zeiger auf den Ansichtskontext abzurufen, der in einem vorherigen Aufruf von [IMAPIForm::SetViewContext](imapiform-setviewcontext.md)erstellt wurde. Wenn kein vorheriger Aufruf von **SetViewContext** vorgenommen wurde, legt **GetViewContext**  _ppViewContext_ auf NULL fest. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Kopieren Sie den Ansichtskontextzeiger des Formulars in den Zeiger, der vom aufrufenden Formularviewer im  _PpViewContext-Parameter_ übergeben wird. Wenn das Formular keinen Ansichtskontext hat, legen Sie  _ppViewContext_ auf NULL fest. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI verwendet die **IMAPIForm::GetViewContext-Methode,** um zu überprüfen, ob ein Formular einen Ansichtskontext aufweist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

