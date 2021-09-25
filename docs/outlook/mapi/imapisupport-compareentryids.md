---
title: IMAPISupportCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.CompareEntryIDs
api_type:
- COM
ms.assetid: be6991d9-6353-4838-bc6b-39de51a94d8d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 393b52fee4da11d63a5c10426405d3b5c35d2f40
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625497"
---
# <a name="imapisupportcompareentryids"></a>IMAPISupport::CompareEntryIDs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie auf dasselbe Objekt verweisen. 
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID1_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID1-Parameter_ verweist. 
    
 _lpEntryID1_
  
> [in] Ein Zeiger auf den ersten Eintragsbezeichner, der verglichen werden soll.
    
 _cbEntryID2_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID2-Parameter_ verweist. 
    
 _lpEntryID2_
  
> [in] Ein Zeiger auf den zweiten Eintragsbezeichner, der verglichen werden soll.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulResult_
  
> [out] Ein Zeiger auf das Ergebnis des Vergleichs. TRUE, wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen; andernfalls FALSE.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Vergleich war erfolgreich.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Einer oder beide der Eintragsbezeichner, die als Parameter angegeben sind, beziehen sich nicht auf gültige Objekte, möglicherweise weil sie derzeit nicht geöffnet und nicht verfügbar sind.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::CompareEntryIDs-Methode** ist für Adressbuch- und Nachrichtenspeicheranbieter-Supportobjekte implementiert. **CompareEntryIDs** vergleicht zwei Eintragsbezeichner, die zu einem einzelnen Dienstanbieter gehören, um zu bestimmen, ob sie auf dasselbe Objekt verweisen. MAPI extrahiert den [MAPIUID-Teil](mapiuid.md) aus den Eintragsbezeichnern, um den für die Objekte verantwortlichen Dienstanbieter zu ermitteln. MapI ruft dann die **CompareEntryIDs-Methode** des Anmeldeobjekts auf, um den Vergleich durchzuführen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **CompareEntryIDs** ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner aufweisen kann. Diese Situation kann beispielsweise auftreten, nachdem eine neue Version eines Dienstanbieters installiert wurde. 
  
Wenn **CompareEntryIDs** einen Fehler zurückgibt, führen Sie keine Aktion basierend auf dem Ergebnis des Vergleichs aus. Verwenden Sie stattdessen den möglichst vorsichtigen Ansatz. **CompareEntryIDs** kann fehlschlagen, wenn beispielsweise einer oder beide Eintragsbezeichner eine ungültige **MAPIUID-Struktur** enthalten. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

