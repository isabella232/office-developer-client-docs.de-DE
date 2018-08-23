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
ms.openlocfilehash: 5380b6541e609c17a9005c3390c6d5db06155306
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567244"
---
# <a name="imapiformmgrcalcformpropset"></a>IMAPIFormMgr::CalcFormPropSet

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt ein Array von Eigenschaften, die eine Gruppe von Formularen verwendet.
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Parameter

 _pfrminfoarray_
  
> [in] Ein Zeiger auf ein Array von Formular Informationen-Objekten, mit denen die Formulare für die Eigenschaften zurückgegeben.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie das Array im Parameter _PpResults_ -Eigenschaft zurückgegeben werden. Die folgenden Kennzeichen können festgelegt werden: 
    
FORMPROPSET_INTERSECTION 
  
> Das zurückgegebene Array enthält die Schnittmenge der Eigenschaften des Formulars.
    
FORMPROPSET_UNION 
  
> Das zurückgegebene Array enthält die Union der Eigenschaften des Formulars.
    
PARAMETER MAPI_UNICODE 
  
> Die Zeichenfolgen, die in das Array zurückgegeben werden im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
 _ppResults_
  
> [out] Ein Zeiger auf einen Zeiger auf das zurückgegebene [SMAPIFormPropArray](smapiformproparray.md) -Struktur, die Eigenschaften enthält, die die Formularen verwendet werden. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formular Viewer rufen Sie die **IMAPIFormMgr::CalcFormPropSet** -Methode, um ein Array der Eigenschaften abzurufen, die eine Gruppe von Formularen verwendet. **CalcFormPropSet** übernimmt entweder eine Schnittmenge oder Kombination dieser Formulare-Eigenschaft festgelegt, je nachdem das Flag festlegen in der _UlFlags_ -Parameter, und es gibt eine **SMAPIFormPropArray** -Struktur, die resultierende Gruppe von enthält Eigenschaften. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Formular Viewer die Option MAPI_UNICODE im Parameter _UlFlags_ übergibt, sollten alle Zeichenfolgen als Unicode-Zeichenfolgen zurückgegeben werden soll. Formular Bibliothek Anbieter, die keine für Unicode-Zeichenfolgen Unterstützung sollte MAPI_E_BAD_CHARWIDTH zurückgegeben, wenn der Parameter MAPI_UNICODE übergeben wird. 
  
## <a name="see-also"></a>Siehe auch



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

