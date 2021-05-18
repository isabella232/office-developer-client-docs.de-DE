---
title: FLATENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRY
api_type:
- COM
ms.assetid: 03e53e08-9113-4101-84c9-ccf6d43127f6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e47f4e0d1ab9ab3ecfd53932b8ef26440134c603
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407242"
---
# <a name="flatentry"></a>FLATENTRY

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine [ENTRYID-Struktur](entryid.md) und eine Byteanzahl, die die Größe der **ENTRYID-Struktur** angibt. 
  
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

## <a name="members"></a>Elemente

 **cb**
  
> Anzahl der Bytes im **abEntry-Element.** 
    
 **abEntry**
  
> Der vollständige Eintragsbezeichner, der das Array von Flags und Binärdaten enthält.
    
## <a name="remarks"></a>Hinweise

Eine **FLATENTRY-Struktur** ähnelt einer [ENTRYID-Struktur.](entryid.md) Es gibt jedoch einige Unterschiede: 
  
- Eine **FLATENTRY-Struktur** speichert die Größe des Eintragsbezeichners. **ENTRYID** nicht. 
    
- Eine **FLATENTRY-Struktur** speichert die Kennzeichendaten zusammen mit dem rest der Eintrags-ID. **ENTRYID** speichert sie separat. 
    
- Eine **FLATENTRY-Struktur** wird verwendet, um einen Eintragsbezeichner in einer Datei zu speichern oder in einem Bytestrom zu übergeben, während eine **ENTRYID-Struktur** von den [IMAPIProp-Schnittstellenmethoden](imapipropiunknown.md) und den folgenden **OpenEntry-Methoden** verwendet wird: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- Eine **FLATENTRY-Struktur** wird verwendet, um eine Eintrags-ID in einer Datei zu speichern oder sie in einem Bytestrom zu übergeben. Eine **ENTRYID-Struktur** wird verwendet, um eine Eintrags-ID auf dem Datenträger zu speichern. 
    
## <a name="see-also"></a>Siehe auch



[ENTRYID](entryid.md)


[MAPI-Strukturen](mapi-structures.md)

