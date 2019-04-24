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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8f71b30bd02af8f768da86218456feadda8ea1b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334881"
---
# <a name="fequalnames"></a><span data-ttu-id="1aeac-103">FEqualNames</span><span class="sxs-lookup"><span data-stu-id="1aeac-103">FEqualNames</span></span>

  
  
<span data-ttu-id="1aeac-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1aeac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1aeac-105">Bestimmt, ob zwei MAPI-benannte Eigenschaften identisch sind.</span><span class="sxs-lookup"><span data-stu-id="1aeac-105">Determines whether two MAPI named properties are the same.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1aeac-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="1aeac-106">Header file:</span></span>  <br/> |<span data-ttu-id="1aeac-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="1aeac-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1aeac-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="1aeac-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1aeac-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1aeac-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1aeac-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="1aeac-110">Called by:</span></span>  <br/> |<span data-ttu-id="1aeac-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="1aeac-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a><span data-ttu-id="1aeac-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1aeac-112">Parameters</span></span>

 <span data-ttu-id="1aeac-113">_lpName1_</span><span class="sxs-lookup"><span data-stu-id="1aeac-113">_lpName1_</span></span>
  
> <span data-ttu-id="1aeac-114">in Zeiger auf eine [MAPINAMEID](mapinameid.md) -Struktur, die die erste benannte Eigenschaft beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1aeac-114">[in] Pointer to a [MAPINAMEID](mapinameid.md) structure describing the first named property.</span></span> 
    
 <span data-ttu-id="1aeac-115">_lpName2_</span><span class="sxs-lookup"><span data-stu-id="1aeac-115">_lpName2_</span></span>
  
> <span data-ttu-id="1aeac-116">in Zeiger auf eine **MAPINAMEID** -Struktur, die die zweite benannte Eigenschaft beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1aeac-116">[in] Pointer to a **MAPINAMEID** structure describing the second named property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1aeac-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1aeac-117">Return value</span></span>

<span data-ttu-id="1aeac-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="1aeac-118">TRUE</span></span> 
  
> <span data-ttu-id="1aeac-119">Die beiden Eigenschaftennamen sind gleich.</span><span class="sxs-lookup"><span data-stu-id="1aeac-119">The two property names are equal.</span></span> 
    
<span data-ttu-id="1aeac-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="1aeac-120">FALSE</span></span> 
  
> <span data-ttu-id="1aeac-121">Die beiden Eigenschaftennamen sind ungleich.</span><span class="sxs-lookup"><span data-stu-id="1aeac-121">The two property names are not equal.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1aeac-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1aeac-122">Remarks</span></span>

<span data-ttu-id="1aeac-123">Die **FEqualNames** -Funktion ist nützlich, da die **MAPINAMEID** -Struktur eine [GUID](guid.md) enthält und den Eigenschaftennamen selbst auf mehrere Weise darstellen kann.</span><span class="sxs-lookup"><span data-stu-id="1aeac-123">The **FEqualNames** function is useful because the **MAPINAMEID** structure contains a [GUID](guid.md) and can represent the property name itself in more than one way.</span></span> <span data-ttu-id="1aeac-124">Dies führt dazu, dass die beiden Strukturen nicht mit einfachen binären Methoden verglichen werden können.</span><span class="sxs-lookup"><span data-stu-id="1aeac-124">This means the two structures cannot be compared by simple binary methods.</span></span> 
  
<span data-ttu-id="1aeac-125">Bei dem Testvorgang wird die Groß-/Kleinschreibung für die Eigenschaftennamen Zeichenfolgen beachtet.</span><span class="sxs-lookup"><span data-stu-id="1aeac-125">The testing process is case-sensitive for the property name strings.</span></span> 
  

