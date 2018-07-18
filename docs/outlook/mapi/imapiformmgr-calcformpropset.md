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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: abd2a3e2a1a810f902ad977413c89f2e8b0113a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792162"
---
# <a name="imapiformmgrcalcformpropset"></a>IMAPIFormMgr::CalcFormPropSet

  
  
**Betrifft**: Outlook 
  
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
    
## <a name="remarks"></a>Bemerkungen

Formular Viewer rufen Sie die **IMAPIFormMgr::CalcFormPropSet** -Methode, um ein Array der Eigenschaften abzurufen, die eine Gruppe von Formularen verwendet. **CalcFormPropSet** übernimmt entweder eine Schnittmenge oder Kombination dieser Formulare-Eigenschaft festgelegt, je nachdem das Flag festlegen in der _UlFlags_ -Parameter, und es gibt eine **SMAPIFormPropArray** -Struktur, die resultierende Gruppe von enthält Eigenschaften. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Formular Viewer die Option MAPI_UNICODE im Parameter _UlFlags_ übergibt, sollten alle Zeichenfolgen als Unicode-Zeichenfolgen zurückgegeben werden soll. Formular Bibliothek Anbieter, die keine für Unicode-Zeichenfolgen Unterstützung sollte MAPI_E_BAD_CHARWIDTH zurückgegeben, wenn der Parameter MAPI_UNICODE übergeben wird. 
  
## <a name="see-also"></a>Siehe auch



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

