---
title: IMsgStoreCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.CompareEntryIDs
api_type:
- COM
ms.assetid: 33d70748-0d3f-4be4-bcb5-7ec048887944
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 23982628a21a2eb5e3816e378977dc9bf35b1690
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620695"
---
# <a name="imsgstorecompareentryids"></a>IMsgStore::CompareEntryIDs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie auf denselben Eintrag in einem Nachrichtenspeicher verweisen. MapI übergibt diesen Aufruf nur dann an einen Dienstanbieter, wenn die eindeutigen Bezeichner (UIDs) in beiden zu vergleichenden Eintragsbezeichnern von diesem Anbieter verarbeitet werden.
  
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
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID1-Parameter_  _verweist._
    
 _lpEntryID1_
  
> [in] Ein Zeiger auf den ersten Eintragsbezeichner, der verglichen werden soll.
    
 _cbEntryID2_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID2-Parameter_  _verweist._
    
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
  
> Einer oder beide der als Parameter angegebenen Eintragsbezeichner beziehen sich nicht auf Objekte, möglicherweise weil die entsprechenden Objekte nicht geöffnet sind und derzeit nicht verfügbar sind.
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgStore::CompareEntryIDs-Methode** vergleicht zwei Eintragsbezeichner, die zum Nachrichtenspeicher gehören, um zu bestimmen, ob sie auf dasselbe Objekt verweisen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **CompareEntryIDs** ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner haben kann (z. B. nach der Installation einer neuen Version eines Nachrichtenspeicheranbieters). 
  
Wenn **CompareEntryIDs** einen Fehler zurückgibt, führen Sie keine Aktion basierend auf dem Ergebnis des Vergleichs aus. Verwenden Sie stattdessen den möglichst vorsichtigen Ansatz. **CompareEntryIDs** kann fehlschlagen, wenn beispielsweise einer oder beide Eintragsbezeichner eine ungültige **MAPIUID** enthalten. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnCompareEntryIDs  <br/> |MFCMAPI verwendet die **IMsgStore::CompareEntryIDs-Methode** zum Vergleichen von Eintrags-IDs.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

