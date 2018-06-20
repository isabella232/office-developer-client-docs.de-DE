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
# <a name="flatentry"></a><span data-ttu-id="c19df-103">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="c19df-103">FLATENTRY</span></span>

  
  
<span data-ttu-id="c19df-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c19df-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c19df-105">Eine Struktur [ENTRYID](entryid.md) plus eine Byteanzahl angegeben, die die Größe der Struktur **ENTRYID** angibt.</span><span class="sxs-lookup"><span data-stu-id="c19df-105">An [ENTRYID](entryid.md) structure plus a byte count that specifies the size of the **ENTRYID** structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c19df-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c19df-106">Header file:</span></span>  <br/> |<span data-ttu-id="c19df-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c19df-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c19df-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="c19df-108">Related macros:</span></span>  <br/> |<span data-ttu-id="c19df-109">[CbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span><span class="sxs-lookup"><span data-stu-id="c19df-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a><span data-ttu-id="c19df-110">Members</span><span class="sxs-lookup"><span data-stu-id="c19df-110">Members</span></span>

 <span data-ttu-id="c19df-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="c19df-111">**cb**</span></span>
  
> <span data-ttu-id="c19df-112">Anzahl der Bytes im **AbEntry** -Member.</span><span class="sxs-lookup"><span data-stu-id="c19df-112">Count of bytes in the **abEntry** member.</span></span> 
    
 <span data-ttu-id="c19df-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="c19df-113">**abEntry**</span></span>
  
> <span data-ttu-id="c19df-114">Die vollständige Eintrag-Bezeichner, der das Array von Flags und binäre Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="c19df-114">The complete entry identifier that includes the array of flags and binary data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c19df-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c19df-115">Remarks</span></span>

<span data-ttu-id="c19df-116">Eine Struktur **FLATENTRY** ähnelt eine [ENTRYID](entryid.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c19df-116">A **FLATENTRY** structure resembles an [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="c19df-117">Es gibt jedoch einige Unterschiede:</span><span class="sxs-lookup"><span data-stu-id="c19df-117">However, there are some differences:</span></span> 
  
- <span data-ttu-id="c19df-118">Eine Struktur **FLATENTRY** speichert die Größe des Eintrags-ID an. **ENTRYID** hingegen nicht.</span><span class="sxs-lookup"><span data-stu-id="c19df-118">A **FLATENTRY** structure stores the size of the entry identifier; **ENTRYID** does not.</span></span> 
    
- <span data-ttu-id="c19df-119">Eine Struktur **FLATENTRY** speichert die Kennzeichnungsdaten zusammen mit den restlichen die Eintrags-ID; **ENTRYID** separat gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c19df-119">A **FLATENTRY** structure stores the flag data together with the rest of the entry identifier; **ENTRYID** stores them separately.</span></span> 
    
- <span data-ttu-id="c19df-120">Eine Struktur **FLATENTRY** wird verwendet, um eine Eintrags-ID in einer Datei speichern oder in einem Stream von Bytes übergeben, während eine **ENTRYID** -Struktur, durch die [IMAPIProp](imapipropiunknown.md) -Schnittstellenmethoden und durch die folgenden Methoden **OpenEntry verwendet wird** : [IABLogon: : OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="c19df-120">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes whereas an **ENTRYID** structure is used by the [IMAPIProp](imapipropiunknown.md) interface methods and by the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="c19df-121">Eine Struktur **FLATENTRY** wird verwendet, um eine Eintrags-ID in einer Datei speichern, oder geben Sie ihn in einen Datenstrom von Bytes.</span><span class="sxs-lookup"><span data-stu-id="c19df-121">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> <span data-ttu-id="c19df-122">Eine **ENTRYID** -Struktur wird verwendet, um die Eintrags-ID auf dem Datenträger speichern.</span><span class="sxs-lookup"><span data-stu-id="c19df-122">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c19df-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c19df-123">See also</span></span>



[<span data-ttu-id="c19df-124">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c19df-124">ENTRYID</span></span>](entryid.md)


[<span data-ttu-id="c19df-125">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c19df-125">MAPI Structures</span></span>](mapi-structures.md)

