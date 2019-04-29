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
ms.openlocfilehash: 734e53c1e897c902c72319aa6f2d3d7af2d23fb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431708"
---
# <a name="imsprovidercomparestoreids"></a>IMSProvider::CompareStoreIDs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Nachrichtenspeicher Eintrags-IDs, um zu bestimmen, ob Sie auf dasselbe Store-Objekt verweisen.
  
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
  
> in Die Größe der Eintrags-ID, auf die durch den _lpEntryID1_ -Parameter verwiesen wird, in Bytes _._
    
 _lpEntryID1_
  
> in Ein Zeiger auf den ersten zu vergleichenden Eintragsbezeichner.
    
 _cbEntryID2_
  
> in Die Größe der Eintrags-ID, auf die durch den _lpEntryID2_ -Parameter verwiesen wird, in Bytes _._
    
 _lpEntryID2_
  
> in Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden soll.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulResult_
  
> Out Ein Zeiger auf das zurückgegebene Ergebnis des Vergleichs. TRUE, wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen, andernfalls false. andernfalls FALSE.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

MAPI Ruft die **IMSProvider:: CompareStoreIDs** -Methode auf, wenn ein Aufruf der [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) -Methode verarbeitet wird. **CompareStoreIDs** wird an dieser Stelle aufgerufen, um zu bestimmen, welcher Profil Abschnitt, falls vorhanden, dem zu öffnenden Nachrichtenspeicher zugeordnet ist. Ein **CompareStoreIDs** -Aufruf kann vorgenommen werden, wenn kein Nachrichtenspeicher für einen bestimmten Speicheranbieter geöffnet ist. Außerdem ruft MAPI **CompareStoreIDs** auf, wenn ein Speicheranbieter Aufruf an die [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) -Methode verarbeitet wird. 
  
Die Eintrags-IDs, die von **CompareStoreIDs** verglichen werden, sind sowohl für die Dynamic Link Library (dll) des aktuellen Speicheranbieters als auch für unwrappede Speicher Eintrags-IDs. Weitere Informationen zum Einbinden von Speicher Eintrags Bezeichnern finden Sie unter [IMAPISupport:: WrapStoreEntryID](imapisupport-wrapstoreentryid.md).
  
Das Vergleichen von Eintrags Bezeichnern ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner aufweisen kann. Dies kann beispielsweise der Fall sein, nachdem eine neue Version eines Nachrichtenspeicher Anbieters installiert wurde. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

