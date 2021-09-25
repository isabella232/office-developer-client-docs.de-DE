---
title: IMAPISessionCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.CompareEntryIDs
api_type:
- COM
ms.assetid: 319f10e9-db8d-4d16-aa1f-6cf5fef493eb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 649384e09c2f46c55f2ee00ec6d8840c6b97fceb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567570"
---
# <a name="imapisessioncompareentryids"></a>IMAPISession::CompareEntryIDs

  
  
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
  
> Einer oder beide der als Parameter angegebenen Eintragsbezeichner beziehen sich nicht auf Objekte, möglicherweise weil diese Objekte derzeit nicht geöffnet und nicht verfügbar sind.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISession::CompareEntryIDs-Methode** vergleicht zwei Eintragsbezeichner, die zu einem einzelnen Dienstanbieter gehören, um zu bestimmen, ob sie auf dasselbe Objekt verweisen. MAPI extrahiert den [MAPIUID-Teil](mapiuid.md) aus den Eintragsbezeichnern, um den für die Objekte verantwortlichen Dienstanbieter zu ermitteln, und ruft dann die **CompareEntryIDs-Methode** des Anmeldeobjekts auf, um den Vergleich durchzuführen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **CompareEntryIDs-Methode** ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner aufweisen kann. Diese Situation kann beispielsweise auftreten, nachdem eine neue Version eines Dienstanbieters installiert wurde. 
  
Wenn **CompareEntryIDs** einen Fehler zurückgibt, führen Sie keine Aktion basierend auf dem Ergebnis des Vergleichs aus. Verwenden Sie stattdessen den möglichst vorsichtigen Ansatz. **CompareEntryIDs** kann fehlschlagen, wenn beispielsweise einer oder beide Eintrags-IDs eine ungültige **MAPIUID** enthalten. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CbaseDialog::OnCompareEntryIDs  <br/> |MFCMAPI verwendet die **IMAPISession::CompareEntryIDs-Methode,** um zwei Eintrags-IDs zu vergleichen, die ein Benutzer eingibt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

