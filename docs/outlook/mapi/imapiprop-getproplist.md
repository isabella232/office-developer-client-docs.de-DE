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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f089fa2c608fb9fcb7deba2e061c5cf5886aa02f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316569"
---
# <a name="imapipropgetproplist"></a>IMAPIProp::GetPropList

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt Eigenschaftentags für alle Eigenschaften zurück. 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Eine Bitmaske von Flags, die das Format für die Zeichenfolgen in den zurückgegebenen Property-Tags steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    
 _lppPropTagArray_
  
> Out Ein Zeiger auf einen Zeiger auf das Property-Tag-Array, das Tags für alle Eigenschaften des Objekts enthält.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Alle Property-Tags wurden erfolgreich zurückgegeben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIProp::** getproplist-Methode ruft das Tag der Eigenschaft für jede Eigenschaft ab, die derzeit von einem Objekt unterstützt wird. Wenn das Objekt derzeit keine Eigenschaften unterstützt, gibt **** getproplist ein Property-Tag-Array zurück, wobei das **cValues** -Element auf 0 festgelegt ist. 
  
Der von getProplist zurück **** gegebene Bereich von Eigenschaften variiert von Anbieter zu Anbieter. Einige Dienstanbieter schließen diese Eigenschaften aus, für die der Aufrufer keinen Zugriff hat. Alle Anbieter geben Eigenschaften vom Typ **PT_OBJECT**zurück.
  
Wenn das Objekt Unicode nicht unterstützt, **** gibt getproplist MAPI_E_BAD_CHARWIDTH zurück, auch wenn keine Zeichenfolgeneigenschaften für das Objekt definiert sind. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Remote Transportanbieter implementieren **** getproplist genau wie hier angegeben. Es gibt keine besonderen Bedenken. Die Implementierung sollte natürlich die gleiche Liste von Eigenschaften zurückgeben, die von der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode unterstützt wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion auf, um das Eigenschaftentag-Array freizugeben, auf das durch _lppPropTagArray_verwiesen wird. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI verwendet die **IMAPIProp::** getproplist-Methode, um eine Eigenschaftenliste abzurufen, **** die an GetProps weitergegeben wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

