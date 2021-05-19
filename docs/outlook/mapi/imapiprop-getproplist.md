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
ms.openlocfilehash: f089fa2c608fb9fcb7deba2e061c5cf5886aa02f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414788"
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
  
> [in] Eine Bitmaske mit Flags, die das Format für die Zeichenfolgen in den zurückgegebenen Eigenschaftstags steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.
    
 _lppPropTagArray_
  
> [out] Ein Zeiger auf einen Zeiger auf das Eigenschaftentagarray, das Tags für alle Eigenschaften des Objekts enthält.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Alle Eigenschaftstags wurden erfolgreich zurückgegeben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIProp::GetPropList-Methode** ruft das Eigenschaftstag für jede Eigenschaft ab, die derzeit von einem Objekt unterstützt wird. Wenn das Objekt derzeit keine Eigenschaften unterstützt, gibt **GetPropList** ein Eigenschaftstagarray zurück, bei dem **das Element cValues** auf 0 festgelegt ist. 
  
Der Umfang der von **GetPropList** zurückgegebenen Eigenschaften variiert von Anbieter zu Anbieter. Einige Dienstanbieter schließen die Eigenschaften aus, auf die der Anrufer keinen Zugriff hat. Alle Anbieter geben Eigenschaften vom Typ **PT_OBJECT**.
  
Wenn das Objekt Unicode nicht unterstützt, gibt **GetPropList** MAPI_E_BAD_CHARWIDTH zurück, auch wenn keine Zeichenfolgeneigenschaften für das Objekt definiert sind. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Remote-Transport-Anbieter implementieren **GetPropList** genau wie hier angegeben. Es gibt keine besonderen Bedenken. Ihre Implementierung sollte natürlich dieselbe Liste von Eigenschaften zurückgeben, die von der [IMAPIProp::GetProps-Methode unterstützt](imapiprop-getprops.md) wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf, um das Eigenschaftentagarray frei zu machen, auf das _von lppPropTagArray verwiesen wird._ 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI verwendet die **IMAPIProp::GetPropList-Methode,** um eine Eigenschaftsliste zu erhalten, die an **GetProps übergeben werden soll.**  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

