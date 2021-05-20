---
title: IMAPIFormMgrCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CalcFormPropSet
api_type:
- COM
ms.assetid: ab302bfd-5cff-49b4-b0d2-308ae5af478d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bf072aba27c90b7cea80c464e17fafb47524b695
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436426"
---
# <a name="imapiformmgrcalcformpropset"></a>IMAPIFormMgr::CalcFormPropSet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt ein Array der Eigenschaften zurück, die von einer Gruppe von Formularen verwendet werden.
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Parameter

 _pfrminfoarray_
  
> [in] Ein Zeiger auf ein Array von Formularinformationsobjekten, die die Formulare identifizieren, für die Eigenschaften zurückgeben werden sollen.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Eigenschaftenarray im  _ppResults-Parameter_ zurückgegeben wird. Die folgenden Kennzeichen können festgelegt werden: 
    
FORMPROPSET_INTERSECTION 
  
> Das zurückgegebene Array enthält die Schnittmenge der Eigenschaften des Formulars.
    
FORMPROPSET_UNION 
  
> Das zurückgegebene Array enthält die Vereinigung der Eigenschaften des Formulars.
    
MAPI_UNICODE 
  
> Die im Array zurückgegebenen Zeichenfolgen haben das Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.
    
 _ppResults_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene [SMAPIFormPropArray-Struktur,](smapiformproparray.md) die die von den Formularen verwendeten Eigenschaften enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IMAPIFormMgr::CalcFormPropSet-Methode** auf, um ein Array der Eigenschaften zu erhalten, die von einer Gruppe von Formularen verwendet werden. **CalcFormPropSet** verwendet je nach dem im  _ulFlags-Parameter_ festgelegten Kennzeichen eine Schnittmenge oder eine Vereinigung der Eigenschaftensätze dieser Formulare und gibt eine **SMAPIFormPropArray-Struktur** zurück, die die resultierende Gruppe von Eigenschaften enthält. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Formularanzeiger das MAPI_UNICODE im  _ulFlags-Parameter_ übergibt, sollten alle Zeichenfolgen als Unicode-Zeichenfolgen zurückgegeben werden. Formularbibliotheksanbieter, die keine Unicode-Zeichenfolgen unterstützen, sollten MAPI_E_BAD_CHARWIDTH zurückgeben, MAPI_UNICODE übergeben wird. 
  
## <a name="see-also"></a>Siehe auch



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

