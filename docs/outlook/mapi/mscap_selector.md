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
ms.openlocfilehash: 9c5d8ab5bbac91250f3b8c552ad891c62134526e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338675"
---
# <a name="mscapselector"></a><span data-ttu-id="5c824-103">MSCAP_SELECTOR</span><span class="sxs-lookup"><span data-stu-id="5c824-103">MSCAP_SELECTOR</span></span>

  
  
<span data-ttu-id="5c824-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c824-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c824-105">Gibt die Funktionen an, die für einen Speicher zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5c824-105">Specifies the capabilities to return for a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5c824-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="5c824-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="5c824-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="5c824-107">Members</span></span>

 <span data-ttu-id="5c824-108">*MSCAP_SEL_RESERVED1*</span><span class="sxs-lookup"><span data-stu-id="5c824-108">*MSCAP_SEL_RESERVED1*</span></span> 
  
> <span data-ttu-id="5c824-109">Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5c824-109">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="5c824-110">*MSCAP_SEL_RESERVED2*</span><span class="sxs-lookup"><span data-stu-id="5c824-110">*MSCAP_SEL_RESERVED2*</span></span> 
  
> <span data-ttu-id="5c824-111">Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5c824-111">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="5c824-112">*MSCAP_SEL_FOLDER*</span><span class="sxs-lookup"><span data-stu-id="5c824-112">*MSCAP_SEL_FOLDER*</span></span> 
  
> <span data-ttu-id="5c824-113">Funktionen zur Unterstützung von Ordnern in einem Speicher.</span><span class="sxs-lookup"><span data-stu-id="5c824-113">Capabilities about supporting folders on a store.</span></span>
    
 <span data-ttu-id="5c824-114">*MSCAP_SEL_RESERVED3*</span><span class="sxs-lookup"><span data-stu-id="5c824-114">*MSCAP_SEL_RESERVED3*</span></span> 
  
> <span data-ttu-id="5c824-115">Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5c824-115">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="5c824-116">*MSCAP_SEL_RESTRICTION*</span><span class="sxs-lookup"><span data-stu-id="5c824-116">*MSCAP_SEL_RESTRICTION*</span></span> 
  
> <span data-ttu-id="5c824-117">Funktionen zur Unterstützung von Einschränkungen in einem Speicher.</span><span class="sxs-lookup"><span data-stu-id="5c824-117">Capabilities about supporting restrictions on a store.</span></span>
    

