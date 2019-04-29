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
  
> in Ein Zeiger auf ein Array von Property-Tags, die die zu löschenden Eigenschaften anzeigen. Das **cValues** -Element der [SPropTagArray](sproptagarray.md) -Struktur, auf die durch _lpPropTagArray_ verwiesen wird, darf nicht NULL sein, und der _lpPropTagArray_ -Parameter selbst darf nicht NULL sein. 
    
 _lppProblems_
  
> [in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur; andernfalls NULL, was bedeutet, dass keine Fehlerinformationen erforderlich sind. Wenn _lppProblems_ ein gültiger Zeiger auf der Eingabe ist, gibt **DeleteProps** detaillierte Informationen zu Fehlern beim Löschen einer oder mehrerer Eigenschaften zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Eigenschaften wurden erfolgreich gelöscht.
    
MAPI_E_NO_ACCESS 
  
> Der Aufrufer verfügt nicht über ausreichende Berechtigungen zum Löschen von Eigenschaften.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIProp::D eleteprops** -Methode entfernt eine oder mehrere Eigenschaften aus dem aktuellen Objekt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie müssen nicht zulassen, dass Eigenschaften aus allen Objekten gelöscht werden. Wenn das Objekt nicht geändert werden kann, geben Sie MAPI_E_NO_ACCESS von der **DeleteProps** -Methode zurück. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie müssen den Eigenschaftentyp für jedes Property-Tag im Property Tag-Array, auf das durch den _lpPropTagArray_ -Parameter verwiesen wird, nicht festlegen. Eigenschaftstypen werden ignoriert; nur die Eigenschaftenbezeichner werden verwendet. 
  
Beachten Sie, dass einige Objekte keine Änderung zulassen und diese Objekte MAPI_E_NO_ACCESS von der **DeleteProps** -Methode zurückgeben. Andere Objekte erlauben, dass einige Eigenschaften gelöscht werden, nicht aber andere. Wenn beim Löschen von nur einigen Eigenschaften ein Problem auftritt, gibt **DELETEPROPS** S_OK zurück. Wenn Sie einen gültigen Zeiger im _lppProblems_ -Parameter übergeben haben, legt **DeleteProps** den Zeiger auf eine **SPropProblemArray** -Struktur fest, die detaillierte Informationen zu den Problemen mit den einzelnen Eigenschaften enthält. Wenn Sie beispielsweise alle Eigenschaften einer Nachricht löschen und ein Problem mit einer oder mehreren ihrer Anlagen vorliegt, enthält die **SPropProblemArray** -Struktur einen Eintrag für die **PR_MESSAGE_ATTACHMENTS** ([pidtagmessageattachments ( ](pidtagmessageattachments-canonical-property.md))-Eigenschaft. 
  
Die Struktur, auf die durch _lppProblems_ verwiesen wird, ist nur gültig, wenn **DeleteProps** S_OK zurückgibt. Wenn **DeleteProps** einen Fehler zurückgibt, versuchen Sie nicht, die **SPropProblemArray** -Struktur zu verwenden. Rufen Sie stattdessen die [IMAPIProp:: getlasterroraufzurufen](imapiprop-getlasterror.md) -Methode des Objekts auf, um weitere Informationen zum Fehler abzurufen. 
  
Freigeben Sie die zurückgegebene **SPropProblemArray** -Struktur durch Aufrufen der [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |DeleteProperty  <br/> |MFCMAPI verwendet die **IMAPIProp::D eleteprops** -Methode, um eine Eigenschaft aus einem Objekt zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

