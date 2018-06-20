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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8eb19f9a2d3458e153b0758b56c502ce612be0cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792290"
---
# <a name="imapipropdeleteprops"></a>IMAPIProp::DeleteProps

  
  
**Betrifft**: Outlook 
  
Löscht eine oder mehrere Eigenschaften aus einem Objekt. 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameter

 _lpPropTagArray_
  
> [in] Ein Zeiger auf ein Array von Eigenschaftentags, die die zu löschenden Eigenschaften angeben. Das **cValues** Mitglied der [SPropTagArray](sproptagarray.md) -Struktur, die auf den _LpPropTagArray_ darf nicht NULL sein, und der _LpPropTagArray_ -Parameter selbst darf nicht NULL sein. 
    
 _lppProblems_
  
> [in, out] Bei Eingabe einen Zeiger auf einen Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur. andernfalls NULL, was bedeutet, dass es keine Notwendigkeit Fehlerinformationen besteht. Wenn _LppProblems_ einen gültigen Zeiger für die Eingabe ist, gibt **"DeleteProps"** detaillierte Informationen zu Fehlern beim Löschen einer oder mehrerer Eigenschaften. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Eigenschaften wurden erfolgreich gelöscht.
    
MAPI_E_NO_ACCESS 
  
> Der Aufrufer verfügt nicht über ausreichende Berechtigungen zum Löschen von Eigenschaften.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIProp::DeleteProps** -Methode entfernt eine oder mehrere Eigenschaften aus dem aktuellen Objekt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie müssen keinen Eigenschaften aller Objekte gelöscht werden können. Wenn das Objekt nicht geändert werden kann, geben Sie MAPI_E_NO_ACCESS von der **"DeleteProps"** -Methode. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie müssen keinen den Eigenschaftstyp für jede Eigenschaftentag in der Tag-Array-Eigenschaft auf das durch den Parameter _LpPropTagArray_ festgelegt. Eigenschaftentypen werden ignoriert. Es werden nur die Eigenschaftenbezeichner verwendet. 
  
Beachten Sie, dass einige Objekte keine Änderung zulassen und diese Objekte MAPI_E_NO_ACCESS von der Methode **"DeleteProps"** zurück. Andere Objekte können einige Eigenschaften gelöscht werden soll, jedoch nicht für andere Benutzer. Wenn ein Problem löschen nur einige der Eigenschaften vorhanden ist, wird **"DeleteProps"** S_OK zurückgegeben. Wenn Sie einen gültigen Zeiger im _LppProblems_ -Parameter übergeben haben, wird **"DeleteProps"** den Zeiger auf eine Struktur **SPropProblemArray** festlegen, detaillierte Informationen zu den Problemen, wobei jede Eigenschaft enthält. Beispielsweise wird Wenn Sie alle Eigenschaften einer Nachricht löschen, und es ein Problem mit einem oder mehreren der zugehörigen Anlagen ist, die **SPropProblemArray** -Struktur einen Eintrag enthalten für die **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments ](pidtagmessageattachments-canonical-property.md)) Eigenschaft. 
  
Die Struktur, die auf den _LppProblems_ ist nur gültig, wenn **"DeleteProps"** gibt S_OK zurück. Wenn **"DeleteProps"** einen Fehler zurückgibt, versuchen Sie nicht die Struktur **SPropProblemArray** verwenden. Rufen Sie stattdessen das Objekt [IMAPIProp::GetLastError](imapiprop-getlasterror.md) -Methode, um weitere Informationen zu dem Fehler zu erhalten. 
  
Frei die zurückgegebene Struktur **SPropProblemArray** durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |DeleteProperty  <br/> |MFCMAPI (engl.) verwendet die **IMAPIProp::DeleteProps** -Methode, um eine Eigenschaft aus einem Objekt zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp: IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

