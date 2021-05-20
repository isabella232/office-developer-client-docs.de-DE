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
ms.openlocfilehash: f0b217372f6b4848f83c993846cd08a81c7098e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430903"
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
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen **GetViewContext auf,** um einen Zeiger auf den Ansichtskontext zu erhalten, der in einem vorherigen Aufruf von [IMAPIForm::SetViewContext eingerichtet wurde.](imapiform-setviewcontext.md) Wenn kein vorheriger Aufruf von **SetViewContext** erfolgt ist, legt **GetViewContext**  _ppViewContext_ auf NULL fest. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Kopieren Sie den Ansichtskontextzeiger Ihres Formulars in den Zeiger, der von der aufrufenden Formularanzeige im  _ppViewContext-Parameter übergeben_ wird. Wenn das Formular keinen Ansichtskontext hat, legen Sie  _ppViewContext auf_ NULL. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI verwendet die **IMAPIForm::GetViewContext-Methode,** um zu überprüfen, ob ein Formular über einen Ansichtskontext verfügt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

