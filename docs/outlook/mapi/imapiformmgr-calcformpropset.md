---
title: IMAPIFormMgrCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgr.CalcFormPropSet
api_type:
- COM
ms.assetid: ab302bfd-5cff-49b4-b0d2-308ae5af478d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 894181e01fbe09fba018fe2cbff58f65ef4eb84c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571794"
---
# <a name="imapiformmgrcalcformpropset"></a>IMAPIFormMgr::CalcFormPropSet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt ein Array der Eigenschaften zurück, die eine Gruppe von Formularen verwendet.
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Parameter

 _pfrminfoarray_
  
> [in] Ein Zeiger auf ein Array von Formularinformationsobjekten, die die Formulare identifizieren, für die Eigenschaften zurückgegeben werden sollen.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Eigenschaftenarray im  _PpResults-Parameter_ zurückgegeben wird. Die folgenden Flags können festgelegt werden: 
    
FORMPROPSET_INTERSECTION 
  
> Das zurückgegebene Array enthält die Schnittmenge der Eigenschaften des Formulars.
    
FORMPROPSET_UNION 
  
> Das zurückgegebene Array enthält die Vereinigung der Eigenschaften des Formulars.
    
MAPI_UNICODE 
  
> Die im Array zurückgegebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
 _ppResults_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene [SMAPIFormPropArray-Struktur,](smapiformproparray.md) die die von den Formularen verwendeten Eigenschaften enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen die **IMAPIFormMgr::CalcFormPropSet-Methode** auf, um ein Array der Eigenschaften abzurufen, die eine Gruppe von Formularen verwendet. **CalcFormPropSet** verwendet entweder eine Schnittmenge oder eine Vereinigung der Eigenschaftensätze dieser Formulare, abhängig vom im  _ulFlags-Parameter_ festgelegten Flag, und es gibt eine **SMAPIFormPropArray-Struktur** zurück, die die resultierende Gruppe von Eigenschaften enthält. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Formularviewer das MAPI_UNICODE Flag im  _ulFlags-Parameter_ übergibt, sollten alle Zeichenfolgen als Unicode-Zeichenfolgen zurückgegeben werden. Formularbibliotheksanbieter, die unicode-Zeichenfolgen nicht unterstützen, sollten MAPI_E_BAD_CHARWIDTH zurückgeben, wenn MAPI_UNICODE übergeben wird. 
  
## <a name="see-also"></a>Siehe auch



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

