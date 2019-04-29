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
ms.openlocfilehash: 5605de7dbcc18197748713bcf909839690d7259f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411596"
---
# <a name="iid"></a><span data-ttu-id="61bd6-103">IID</span><span class="sxs-lookup"><span data-stu-id="61bd6-103">IID</span></span>

  
  
<span data-ttu-id="61bd6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61bd6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61bd6-105">Beschreibt eine [GUID](guid.md) -Struktur, die zur Beschreibung eines Bezeichners für eine MAPI-Schnittstelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="61bd6-105">Describes a [GUID](guid.md) structure used to describe an identifier for a MAPI interface.</span></span> 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="61bd6-106">Members</span><span class="sxs-lookup"><span data-stu-id="61bd6-106">Members</span></span>

<span data-ttu-id="61bd6-107">Siehe die **GUID** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="61bd6-107">See the **GUID** structure.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="61bd6-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61bd6-108">Remarks</span></span>

<span data-ttu-id="61bd6-109">Eine **IID** -Struktur wird verwendet, um eine MAPI-Schnittstelle eindeutig zu identifizieren und eine bestimmte Schnittstelle einem Objekt zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="61bd6-109">An **IID** structure is used to uniquely identify a MAPI interface and to associate a particular interface with an object.</span></span> <span data-ttu-id="61bd6-110">Wenn ein Client beispielsweise [IMAPISession:: OpenEntry](imapisession-openentry.md) zum Öffnen eines Ordners aufruft, wird der _lpInterface_ -Parameter so festgelegt, dass er auf eine **IID** zeigt, die die [IMAPIFolder](imapifolderimapicontainer.md) -Schnittstelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="61bd6-110">For example, when a client calls [IMAPISession::OpenEntry](imapisession-openentry.md) to open a folder, the client sets the  _lpInterface_ parameter to point to an **IID** representing the [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> <span data-ttu-id="61bd6-111">MAPI definiert die **IMAPIFolderIID** als IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="61bd6-111">MAPI defines the **IMAPIFolderIID** to be IID_IMAPIFolder.</span></span> <span data-ttu-id="61bd6-112">**IID** -Strukturen werden auch verwendet, um OLE-Schnittstellen eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="61bd6-112">**IID** structures are also used to uniquely identify OLE interfaces.</span></span> 
  
<span data-ttu-id="61bd6-113">Alle spezifischen **IID** -Strukturen für die MAPI-Schnittstellen sind in der Headerdatei Mapiguid. h definiert.</span><span class="sxs-lookup"><span data-stu-id="61bd6-113">All of the specific **IID** structures for the MAPI interfaces are defined in the Mapiguid.h header file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="61bd6-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61bd6-114">See also</span></span>



[<span data-ttu-id="61bd6-115">GUID</span><span class="sxs-lookup"><span data-stu-id="61bd6-115">GUID</span></span>](guid.md)


[<span data-ttu-id="61bd6-116">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="61bd6-116">MAPI Structures</span></span>](mapi-structures.md)

