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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a1c5cdc67bc64f20dd8ba0a5e8682c5e2f97294f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792620"
---
# <a name="imsgstorecompareentryids"></a>IMsgStore::CompareEntryIDs

  
  
**Betrifft**: Outlook 
  
Vergleicht zwei Eintragsbezeichner, um festzustellen, ob sie auf dieselbe Rechtsgrundlage in einem Nachrichtenspeicher verweisen. MAPI übergibt dieses Anrufs mit einem Dienstanbieter nur, wenn der eindeutige Bezeichner (UIDs) in beiden Eintragsbezeichner verglichen werden soll, die von diesem Provider behandelt werden.
  
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
  
> [in] Die Byteanzahl von in die Eintrags-ID auf das durch den Parameter _lpEntryID1_ _._
    
 _lpEntryID1_
  
> [in] Ein Zeiger auf die erste Eintrags-ID, die verglichen werden.
    
 _cbEntryID2_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf das durch den Parameter _lpEntryID2_ _._
    
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
  
> Stellen eine oder beide der Eintragsbezeichner angegeben, wie der Parameter nicht auf Objekte, möglicherweise verweisen, da die entsprechenden Objekte nicht geöffneten und nicht mehr verfügbar sind.
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgStore::CompareEntryIDs** -Methode vergleicht zwei Eintragsbezeichner, die mit dem Nachrichtenspeicher, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen gehören. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **CompareEntryIDs** ist hilfreich, da ein Objekt mehr als eine gültige Eintrags-ID (beispielsweise nach der Installation einer neuen Version einer Nachricht Speicheranbieter) haben kann. 
  
Wenn **CompareEntryIDs** einen Fehler zurückgibt, führen Sie keine Aktion basierend auf dem Ergebnis des Vergleichs. In diesem Fall sollten Sie am häufigsten konservative Methode möglich. **CompareEntryIDs** können Fehler auftreten, wenn Sie beispielsweise eine oder beide der Eintragsbezeichner enthält eine ungültige **MAPIUID**. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnCompareEntryIDs  <br/> |MFCMAPI (engl.) verwendet die **IMsgStore::CompareEntryIDs** -Methode zum Vergleichen von Eintrags-IDs.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

