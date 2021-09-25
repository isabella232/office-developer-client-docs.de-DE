---
title: IMAPIPropDeleteProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.DeleteProps
api_type:
- COM
ms.assetid: 5cc642de-21f0-4826-bf21-aac4bcfc1328
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 036ec32924c8bbb0a305b46558180bfe25e02777
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564134"
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
  
> [in] Ein Zeiger auf ein Array von Eigenschaftentags, die die zu löschenden Eigenschaften angeben. Das **cValues-Element** der [SPropTagArray-Struktur,](sproptagarray.md) auf die von  _lpPropTagArray_ verwiesen wird, darf nicht Null sein, und der  _lpPropTagArray-Parameter_ selbst darf nicht NULL sein. 
    
 _lppProblems_
  
> [in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray-Struktur;](spropproblemarray.md) andernfalls NULL, was bedeutet, dass keine Fehlerinformationen erforderlich sind. Wenn  _lppProblems_ ein gültiger Zeiger für die Eingabe ist, gibt **DeleteProps** detaillierte Informationen zu Fehlern beim Löschen einer oder mehrerer Eigenschaften zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Eigenschaften wurden erfolgreich gelöscht.
    
MAPI_E_NO_ACCESS 
  
> Der Aufrufer verfügt über unzureichende Berechtigungen zum Löschen von Eigenschaften.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIProp::D eleteProps-Methode** entfernt eine oder mehrere Eigenschaften aus dem aktuellen Objekt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie müssen nicht zulassen, dass Eigenschaften aus allen Objekten gelöscht werden. Wenn das Objekt nicht modifizierbar ist, geben Sie MAPI_E_NO_ACCESS aus der **DeleteProps** -Methode zurück. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie müssen nicht den Eigenschaftstyp für jedes Eigenschaftstag im Eigenschaftentagarray festlegen, auf das der  _lpPropTagArray-Parameter_ verweist. Eigenschaftstypen werden ignoriert. es werden nur die Eigenschaftsbezeichner verwendet. 
  
Beachten Sie, dass einige Objekte keine Änderung zulassen und dass diese Objekte MAPI_E_NO_ACCESS aus der **DeleteProps-Methode** zurückgeben. Andere Objekte ermöglichen das Löschen einiger Eigenschaften, andere jedoch nicht. Wenn beim Löschen einiger Eigenschaften ein Problem auftritt, gibt **DeleteProps** S_OK zurück. Wenn Sie einen gültigen Zeiger im  _Parameter lppProblems_ übergeben haben, legt **DeleteProps** den Zeiger auf eine **SPropProblemArray-Struktur** fest, die detaillierte Informationen zu den Problemen mit den einzelnen Eigenschaften enthält. Wenn Sie beispielsweise alle Eigenschaften einer Nachricht löschen und ein Problem mit einer oder mehreren ihrer Anlagen vorliegt, enthält die **SPropProblemArray-Struktur** einen Eintrag für die **eigenschaft PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
Die Struktur, auf die von  _lppProblems_ verwiesen wird, ist nur gültig, wenn **DeleteProps** S_OK zurückgibt. Wenn **DeleteProps** einen Fehler zurückgibt, versuchen Sie nicht, die **SPropProblemArray-Struktur** zu verwenden. Rufen Sie stattdessen die [IMAPIProp::GetLastError-Methode](imapiprop-getlasterror.md) des Objekts auf, um weitere Informationen zum Fehler abzurufen. 
  
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

