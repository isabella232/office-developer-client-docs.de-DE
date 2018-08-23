---
title: IMSProviderCompareStoreIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.CompareStoreIDs
api_type:
- COM
ms.assetid: c3e3cfaa-9c4a-482a-9411-9c4ab01d312f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 57b8438d655b3bc5b708fd7ed6734554a3a23ac4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585990"
---
# <a name="imsprovidercomparestoreids"></a>IMSProvider::CompareStoreIDs

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei e-Mail-Store-Eintragsbezeichner, um zu bestimmen, ob sie auf das gleiche Store-Objekt verweisen.
  
```cpp
HRESULT CompareStoreIDs(
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
  
> [in] Die Größe in Bytes für die Eintrags-ID auf das durch den Parameter _lpEntryID1_ _._
    
 _lpEntryID1_
  
> [in] Ein Zeiger auf die erste Eintrags-ID, die verglichen werden.
    
 _cbEntryID2_
  
> [in] Die Größe in Bytes für die Eintrags-ID auf das durch den Parameter _lpEntryID2_ _._
    
 _lpEntryID2_
  
> [in] Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulResult_
  
> [out] Ein Zeiger auf das zurückgegebene Ergebnis des Vergleichs. True, wenn die zwei-Eintragsbezeichner auf dasselbe Objekt verweisen. andernfalls, FALSE.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

MAPI ruft die **IMSProvider::CompareStoreIDs** -Methode auf, wenn sie einen Anruf an die [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) -Methode verarbeitet. **CompareStoreIDs** ist zu diesem Zeitpunkt aufgerufen, um zu bestimmen, welcher Profilabschnitt gegebenenfalls zugeordnet Nachrichtenspeicher wird geöffnet ist. **CompareStoreIDs** können aufgerufen werden, wenn keine Nachrichtenspeicher für einen bestimmten Anbieter geöffnet sind. Darüber hinaus ruft MAPI auch **CompareStoreIDs** bei der Verarbeitung eines Speicher-Anbieter Aufrufs der [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) -Methode. 
  
Die **CompareStoreIDs** bei einem Vergleich Eintragsbezeichner sind sowohl für die aktuelle Speichern des Anbieters Dynamic Link Library (DLL) und sind beide allein stehenden Store-Eintragsbezeichner. Weitere Informationen zum Umfließen eines Store-Eintragsbezeichner finden Sie unter [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).
  
Vergleichen von Eintragsbezeichner ist hilfreich, da ein Objekt mehr als eine gültige Eingabe Bezeichner haben kann. Dies kann beispielsweise vorkommen, nach der Installation einer neuen Version des Anbieters einer Nachricht. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

