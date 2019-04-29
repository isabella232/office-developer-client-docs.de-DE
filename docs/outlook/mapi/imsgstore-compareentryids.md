---
title: IMsgStoreCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.CompareEntryIDs
api_type:
- COM
ms.assetid: 33d70748-0d3f-4be4-bcb5-7ec048887944
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2a2439bae79b497f018391983e2c4b03a35eee70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424252"
---
# <a name="imsgstorecompareentryids"></a>IMsgStore::CompareEntryIDs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob Sie auf den gleichen Eintrag in einem Nachrichtenspeicher verweisen. Dieser Aufruf wird von MAPI nur dann an einen Dienstanbieter weitergeleitet, wenn die eindeutigen IDs in beiden Eintrags Bezeichnern, die verglichen werden sollen, von diesem Anbieter verarbeitet werden.
  
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
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID1_ -Parameter verwiesen wird _._
    
 _lpEntryID1_
  
> in Ein Zeiger auf den ersten zu vergleichenden Eintragsbezeichner.
    
 _cbEntryID2_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID2_ -Parameter verwiesen wird _._
    
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
  
> Eine oder beide der als Parameter angegebenen Eintragsbezeichner verweisen nicht auf Objekte, möglicherweise weil die entsprechenden Objekte ungeöffnet und derzeit nicht verfügbar sind.
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgStore:: CompareEntryIDs** -Methode vergleicht zwei Eintragsbezeichner, die zum Nachrichtenspeicher gehören, um zu bestimmen, ob Sie auf dasselbe Objekt verweisen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **CompareEntryIDs** ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner aufweisen kann (beispielsweise nach der Installation einer neuen Version eines Nachrichtenspeicher Anbieters). 
  
Wenn **CompareEntryIDs** einen Fehler zurückgibt, führen Sie keine Aktion basierend auf dem Ergebnis des Vergleichs aus. Verwenden Sie stattdessen die konservativste Vorgehensweise. **CompareEntryIDs** kann fehlschlagen, wenn beispielsweise eine oder beide der Eintragsbezeichner eine ungültige **MAPIUID**enthält. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog. cpp  <br/> |CBaseDialog:: OnCompareEntryIDs  <br/> |MFCMAPI verwendet die **IMsgStore:: CompareEntryIDs** -Methode, um Eintrags-IDs zu vergleichen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

