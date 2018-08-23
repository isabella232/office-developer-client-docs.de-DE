---
title: GUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GUID
api_type:
- COM
ms.assetid: e3608c47-06be-4476-a6ef-060fac252387
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 94bafdf0ca84fa31a7df2f022265d5d5d1a99a37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577695"
---
# <a name="guid"></a><span data-ttu-id="bc1f2-103">GUID</span><span class="sxs-lookup"><span data-stu-id="bc1f2-103">GUID</span></span>

  
  
<span data-ttu-id="bc1f2-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc1f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc1f2-105">Beschreibt einen global eindeutigen Bezeichner (GUID).</span><span class="sxs-lookup"><span data-stu-id="bc1f2-105">Describes a globally unique identifier (GUID).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc1f2-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="bc1f2-106">Header file:</span></span>  <br/> |<span data-ttu-id="bc1f2-107">Mapiguid.h</span><span class="sxs-lookup"><span data-stu-id="bc1f2-107">Mapiguid.h</span></span>  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="bc1f2-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="bc1f2-108">Members</span></span>

 <span data-ttu-id="bc1f2-109">**Data1**</span><span class="sxs-lookup"><span data-stu-id="bc1f2-109">**Data1**</span></span>
  
> <span data-ttu-id="bc1f2-110">Eine lange Ganzzahl ohne Vorzeichen Datenwert.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-110">An unsigned long integer data value.</span></span>
    
 <span data-ttu-id="bc1f2-111">**Data2**</span><span class="sxs-lookup"><span data-stu-id="bc1f2-111">**Data2**</span></span>
  
> <span data-ttu-id="bc1f2-112">Eine ganze Zahl ohne Vorzeichen kurzen Datenwert.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-112">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="bc1f2-113">**Data3**</span><span class="sxs-lookup"><span data-stu-id="bc1f2-113">**Data3**</span></span>
  
> <span data-ttu-id="bc1f2-114">Eine ganze Zahl ohne Vorzeichen kurzen Datenwert.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-114">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="bc1f2-115">**Data4**</span><span class="sxs-lookup"><span data-stu-id="bc1f2-115">**Data4**</span></span>
  
> <span data-ttu-id="bc1f2-116">Ein Array von nicht signierte Zeichen.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-116">An array of unsigned characters.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bc1f2-117">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="bc1f2-117">Remarks</span></span>

 <span data-ttu-id="bc1f2-118">**GUID** -Strukturen werden in MAPI wie folgt verwendet:</span><span class="sxs-lookup"><span data-stu-id="bc1f2-118">**GUID** structures are used in MAPI as follows:</span></span> 
  
- <span data-ttu-id="bc1f2-119">In den [MAPIUID](mapiuid.md) -Strukturen, mit die Dienstanbieter eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-119">In the [MAPIUID](mapiuid.md) structures that uniquely identify service providers.</span></span> 
    
- <span data-ttu-id="bc1f2-120">Schnittstelle-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-120">For interface identifiers.</span></span>
    
- <span data-ttu-id="bc1f2-121">Legen in die Eigenschaft Namen der benannten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-121">In the property set names of named properties.</span></span> 
    
<span data-ttu-id="bc1f2-122">Nachrichtenspeicher und Adresse adressbuchanbietern implementierte generieren eine **GUID** -Struktur, die in ihrer **MAPIUID** Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-122">Message store and address book providers generate a **GUID** structure to use in their **MAPIUID** structure.</span></span> <span data-ttu-id="bc1f2-123">Informieren Sie, indem Sie die resultierende **MAPIUID** an [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)übergeben, dieser Dienstanbieter MAPI der jeweiligen eindeutigen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-123">By passing the resulting **MAPIUID** to [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), these service providers inform MAPI of their unique identifier.</span></span>
  
<span data-ttu-id="bc1f2-124">Darüber hinaus werden sie in der Implementierung von Microsoft Remote Procedure Call (RPC) sowie dem Objekt Description Language () verwendet.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-124">Also, they are used in the implementation of Microsoft Remote Procedure Call (RPC) and the Object Description Language (ODL).</span></span> <span data-ttu-id="bc1f2-125">Weitere Informationen zu diesen verwendet finden Sie unter der *Microsoft RPC Programmer's Guide und Verweis* *OLE Programmer's Reference* und *In OLE*, *Second Edition* .</span><span class="sxs-lookup"><span data-stu-id="bc1f2-125">For more information about these uses, see the  *Microsoft RPC Programmer's Guide and Reference*, *OLE Programmer's Reference*  ,and  *Inside OLE*, *Second Edition*  .</span></span> 
  
<span data-ttu-id="bc1f2-126">Die **GUID** -Struktur ist in der *Win32 Programmer's Reference* definiert.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-126">The **GUID** structure is defined in the  *Win32 Programmer's Reference*  .</span></span> <span data-ttu-id="bc1f2-127">Konkrete Werte für die **GUID** -Strukturen, die in MAPI verwendet werden, werden in der MAPI-Headerdatei Mapiguid.h definiert.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-127">Specific values for **GUID** structures that are used within MAPI are defined in the MAPI header file Mapiguid.h.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bc1f2-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc1f2-128">See also</span></span>



[<span data-ttu-id="bc1f2-129">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="bc1f2-129">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="bc1f2-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="bc1f2-130">MAPI Structures</span></span>](mapi-structures.md)

