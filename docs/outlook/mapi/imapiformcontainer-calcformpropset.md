---
title: IMAPIFormContainerCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.CalcFormPropSet
api_type:
- COM
ms.assetid: 594e3aac-a00f-422e-8e7a-949e4c9a3f8d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ec1933f80f211c7c381f9de6b15d414932b9a78e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414914"
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
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Eigenschaftenarray im  _ppResults-Parameter_ zurückgegeben wird. Die folgenden Kennzeichen können festgelegt werden: 
    
FORMPROPSET_INTERSECTION 
  
> Das zurückgegebene Array enthält die Schnittmenge der Eigenschaften der Formulare.
    
FORMPROPSET_UNION 
  
> Das zurückgegebene Array enthält die Vereinigung der Eigenschaften der Formulare.
    
MAPI_UNICODE 
  
> Die im Array zurückgegebenen Zeichenfolgen haben das Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.
    
 _ppResults_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene [SMAPIFormPropArray-Struktur.](smapiformproparray.md) Diese Struktur enthält alle Eigenschaften, die von den installierten Formularen verwendet werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Hinweise

Clientanwendungen rufen die **IMAPIFormContainer::CalcFormPropSet-Methode** auf, um ein Array von Eigenschaften zu erhalten, das von allen in einem Formularcontainer installierten Formularen verwendet wird. **IMAPIFormContainer::CalcFormPropSet** funktioniert wie die [IMAPIFormMgr::CalcFormPropSet-Methode,](imapiformmgr-calcformpropset.md) mit der Ausnahme, dass sie auf jedem Formular ausgeführt wird, das in einem bestimmten Container registriert ist. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Formularbibliotheksanbieter, die keine Unicode-Zeichenfolgen unterstützen, sollten MAPI_E_BAD_CHARWIDTH zurückgeben, MAPI_UNICODE übergeben wird.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **IMAPIFormContainer::CalcFormPropSet** nimmt je nach dem im  _ulFlags-Parameter_ festgelegten Flag entweder eine Schnittmenge oder eine Vereinigung der Eigenschaftensätze der Formulare an und gibt eine **SMAPIFormPropArray-Struktur** zurück, die die resultierende Gruppe von Eigenschaften enthält. 
  
Wenn ein Client das MAPI_UNICODE in  _ulFlags_ übergibt, sind alle zurückgegebenen Zeichenfolgen Unicode.
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
  
[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

