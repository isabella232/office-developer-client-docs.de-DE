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
  
Vergleicht zwei Nachrichtenspeichereintragsbezeichner, um zu bestimmen, ob sie auf dasselbe Speicherobjekt verweisen.
  
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
  
> [in] Die Größe des Eintragsbezeichners in Bytes, auf den der  _lpEntryID1-Parameter_  _verweist._
    
 _lpEntryID1_
  
> [in] Ein Zeiger auf die erste Zutritts-ID, die verglichen werden soll.
    
 _cbEntryID2_
  
> [in] Die Größe des Eintragsbezeichners in Bytes, auf den der  _lpEntryID2-Parameter_  _verweist._
    
 _lpEntryID2_
  
> [in] Ein Zeiger auf den zweiten Eintragsbezeichner, der verglichen werden soll.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulResult_
  
> [out] Ein Zeiger auf das zurückgegebene Ergebnis des Vergleichs. TRUE, wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen. Andernfalls FALSE.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

MAPI ruft die **IMSProvider::CompareStoreIDs-Methode** auf, wenn sie einen Aufruf der [IMAPISession::OpenMsgStore-Methode](imapisession-openmsgstore.md) verarbeitet. **CompareStoreIDs wird** an dieser Stelle aufgerufen, um zu bestimmen, welcher Profilabschnitt dem geöffneten Nachrichtenspeicher zugeordnet ist. Ein **CompareStoreIDs-Aufruf** kann vorgenommen werden, wenn keine Nachrichtenspeicher für einen bestimmten Speicheranbieter geöffnet sind. Darüber hinaus ruft MAPI **compareStoreIDs** auf, wenn ein Speicheranbieteraufruf an die [IMAPISupport::OpenProfileSection-Methode verarbeitet](imapisupport-openprofilesection.md) wird. 
  
Die mit **CompareStoreIDs** verglichenen Eintrags-IDs sind sowohl für die Dynamic-Link Library (DLL) des aktuellen Speicheranbieters als auch für die entpackten Speichereintrags-IDs. Weitere Informationen zum Umbruch von Speichereintragsbezeichnern finden Sie unter [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).
  
Das Vergleichen von Eintragsbezeichnern ist nützlich, da ein Objekt mehr als einen gültigen Eintragsbezeichner enthalten kann. Dies kann beispielsweise auftreten, nachdem eine neue Version eines Nachrichtenspeicheranbieters installiert wurde. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

