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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286587"
---
# <a name="imapiformcontainercalcformpropset"></a>IMAPIFormContainer::CalcFormPropSet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt ein Array der Eigenschaften zurück, die von allen in einem Formular Container installierten Formularen verwendet werden.
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie das Eigenschaftenarray im _ppResults_ -Parameter zurückgegeben wird. Die folgenden Flags können festgelegt werden: 
    
FORMPROPSET_INTERSECTION 
  
> Das zurückgegebene Array enthält den Schnittpunkt der Eigenschaften der Formulare.
    
FORMPROPSET_UNION 
  
> Das zurückgegebene Array enthält die Vereinigung der Eigenschaften der Formulare.
    
MAPI_UNICODE 
  
> Die im Array zurückgegebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    
 _ppResults_
  
> Out Ein Zeiger auf einen Zeiger auf die zurückgegebene [SMAPIFormPropArray](smapiformproparray.md) -Struktur. Diese Struktur enthält alle Eigenschaften, die von den installierten Formularen verwendet werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Bemerkungen

Client Anwendungen rufen die **IMAPIFormContainer:: CalcFormPropSet** -Methode auf, um ein Array von Eigenschaften abzurufen, die von allen in einem Formular Container installierten Formularen verwendet werden. **IMAPIFormContainer:: CalcFormPropSet** funktioniert wie die [IMAPIFormMgr:: CalcFormPropSet](imapiformmgr-calcformpropset.md) -Methode, mit der Ausnahme, dass Sie auf jedem in einem bestimmten Container registrierten Formular ausgeführt wird. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Formularbibliothek Anbieter, die Unicode-Zeichenfolgen nicht unterstützen, sollten MAPI_E_BAD_CHARWIDTH zurückgeben, wenn MAPI_UNICODE übergeben wird.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **IMAPIFormContainer:: CalcFormPropSet** nimmt entweder eine Schnittmenge oder eine Vereinigung der Eigenschaftensätze der Formulare an, je nach dem im _ulFlags_ -Parameter festgelegten Flag und gibt eine **SMAPIFormPropArray** -Struktur zurück, die die die resultierende Gruppe von Eigenschaften. 
  
Wenn ein Client das MAPI_UNICODE-Flag in _ulFlags_übergibt, sind alle zurückgegebenen Zeichenfolgen Unicode.
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
  
[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

