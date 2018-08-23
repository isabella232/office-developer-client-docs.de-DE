---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8c23788d64fe3703c7c46998cade0bd40d2f3dd2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588125"
---
# <a name="mscapselector"></a><span data-ttu-id="a07af-103">MSCAP_SELECTOR</span><span class="sxs-lookup"><span data-stu-id="a07af-103">MSCAP_SELECTOR</span></span>

  
  
<span data-ttu-id="a07af-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a07af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a07af-105">Gibt an, das die Funktionen für einen Speicher zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a07af-105">Specifies the capabilities to return for a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a07af-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="a07af-106">Quick info</span></span>

```cpp
typedef enum 
{ 
    MSCAP_SEL_RESERVED1 = 0, 
    MSCAP_SEL_RESERVED2, 
    MSCAP_SEL_FOLDER, 
    MSCAP_SEL_RESERVED3, 
    MSCAP_SEL_RESTRICTION, 
} MSCAP_SELECTOR;
```

## <a name="members"></a><span data-ttu-id="a07af-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="a07af-107">Members</span></span>

 <span data-ttu-id="a07af-108">*MSCAP_SEL_RESERVED1*</span><span class="sxs-lookup"><span data-stu-id="a07af-108">*MSCAP_SEL_RESERVED1*</span></span> 
  
> <span data-ttu-id="a07af-109">Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a07af-109">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="a07af-110">*MSCAP_SEL_RESERVED2*</span><span class="sxs-lookup"><span data-stu-id="a07af-110">*MSCAP_SEL_RESERVED2*</span></span> 
  
> <span data-ttu-id="a07af-111">Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a07af-111">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="a07af-112">*MSCAP_SEL_FOLDER*</span><span class="sxs-lookup"><span data-stu-id="a07af-112">*MSCAP_SEL_FOLDER*</span></span> 
  
> <span data-ttu-id="a07af-113">Funktionen zur Unterstützung von Ordnern in einem Speicher.</span><span class="sxs-lookup"><span data-stu-id="a07af-113">Capabilities about supporting folders on a store.</span></span>
    
 <span data-ttu-id="a07af-114">*MSCAP_SEL_RESERVED3*</span><span class="sxs-lookup"><span data-stu-id="a07af-114">*MSCAP_SEL_RESERVED3*</span></span> 
  
> <span data-ttu-id="a07af-115">Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a07af-115">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="a07af-116">*MSCAP_SEL_RESTRICTION*</span><span class="sxs-lookup"><span data-stu-id="a07af-116">*MSCAP_SEL_RESTRICTION*</span></span> 
  
> <span data-ttu-id="a07af-117">Funktionen zur Unterstützung von Einschränkungen in einem Speicher.</span><span class="sxs-lookup"><span data-stu-id="a07af-117">Capabilities about supporting restrictions on a store.</span></span>
    

