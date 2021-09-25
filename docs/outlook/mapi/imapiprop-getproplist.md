---
title: IMAPIPropGetPropList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.GetPropList
api_type:
- COM
ms.assetid: 0069c223-32bb-4286-b763-39fd45dc263b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dba0ced4c0a0858ebfd89ba1aaea7232d77deb1e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556595"
---
# <a name="imapipropgetproplist"></a>IMAPIProp::GetPropList

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt Eigenschaftstags für alle Eigenschaften zurück. 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die das Format für die Zeichenfolgen in den zurückgegebenen Eigenschaftstags steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
 _lppPropTagArray_
  
> [out] Ein Zeiger auf einen Zeiger auf das Eigenschaftentagarray, das Tags für alle Eigenschaften des Objekts enthält.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Alle Eigenschaftstags wurden erfolgreich zurückgegeben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIProp::GetPropList-Methode** ruft das Eigenschaftentag für jede Eigenschaft ab, die derzeit von einem Objekt unterstützt wird. Wenn das Objekt derzeit keine Eigenschaften unterstützt, gibt **GetPropList** ein Eigenschaftstagarray zurück, bei dem der **cValues-Member** auf 0 festgelegt ist. 
  
Der Bereich der von **GetPropList** zurückgegebenen Eigenschaften variiert von Anbieter zu Anbieter. Einige Dienstanbieter schließen diese Eigenschaften aus, für die der Aufrufer keinen Zugriff hat. Alle Anbieter geben Eigenschaften vom Typ **PT_OBJECT** zurück.
  
Wenn das Objekt Unicode nicht unterstützt, gibt **GetPropList** MAPI_E_BAD_CHARWIDTH zurück, auch wenn für das Objekt keine Zeichenfolgeneigenschaften definiert sind. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Remote-Transportanbieter implementieren **GetPropList** genau wie hier angegeben. Es gibt keine besonderen Bedenken. Ihre Implementierung sollte natürlich die gleiche Liste von Eigenschaften zurückgeben, die von der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) unterstützt wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf, um das Eigenschaftentagarray frei zu geben, auf das durch  _lppPropTagArray_ verwiesen wird. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI verwendet die **IMAPIProp::GetPropList-Methode,** um eine Eigenschaftenliste abzurufen, die an **GetProps** übergeben werden soll.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

