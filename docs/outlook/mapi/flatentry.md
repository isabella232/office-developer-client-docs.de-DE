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
ms.openlocfilehash: e47f4e0d1ab9ab3ecfd53932b8ef26440134c603
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334818"
---
# <a name="flatentry"></a><span data-ttu-id="02945-103">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="02945-103">FLATENTRY</span></span>

  
  
<span data-ttu-id="02945-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02945-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02945-105">Eine [Eintrags](entryid.md) -Struktur plus eine Byte-Anzahl, die die Größe \*\*\*\* der Eintrags-Struktur angibt.</span><span class="sxs-lookup"><span data-stu-id="02945-105">An [ENTRYID](entryid.md) structure plus a byte count that specifies the size of the **ENTRYID** structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02945-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="02945-106">Header file:</span></span>  <br/> |<span data-ttu-id="02945-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="02945-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="02945-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="02945-108">Related macros:</span></span>  <br/> |<span data-ttu-id="02945-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span><span class="sxs-lookup"><span data-stu-id="02945-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a><span data-ttu-id="02945-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="02945-110">Members</span></span>

 <span data-ttu-id="02945-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="02945-111">**cb**</span></span>
  
> <span data-ttu-id="02945-112">Die Anzahl der Bytes im **abEntry** -Element.</span><span class="sxs-lookup"><span data-stu-id="02945-112">Count of bytes in the **abEntry** member.</span></span> 
    
 <span data-ttu-id="02945-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="02945-113">**abEntry**</span></span>
  
> <span data-ttu-id="02945-114">Die vollständige Eintrags-ID, die das Array von Flags und Binärdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="02945-114">The complete entry identifier that includes the array of flags and binary data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="02945-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02945-115">Remarks</span></span>

<span data-ttu-id="02945-116">Eine **FLATENTRY** -Struktur ähnelt einer [Eintrags](entryid.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="02945-116">A **FLATENTRY** structure resembles an [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="02945-117">Es gibt jedoch einige Unterschiede:</span><span class="sxs-lookup"><span data-stu-id="02945-117">However, there are some differences:</span></span> 
  
- <span data-ttu-id="02945-118">Eine **FLATENTRY** -Struktur speichert die Größe des Eintrags Bezeichners; \*\*\*\* Die Eintrags-Nr.</span><span class="sxs-lookup"><span data-stu-id="02945-118">A **FLATENTRY** structure stores the size of the entry identifier; **ENTRYID** does not.</span></span> 
    
- <span data-ttu-id="02945-119">Eine **FLATENTRY** -Struktur speichert die kennzeichendaten zusammen mit dem Rest der Eintrags-ID. \*\*\*\* Sie wird separat gespeichert.</span><span class="sxs-lookup"><span data-stu-id="02945-119">A **FLATENTRY** structure stores the flag data together with the rest of the entry identifier; **ENTRYID** stores them separately.</span></span> 
    
- <span data-ttu-id="02945-120">Eine **FLATENTRY** -Struktur wird verwendet, um eine Eintrags-ID in einer Datei zu speichern oder in einem Stream von \*\*\*\* Bytes zu übertragen, während eine Eintragsstruktur von den [IMAPIProp](imapipropiunknown.md) -schnittstellenMethoden und von den folgenden OpenEntry-Methoden verwendet wird: \*\*\*\* [IABLogon: :](iablogon-openentry.md)OpenEntry, [IAddrBook::](iaddrbook-openentry.md)OpenEntry, [IMAPIContainer::](imapicontainer-openentry.md)OpenEntry, [IMAPISession::](imapisession-openentry.md)OpenEntry, [IMAPISupport::](imapisupport-openentry.md)OpenEntry, [IMsgStore::](imsgstore-openentry.md)OpenEntry, [IMSLogon:](imslogon-openentry.md) : OpenEntry</span><span class="sxs-lookup"><span data-stu-id="02945-120">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes whereas an **ENTRYID** structure is used by the [IMAPIProp](imapipropiunknown.md) interface methods and by the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="02945-121">Eine **FLATENTRY** -Struktur wird verwendet, um eine Eintrags-ID in einer Datei zu speichern oder in einem Stream von Bytes zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="02945-121">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> <span data-ttu-id="02945-122">Eine **Eintrags** Struktur wird verwendet, um eine Eintrags-ID auf dem Datenträger zu speichern.</span><span class="sxs-lookup"><span data-stu-id="02945-122">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="02945-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02945-123">See also</span></span>



[<span data-ttu-id="02945-124">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="02945-124">ENTRYID</span></span>](entryid.md)


[<span data-ttu-id="02945-125">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="02945-125">MAPI Structures</span></span>](mapi-structures.md)

