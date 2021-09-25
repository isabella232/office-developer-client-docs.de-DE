---
title: IMSProviderCompareStoreIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSProvider.CompareStoreIDs
api_type:
- COM
ms.assetid: c3e3cfaa-9c4a-482a-9411-9c4ab01d312f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: af34b77eb1a6fe8809d1910c03c80c2fea46fbf6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579775"
---
# <a name="imsprovidercomparestoreids"></a>IMSProvider::CompareStoreIDs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Eintragsbezeichner für den Nachrichtenspeicher, um zu bestimmen, ob sie auf dasselbe Speicherobjekt verweisen.
  
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
  
> [in] Die Größe (in Byte) des Eintragsbezeichners, auf den der  _lpEntryID1-Parameter_  _verweist._
    
 _lpEntryID1_
  
> [in] Ein Zeiger auf den ersten Eintragsbezeichner, der verglichen werden soll.
    
 _cbEntryID2_
  
> [in] Die Größe (in Byte) des Eintragsbezeichners, auf den der  _lpEntryID2-Parameter_  _verweist._
    
 _lpEntryID2_
  
> [in] Ein Zeiger auf den zweiten Eintragsbezeichner, der verglichen werden soll.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulResult_
  
> [out] Ein Zeiger auf das zurückgegebene Ergebnis des Vergleichs. TRUE, wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen; andernfalls FALSE.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

MAPI ruft die **IMSProvider::CompareStoreIDs-Methode** auf, wenn sie einen Aufruf der [IMAPISession::OpenMsgStore-Methode](imapisession-openmsgstore.md) verarbeitet. **CompareStoreIDs** wird an dieser Stelle aufgerufen, um zu bestimmen, welcher Profilabschnitt dem geöffneten Nachrichtenspeicher zugeordnet ist. Ein **CompareStoreIDs-Aufruf** kann ausgeführt werden, wenn keine Nachrichtenspeicher für einen bestimmten Speicheranbieter geöffnet sind. Darüber hinaus ruft MAPI **auch CompareStoreIDs** auf, wenn sie einen Store-Anbieteraufruf an die [IMAPISupport::OpenProfileSection-Methode](imapisupport-openprofilesection.md) verarbeitet. 
  
Die Von **CompareStoreIDs** verglichenen Eintragsbezeichner sind sowohl für die Dynamic Link Library (DLL) des aktuellen Speicheranbieters als auch für nicht gepackte Eintragsbezeichner des Speichers. Weitere Informationen zum Umbrechen von Speichereintragsbezeichnern finden Sie unter [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).
  
Das Vergleichen von Eintragsbezeichnern ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner aufweisen kann. Dies kann beispielsweise auftreten, nachdem eine neue Version eines Nachrichtenspeicheranbieters installiert wurde. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

