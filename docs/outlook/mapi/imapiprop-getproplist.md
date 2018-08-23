---
title: IMAPIPropGetPropList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetPropList
api_type:
- COM
ms.assetid: 0069c223-32bb-4286-b763-39fd45dc263b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5417853dbb1fa87d2beead2f73ca57329e17b044
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571122"
---
# <a name="imapipropgetproplist"></a>IMAPIProp::GetPropList

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Eigenschaftentags für alle Eigenschaften zurückgegeben. 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die das Format für die Zeichenfolgen in der zurückgegebenen Eigenschaftentags steuert. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
 _lppPropTagArray_
  
> [out] Ein Zeiger auf einen Zeiger auf die Eigenschaft Tag-Array, das für alle Eigenschaften des Objekts enthält.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Alle Eigenschaftentags wurden erfolgreich zurückgegeben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIProp::GetPropList** -Methode ruft das Eigenschafts-Tag für jede Eigenschaft, die derzeit von einem Objekt unterstützt. Wenn das Objekt keine Eigenschaften derzeit nicht unterstützt, gibt **GetPropList** ein Array Tag-Eigenschaft mit dem **cValues** -Element auf 0 festgelegt. 
  
Der Umfang der Eigenschaften von **GetPropList** zurückgegebene variiert von Anbieter zu Anbieter. Einige Dienstanbieter ausschließen diese Eigenschaften für die der Anrufer nicht zugreifen kann. Alle Anbieter geben Eigenschaften vom Typ **PT_OBJECT**zurück.
  
Wenn das Objekt Unicode nicht unterstützt, gibt **GetPropList** MAPI_E_BAD_CHARWIDTH, auch wenn es keine Zeichenfolgeneigenschaften für das Objekt definiert sind. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Remote-Transport-Anbieter implementieren **GetPropList** hier genau wie angegeben. Es sind keine besonderen Bedenken. Die Implementierung sollte, natürlich, Eigenschaften, die von der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode unterstützt die gleiche Liste zurückgegeben. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion, um die Array-Tag-Eigenschaft auf den _LppPropTagArray_frei. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI (engl.) verwendet die **IMAPIProp::GetPropList** -Methode, um eine Eigenschaftenliste zum Übergeben an **GetProps**abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

