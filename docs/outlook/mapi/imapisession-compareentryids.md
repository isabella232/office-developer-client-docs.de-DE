---
title: IMAPISessionCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.CompareEntryIDs
api_type:
- COM
ms.assetid: 319f10e9-db8d-4d16-aa1f-6cf5fef493eb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4dfde82aa843072168288f4e0b0084dfccd5cd2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427815"
---
# <a name="imapisessioncompareentryids"></a>IMAPISession::CompareEntryIDs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob Sie auf dasselbe Objekt verweisen. 
  
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
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID1_ -Parameter verwiesen wird. 
    
 _lpEntryID1_
  
> in Ein Zeiger auf den ersten zu vergleichenden Eintragsbezeichner.
    
 _cbEntryID2_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID2_ -Parameter verwiesen wird. 
    
 _lpEntryID2_
  
> in Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden soll.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulResult_
  
> Out Ein Zeiger auf das Ergebnis des Vergleichs. TRUE, wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen, andernfalls false. andernfalls FALSE.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Vergleich war erfolgreich.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Eine oder beide der als Parameter angegebenen Eintragsbezeichner verweisen nicht auf Objekte, möglicherweise, da diese Objekte derzeit nicht geöffnet und nicht verfügbar sind.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISession:: CompareEntryIDs** -Methode vergleicht zwei Eintragsbezeichner, die zu einem einzelnen Dienstanbieter gehören, um zu bestimmen, ob Sie auf dasselbe Objekt verweisen. MAPI extrahiert den [MAPIUID](mapiuid.md) -Teil aus den Eintrags Bezeichnern, um den für die Objekte Verantwortlichen Dienstanbieter zu bestimmen, und ruft dann die **CompareEntryIDs** -Methode des Logo-Objekts auf, um den Vergleich auszuführen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **CompareEntryIDs** -Methode ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner aufweisen kann. Diese Situation kann beispielsweise auftreten, nachdem eine neue Version eines Dienstanbieters installiert wurde. 
  
Wenn **CompareEntryIDs** einen Fehler zurückgibt, führen Sie keine Aktion basierend auf dem Ergebnis des Vergleichs aus. Verwenden Sie stattdessen die konservativste Vorgehensweise. **CompareEntryIDs** kann fehlschlagen, wenn beispielsweise eine oder beide der Eintragsbezeichner eine ungültige **MAPIUID**enthalten. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog. cpp  <br/> |CbaseDialog:: OnCompareEntryIDs  <br/> |MFCMAPI verwendet die **IMAPISession:: CompareEntryIDs** -Methode, um zwei Eintrags-IDs zu vergleichen, die ein Benutzer eingibt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

