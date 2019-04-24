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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 12c50ab5936d7fffd364c276ba07ca69d3459ae7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299517"
---
# <a name="guid"></a><span data-ttu-id="fa67f-103">GUID</span><span class="sxs-lookup"><span data-stu-id="fa67f-103">GUID</span></span>

  
  
<span data-ttu-id="fa67f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa67f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa67f-105">Beschreibt eine GUID (Globally Unique Identifier).</span><span class="sxs-lookup"><span data-stu-id="fa67f-105">Describes a globally unique identifier (GUID).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fa67f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="fa67f-106">Header file:</span></span>  <br/> |<span data-ttu-id="fa67f-107">Mapiguid. h</span><span class="sxs-lookup"><span data-stu-id="fa67f-107">Mapiguid.h</span></span>  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="fa67f-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="fa67f-108">Members</span></span>

 <span data-ttu-id="fa67f-109">**Data1**</span><span class="sxs-lookup"><span data-stu-id="fa67f-109">**Data1**</span></span>
  
> <span data-ttu-id="fa67f-110">Ein Datenwert mit langer Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="fa67f-110">An unsigned long integer data value.</span></span>
    
 <span data-ttu-id="fa67f-111">**Data2**</span><span class="sxs-lookup"><span data-stu-id="fa67f-111">**Data2**</span></span>
  
> <span data-ttu-id="fa67f-112">Ein unsigned Short Integer-Datenwert.</span><span class="sxs-lookup"><span data-stu-id="fa67f-112">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="fa67f-113">**Data3**</span><span class="sxs-lookup"><span data-stu-id="fa67f-113">**Data3**</span></span>
  
> <span data-ttu-id="fa67f-114">Ein unsigned Short Integer-Datenwert.</span><span class="sxs-lookup"><span data-stu-id="fa67f-114">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="fa67f-115">**Data4**</span><span class="sxs-lookup"><span data-stu-id="fa67f-115">**Data4**</span></span>
  
> <span data-ttu-id="fa67f-116">Ein Array mit nicht signierten Zeichen.</span><span class="sxs-lookup"><span data-stu-id="fa67f-116">An array of unsigned characters.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fa67f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa67f-117">Remarks</span></span>

 <span data-ttu-id="fa67f-118">**GUID** -Strukturen werden in MAPI wie folgt verwendet:</span><span class="sxs-lookup"><span data-stu-id="fa67f-118">**GUID** structures are used in MAPI as follows:</span></span> 
  
- <span data-ttu-id="fa67f-119">In den [MAPIUID](mapiuid.md) -Strukturen, die Dienstanbieter eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fa67f-119">In the [MAPIUID](mapiuid.md) structures that uniquely identify service providers.</span></span> 
    
- <span data-ttu-id="fa67f-120">Für Schnittstellenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="fa67f-120">For interface identifiers.</span></span>
    
- <span data-ttu-id="fa67f-121">In den Eigenschaftensatz Namen benannter Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fa67f-121">In the property set names of named properties.</span></span> 
    
<span data-ttu-id="fa67f-122">Nachrichtenspeicher-und Adressbuchanbieter generieren eine **GUID** -Struktur, die in Ihrer **MAPIUID** -Struktur verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa67f-122">Message store and address book providers generate a **GUID** structure to use in their **MAPIUID** structure.</span></span> <span data-ttu-id="fa67f-123">Durch das Übergeben des resultierenden **MAPIUID** an [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md)informieren diese Dienstanbieter MAPI über Ihren eindeutigen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="fa67f-123">By passing the resulting **MAPIUID** to [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), these service providers inform MAPI of their unique identifier.</span></span>
  
<span data-ttu-id="fa67f-124">Außerdem werden Sie bei der Implementierung von Microsoft Remote Procedure Call (RPC) und der Object Description Language (ODL) verwendet.</span><span class="sxs-lookup"><span data-stu-id="fa67f-124">Also, they are used in the implementation of Microsoft Remote Procedure Call (RPC) and the Object Description Language (ODL).</span></span> <span data-ttu-id="fa67f-125">Weitere Informationen zu diesen Zwecken finden Sie im *Microsoft RPC Programmer es Guide and Reference*, *OLE Programmer es Reference* und *Inside OLE*, *Second Edition* .</span><span class="sxs-lookup"><span data-stu-id="fa67f-125">For more information about these uses, see the  *Microsoft RPC Programmer's Guide and Reference*, *OLE Programmer's Reference*  ,and  *Inside OLE*, *Second Edition*  .</span></span> 
  
<span data-ttu-id="fa67f-126">Die **GUID** -Struktur ist in der *Win32-Programmierreferenz* definiert.</span><span class="sxs-lookup"><span data-stu-id="fa67f-126">The **GUID** structure is defined in the  *Win32 Programmer's Reference*  .</span></span> <span data-ttu-id="fa67f-127">Bestimmte Werte für **GUID** -Strukturen, die in MAPI verwendet werden, sind in der MAPI-Headerdatei Mapiguid. h definiert.</span><span class="sxs-lookup"><span data-stu-id="fa67f-127">Specific values for **GUID** structures that are used within MAPI are defined in the MAPI header file Mapiguid.h.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fa67f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa67f-128">See also</span></span>



[<span data-ttu-id="fa67f-129">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="fa67f-129">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="fa67f-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="fa67f-130">MAPI Structures</span></span>](mapi-structures.md)

