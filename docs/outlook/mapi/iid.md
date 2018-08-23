---
title: IID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IID
api_type:
- COM
ms.assetid: fa5498ab-2f8a-42f8-ba9d-1d555768594f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 00c7560427ece58026030ce6895d60aec7cc5a2e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570940"
---
# <a name="iid"></a><span data-ttu-id="691b9-103">IID</span><span class="sxs-lookup"><span data-stu-id="691b9-103">IID</span></span>

  
  
<span data-ttu-id="691b9-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="691b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="691b9-105">Beschreibt eine [GUID](guid.md) -Struktur verwendet, um einen Bezeichner für die MAPI-Schnittstelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="691b9-105">Describes a [GUID](guid.md) structure used to describe an identifier for a MAPI interface.</span></span> 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="691b9-106">Elemente</span><span class="sxs-lookup"><span data-stu-id="691b9-106">Members</span></span>

<span data-ttu-id="691b9-107">Finden Sie unter der **GUID** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="691b9-107">See the **GUID** structure.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="691b9-108">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="691b9-108">Remarks</span></span>

<span data-ttu-id="691b9-109">Eine **IID** -Struktur dient zur eindeutigen Identifizierung eine MAPI-Schnittstelle und ein Objekt eine bestimmte Schnittstelle zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="691b9-109">An **IID** structure is used to uniquely identify a MAPI interface and to associate a particular interface with an object.</span></span> <span data-ttu-id="691b9-110">Beispielsweise legt fest, wenn eine Client-Anrufe [IMAPISession::OpenEntry](imapisession-openentry.md) an einen Ordner zu öffnen, der Client den _LpInterface_ -Parameter auf **IID** zeigen, das [IMAPIFolder](imapifolderimapicontainer.md) Schnittstelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="691b9-110">For example, when a client calls [IMAPISession::OpenEntry](imapisession-openentry.md) to open a folder, the client sets the  _lpInterface_ parameter to point to an **IID** representing the [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> <span data-ttu-id="691b9-111">MAPI definiert die **IMAPIFolderIID** um IID_IMAPIFolder werden.</span><span class="sxs-lookup"><span data-stu-id="691b9-111">MAPI defines the **IMAPIFolderIID** to be IID_IMAPIFolder.</span></span> <span data-ttu-id="691b9-112">**IID** Strukturen werden auch verwendet, um OLE-Schnittstellen eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="691b9-112">**IID** structures are also used to uniquely identify OLE interfaces.</span></span> 
  
<span data-ttu-id="691b9-113">Alle von der bestimmten **IID** Strukturen für die MAPI-Schnittstellen werden in der Headerdatei Mapiguid.h definiert.</span><span class="sxs-lookup"><span data-stu-id="691b9-113">All of the specific **IID** structures for the MAPI interfaces are defined in the Mapiguid.h header file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="691b9-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="691b9-114">See also</span></span>



[<span data-ttu-id="691b9-115">GUID</span><span class="sxs-lookup"><span data-stu-id="691b9-115">GUID</span></span>](guid.md)


[<span data-ttu-id="691b9-116">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="691b9-116">MAPI Structures</span></span>](mapi-structures.md)

