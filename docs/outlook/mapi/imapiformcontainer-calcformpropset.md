---
title: IMAPIFormContainerCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormContainer.CalcFormPropSet
api_type:
- COM
ms.assetid: 594e3aac-a00f-422e-8e7a-949e4c9a3f8d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e88762457df923b88c22bc21845052f39c2fe051
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571815"
---
# <a name="imapiformcontainercalcformpropset"></a>IMAPIFormContainer::CalcFormPropSet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt ein Array der Eigenschaften zurück, die von allen in einem Formularcontainer installierten Formularen verwendet werden.
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Eigenschaftenarray im  _PpResults-Parameter_ zurückgegeben wird. Die folgenden Flags können festgelegt werden: 
    
FORMPROPSET_INTERSECTION 
  
> Das zurückgegebene Array enthält die Schnittmenge der Formulareigenschaften.
    
FORMPROPSET_UNION 
  
> Das zurückgegebene Array enthält die Vereinigung der Eigenschaften der Formulare.
    
MAPI_UNICODE 
  
> Die im Array zurückgegebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
 _ppResults_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene [SMAPIFormPropArray-Struktur.](smapiformproparray.md) Diese Struktur enthält alle Eigenschaften, die von den installierten Formularen verwendet werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>HinwBemerkungeneise

Clientanwendungen rufen die **IMAPIFormContainer::CalcFormPropSet-Methode** auf, um ein Array von Eigenschaften abzurufen, die von allen in einem Formularcontainer installierten Formularen verwendet werden. **IMAPIFormContainer::CalcFormPropSet** funktioniert wie die [IMAPIFormMgr::CalcFormPropSet-Methode,](imapiformmgr-calcformpropset.md) außer dass es auf jedem Formular ausgeführt wird, das in einem bestimmten Container registriert ist. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Formularbibliotheksanbieter, die unicode-Zeichenfolgen nicht unterstützen, sollten MAPI_E_BAD_CHARWIDTH zurückgeben, wenn MAPI_UNICODE übergeben wird.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **IMAPIFormContainer::CalcFormPropSet** verwendet eine Schnittmenge oder eine Vereinigung der Eigenschaftensätze der Formulare, abhängig vom im  _ulFlags-Parameter_ festgelegten Flag, und es wird eine **SMAPIFormPropArray-Struktur** zurückgegeben, die die resultierende Gruppe von Eigenschaften enthält. 
  
Wenn ein Client das flag MAPI_UNICODE in  _ulFlags_ übergibt, sind alle zurückgegebenen Zeichenfolgen Unicode.
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
  
[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

