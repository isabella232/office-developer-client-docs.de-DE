---
title: IMAPIPropDeleteProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.DeleteProps
api_type:
- COM
ms.assetid: 5cc642de-21f0-4826-bf21-aac4bcfc1328
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5bfef87baa2dffa4605f9a7afa3833024f514430
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409237"
---
# <a name="imapipropdeleteprops"></a>IMAPIProp::DeleteProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Löscht eine oder mehrere Eigenschaften aus einem Objekt. 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameter

 _lpPropTagArray_
  
> [in] Ein Zeiger auf ein Array von Eigenschaftstags, die die zu löschenden Eigenschaften angeben. Das **cValues-Element** der [SPropTagArray-Struktur,](sproptagarray.md) auf die  _von lpPropTagArray_ verwiesen wird, darf nicht Null sein, und der  _lpPropTagArray-Parameter_ selbst darf nicht NULL sein. 
    
 _lppProblems_
  
> [in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray-Struktur;](spropproblemarray.md) Andernfalls NULL, was angibt, dass keine Fehlerinformationen benötigt werden. Wenn  _lppProblems ein_ gültiger Zeiger auf Eingaben ist, gibt **DeleteProps** detaillierte Informationen zu Fehlern beim Löschen einer oder mehreren Eigenschaften zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Eigenschaften wurden erfolgreich gelöscht.
    
MAPI_E_NO_ACCESS 
  
> Der Aufrufer verfügt über unzureichende Berechtigungen zum Löschen von Eigenschaften.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIProp::D eleteProps-Methode** entfernt eine oder mehrere Eigenschaften aus dem aktuellen Objekt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie müssen nicht zulassen, dass Eigenschaften aus allen Objekten gelöscht werden. Wenn das Objekt nicht veränderbar ist, geben Sie MAPI_E_NO_ACCESS **deleteProps-Methode** zurück. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie müssen nicht den Eigenschaftentyp für jedes Eigenschaftstag im Eigenschaftentagarray festlegen, auf das der  _lpPropTagArray-Parameter_ verweist. Eigenschaftstypen werden ignoriert. nur die Eigenschaftsbezeichner werden verwendet. 
  
Beachten Sie, dass einige Objekte keine Änderung zulassen und dass diese Objekte MAPI_E_NO_ACCESS **deleteProps-Methode** zurückgeben. Bei anderen Objekten können einige Eigenschaften gelöscht werden, andere jedoch nicht. Wenn ein Problem beim Löschen nur einiger Eigenschaften besteht, gibt **DeleteProps** S_OK. Wenn Sie einen gültigen Zeiger im  _lppProblems-Parameter_ übergeben haben, legt **DeleteProps** den Zeiger auf eine **SPropProblemArray-Struktur** fest, die detaillierte Informationen zu den Problemen mit jeder Eigenschaft enthält. Wenn Sie beispielsweise alle Eigenschaften einer Nachricht löschen und ein Problem mit einer oder mehreren Anlagen besteht, enthält die **SPropProblemArray-Struktur** einen Eintrag für die **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))-Eigenschaft. 
  
Die Struktur, auf die  _lppProblems_ verweist, ist nur gültig, wenn **DeleteProps** S_OK. Wenn **DeleteProps** einen Fehler zurückgibt, versuchen Sie nicht, die **SPropProblemArray-Struktur zu** verwenden. Rufen Sie stattdessen die [IMAPIProp::GetLastError-Methode](imapiprop-getlasterror.md) des Objekts auf, um weitere Informationen zum Fehler zu erhalten. 
  
Geben Sie die zurückgegebene **SPropProblemArray-Struktur** frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |DeleteProperty  <br/> |MFCMAPI verwendet die **IMAPIProp::D eleteProps-Methode,** um eine Eigenschaft aus einem Objekt zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

