---
title: FEqualNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FEqualNames
api_type:
- COM
ms.assetid: 4dd58b0b-dc39-4782-a9ec-05e353c90927
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 09c6540f2a224b7dc89a62c34cfb0c867cef4632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570849"
---
# <a name="fequalnames"></a><span data-ttu-id="2f592-103">FEqualNames</span><span class="sxs-lookup"><span data-stu-id="2f592-103">FEqualNames</span></span>

  
  
<span data-ttu-id="2f592-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f592-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f592-105">Bestimmt, ob zwei MAPI benannte Eigenschaften sind identisch.</span><span class="sxs-lookup"><span data-stu-id="2f592-105">Determines whether two MAPI named properties are the same.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f592-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="2f592-106">Header file:</span></span>  <br/> |<span data-ttu-id="2f592-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2f592-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2f592-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="2f592-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2f592-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2f592-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2f592-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="2f592-110">Called by:</span></span>  <br/> |<span data-ttu-id="2f592-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="2f592-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a><span data-ttu-id="2f592-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f592-112">Parameters</span></span>

 <span data-ttu-id="2f592-113">_lpName1_</span><span class="sxs-lookup"><span data-stu-id="2f592-113">_lpName1_</span></span>
  
> <span data-ttu-id="2f592-114">[in] Zeiger auf eine [MAPINAMEID](mapinameid.md) -Struktur, die die erste benannte Eigenschaft beschreibt.</span><span class="sxs-lookup"><span data-stu-id="2f592-114">[in] Pointer to a [MAPINAMEID](mapinameid.md) structure describing the first named property.</span></span> 
    
 <span data-ttu-id="2f592-115">_lpName2_</span><span class="sxs-lookup"><span data-stu-id="2f592-115">_lpName2_</span></span>
  
> <span data-ttu-id="2f592-116">[in] Zeiger auf eine **MAPINAMEID** -Struktur, die zweite benannte Eigenschaft beschreibt.</span><span class="sxs-lookup"><span data-stu-id="2f592-116">[in] Pointer to a **MAPINAMEID** structure describing the second named property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2f592-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="2f592-117">Return value</span></span>

<span data-ttu-id="2f592-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="2f592-118">TRUE</span></span> 
  
> <span data-ttu-id="2f592-119">Die zwei Eigenschaftennamen sind gleich.</span><span class="sxs-lookup"><span data-stu-id="2f592-119">The two property names are equal.</span></span> 
    
<span data-ttu-id="2f592-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="2f592-120">FALSE</span></span> 
  
> <span data-ttu-id="2f592-121">Die zwei Eigenschaftennamen sind nicht gleich.</span><span class="sxs-lookup"><span data-stu-id="2f592-121">The two property names are not equal.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2f592-122">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="2f592-122">Remarks</span></span>

<span data-ttu-id="2f592-123">Die **FEqualNames** -Funktion ist nützlich, da die **MAPINAMEID** Struktur eine [GUID enthält](guid.md) und der Name der Eigenschaft selbst in mehr als eine Möglichkeit darstellen kann.</span><span class="sxs-lookup"><span data-stu-id="2f592-123">The **FEqualNames** function is useful because the **MAPINAMEID** structure contains a [GUID](guid.md) and can represent the property name itself in more than one way.</span></span> <span data-ttu-id="2f592-124">Dies bedeutet, dass die zwei Strukturen nicht durch einfache binäre Methoden verglichen werden können.</span><span class="sxs-lookup"><span data-stu-id="2f592-124">This means the two structures cannot be compared by simple binary methods.</span></span> 
  
<span data-ttu-id="2f592-125">Testvorgang beachtet werden für die Eigenschaft Namenszeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="2f592-125">The testing process is case-sensitive for the property name strings.</span></span> 
  

