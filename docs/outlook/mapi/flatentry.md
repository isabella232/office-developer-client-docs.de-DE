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
  
Eine [Eintrags](entryid.md) -Struktur plus eine Byte-Anzahl, die die Größe **** der Eintrags-Struktur angibt. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
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
  
> Die Anzahl der Bytes im **abEntry** -Element. 
    
 **abEntry**
  
> Die vollständige Eintrags-ID, die das Array von Flags und Binärdaten enthält.
    
## <a name="remarks"></a>Bemerkungen

Eine **FLATENTRY** -Struktur ähnelt einer [Eintrags](entryid.md) -Struktur. Es gibt jedoch einige Unterschiede: 
  
- Eine **FLATENTRY** -Struktur speichert die Größe des Eintrags Bezeichners; **** Die Eintrags-Nr. 
    
- Eine **FLATENTRY** -Struktur speichert die kennzeichendaten zusammen mit dem Rest der Eintrags-ID. **** Sie wird separat gespeichert. 
    
- Eine **FLATENTRY** -Struktur wird verwendet, um eine Eintrags-ID in einer Datei zu speichern oder in einem Stream von **** Bytes zu übertragen, während eine Eintragsstruktur von den [IMAPIProp](imapipropiunknown.md) -schnittstellenMethoden und von den folgenden OpenEntry-Methoden verwendet wird: **** [IABLogon: :](iablogon-openentry.md)OpenEntry, [IAddrBook::](iaddrbook-openentry.md)OpenEntry, [IMAPIContainer::](imapicontainer-openentry.md)OpenEntry, [IMAPISession::](imapisession-openentry.md)OpenEntry, [IMAPISupport::](imapisupport-openentry.md)OpenEntry, [IMsgStore::](imsgstore-openentry.md)OpenEntry, [IMSLogon:](imslogon-openentry.md) : OpenEntry
    
- Eine **FLATENTRY** -Struktur wird verwendet, um eine Eintrags-ID in einer Datei zu speichern oder in einem Stream von Bytes zu übertragen. Eine **Eintrags** Struktur wird verwendet, um eine Eintrags-ID auf dem Datenträger zu speichern. 
    
## <a name="see-also"></a>Siehe auch



[ENTRYID](entryid.md)


[MAPI-Strukturen](mapi-structures.md)

