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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: df6347298aab5404ec69bd9ac876863e31b741d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792321"
---
# <a name="imapisessioncompareentryids"></a>IMAPISession::CompareEntryIDs

  
  
**Betrifft**: Outlook 
  
Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen. 
  
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
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _lpEntryID1_ verwiesen. 
    
 _lpEntryID1_
  
> [in] Ein Zeiger auf die erste Eintrags-ID, die verglichen werden.
    
 _cbEntryID2_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _lpEntryID2_ verwiesen. 
    
 _lpEntryID2_
  
> [in] Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulResult_
  
> [out] Ein Zeiger auf das Ergebnis des Vergleichs. True, wenn die zwei-Eintragsbezeichner auf dasselbe Objekt verweisen. andernfalls, FALSE.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Vergleich war erfolgreich.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Eine oder beide der als Parameter angegebenen Eintrags-IDs verweisen für Objekte, möglicherweise nicht, da diese Objekte derzeit nicht geöffneten und nicht verfügbar sind.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISession::CompareEntryIDs** -Methode vergleicht zwei Eintragsbezeichner, die mit einem einzelnen Dienstanbieter zu bestimmen, ob sie sich auf dasselbe Objekt verweisen gehören. MAPI extrahiert den [MAPIUID](mapiuid.md) Teil aus der Eintragsbezeichner bestimmen den Dienstanbieter verantwortlich für die Objekte und ruft dann **die Anmeldung des Objekts-Eintragsbezeichner zum Durchführen des Vergleichs** . 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

**CompareEntryIDs** -Methode ist nützlich, da ein Objekt mehr als eine gültige Eingabe Bezeichner haben kann. Dies kann beispielsweise vorkommen, nach der Installation einer neuen Version von einem Dienstanbieter. 
  
Wenn **CompareEntryIDs** einen Fehler zurückgibt, führen Sie keine Aktion basierend auf dem Ergebnis des Vergleichs. In diesem Fall sollten Sie am häufigsten konservative Methode möglich. **CompareEntryIDs** können Fehler auftreten, wenn Sie beispielsweise eine oder beide der Eintragsbezeichner eine ungültige **MAPIUID**enthalten. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CbaseDialog::OnCompareEntryIDs  <br/> |MFCMAPI (engl.) verwendet die **IMAPISession::CompareEntryIDs** -Methode zum Vergleichen von zwei Eintrags-ID, die ein Benutzer eingibt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

