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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2f5f4d50b085c437d1caab5f70dcb741afe090bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791692"
---
# <a name="flatentry"></a>FLATENTRY

  
  
**Betrifft**: Outlook 
  
Eine Struktur [ENTRYID](entryid.md) plus eine Byteanzahl angegeben, die die Größe der Struktur **ENTRYID** angibt. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makros:  <br/> |[CbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a>Members

 **cb**
  
> Anzahl der Bytes im **AbEntry** -Member. 
    
 **abEntry**
  
> Die vollständige Eintrag-Bezeichner, der das Array von Flags und binäre Daten enthält.
    
## <a name="remarks"></a>Hinweise

Eine Struktur **FLATENTRY** ähnelt eine [ENTRYID](entryid.md) -Struktur. Es gibt jedoch einige Unterschiede: 
  
- Eine Struktur **FLATENTRY** speichert die Größe des Eintrags-ID an. **ENTRYID** hingegen nicht. 
    
- Eine Struktur **FLATENTRY** speichert die Kennzeichnungsdaten zusammen mit den restlichen die Eintrags-ID; **ENTRYID** separat gespeichert. 
    
- Eine Struktur **FLATENTRY** wird verwendet, um eine Eintrags-ID in einer Datei speichern oder in einem Stream von Bytes übergeben, während eine **ENTRYID** -Struktur, durch die [IMAPIProp](imapipropiunknown.md) -Schnittstellenmethoden und durch die folgenden Methoden **OpenEntry verwendet wird** : [IABLogon: : OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- Eine Struktur **FLATENTRY** wird verwendet, um eine Eintrags-ID in einer Datei speichern, oder geben Sie ihn in einen Datenstrom von Bytes. Eine **ENTRYID** -Struktur wird verwendet, um die Eintrags-ID auf dem Datenträger speichern. 
    
## <a name="see-also"></a>Siehe auch



[ENTRYID](entryid.md)


[MAPI-Strukturen](mapi-structures.md)

