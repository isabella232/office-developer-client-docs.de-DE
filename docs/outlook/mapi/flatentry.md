---
title: FLATENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FLATENTRY
api_type:
- COM
ms.assetid: 03e53e08-9113-4101-84c9-ccf6d43127f6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 38b8d06b39ddab2e7c287ee913b24cda26811e26
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604971"
---
# <a name="flatentry"></a>FLATENTRY

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine [ENTRYID-Struktur](entryid.md) plus eine Byteanzahl, die die Größe der **ENTRYID-Struktur** angibt. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makros:  <br/> |[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a>Members

 **cb**
  
> Anzahl der Bytes im **abEntry-Element.** 
    
 **abEntry**
  
> Der vollständige Eintragsbezeichner, der das Array von Flags und Binärdaten enthält.
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine **FLATENTRY-Struktur** ähnelt einer [ENTRYID-Struktur.](entryid.md) Es gibt jedoch einige Unterschiede: 
  
- Eine **FLATENTRY-Struktur** speichert die Größe des Eintragsbezeichners. **ENTRYID** nicht. 
    
- Eine **FLATENTRY-Struktur** speichert die Kennzeichendaten zusammen mit dem restlichen Eintragsbezeichner. **ENTRYID** speichert sie separat. 
    
- Eine **FLATENTRY-Struktur** wird verwendet, um einen Eintragsbezeichner in einer Datei zu speichern oder in einem Bytestream zu übergeben, während eine **ENTRYID-Struktur** von den [IMAPIProp-Schnittstellenmethoden](imapipropiunknown.md) und den folgenden **OpenEntry-Methoden** verwendet wird: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- Eine **FLATENTRY-Struktur** wird verwendet, um einen Eintragsbezeichner in einer Datei zu speichern oder in einem Bytestream zu übergeben. Eine **ENTRYID-Struktur** wird verwendet, um einen Eintragsbezeichner auf dem Datenträger zu speichern. 
    
## <a name="see-also"></a>Siehe auch



[ENTRYID](entryid.md)


[MAPI-Strukturen](mapi-structures.md)

