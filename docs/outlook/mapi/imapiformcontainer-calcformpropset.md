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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b15dc4e467644c2a0c3856372b550c3b55469f1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792143"
---
# <a name="imapiformcontainercalcformpropset"></a>IMAPIFormContainer::CalcFormPropSet

  
  
**Betrifft**: Outlook 
  
Gibt ein Array der Eigenschaften verwendet, die für alle Formen in einem Formular Container installiert.
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie das Array im Parameter _PpResults_ -Eigenschaft zurückgegeben werden. Die folgenden Kennzeichen können festgelegt werden: 
    
FORMPROPSET_INTERSECTION 
  
> Das zurückgegebene Array enthält die Schnittmenge der Eigenschaften der Forms.
    
FORMPROPSET_UNION 
  
> Das zurückgegebene Array enthält die Vereinigung der Forms-Eigenschaften.
    
PARAMETER MAPI_UNICODE 
  
> Die Zeichenfolgen, die in das Array zurückgegeben werden im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
 _ppResults_
  
> [out] Ein Zeiger auf einen Zeiger auf das zurückgegebene [SMAPIFormPropArray](smapiformproparray.md) -Struktur. Diese Struktur enthält alle Eigenschaften, die von den installierten Formularen verwendet. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Hinweise

Clientanwendungen rufen Sie die **IMAPIFormContainer::CalcFormPropSet** -Methode, um ein Array von Eigenschaften, die alle Formen in einem Formular Container installiert abzurufen. **IMAPIFormContainer::CalcFormPropSet** funktioniert wie die [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) -Methode, außer dass sie für jedes Formular, das in einem bestimmten Container registriert ausgeführt wird. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Formular Bibliothek Anbieter, die keine für Unicode-Zeichenfolgen Unterstützung sollte MAPI_E_BAD_CHARWIDTH zurückgegeben, wenn der Parameter MAPI_UNICODE übergeben wird.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **IMAPIFormContainer::CalcFormPropSet** akzeptiert, Schnittmenge oder eine Union-Sätzen für die Formulare-Eigenschaft, je nachdem das Flag in den _UlFlags_ -Parameter festgelegt, und es gibt eine **SMAPIFormPropArray** -Struktur, enthält die resultierende Gruppe von Eigenschaften. 
  
Wenn ein Client die Option MAPI_UNICODE _UlFlags_übergibt, werden alle zurückgegebene Zeichenfolgen Unicode.
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
  
[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md)

