---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 420b2661e766ecf97a5e9e488e9c18f29cd91329
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19793268"
---
# <a name="mscapselector"></a><span data-ttu-id="dbf26-103">MSCAP_SELECTOR</span><span class="sxs-lookup"><span data-stu-id="dbf26-103">MSCAP_SELECTOR</span></span>

  
  
<span data-ttu-id="dbf26-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dbf26-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dbf26-105">Gibt an, das die Funktionen für einen Speicher zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dbf26-105">Specifies the capabilities to return for a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="dbf26-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="dbf26-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="dbf26-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="dbf26-107">Members</span></span>

 <span data-ttu-id="dbf26-108">*MSCAP_SEL_RESERVED1*</span><span class="sxs-lookup"><span data-stu-id="dbf26-108">*MSCAP_SEL_RESERVED1*</span></span> 
  
> <span data-ttu-id="dbf26-109">Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dbf26-109">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="dbf26-110">*MSCAP_SEL_RESERVED2*</span><span class="sxs-lookup"><span data-stu-id="dbf26-110">*MSCAP_SEL_RESERVED2*</span></span> 
  
> <span data-ttu-id="dbf26-111">Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dbf26-111">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="dbf26-112">*MSCAP_SEL_FOLDER*</span><span class="sxs-lookup"><span data-stu-id="dbf26-112">*MSCAP_SEL_FOLDER*</span></span> 
  
> <span data-ttu-id="dbf26-113">Funktionen zur Unterstützung von Ordnern in einem Speicher.</span><span class="sxs-lookup"><span data-stu-id="dbf26-113">Capabilities about supporting folders on a store.</span></span>
    
 <span data-ttu-id="dbf26-114">*MSCAP_SEL_RESERVED3*</span><span class="sxs-lookup"><span data-stu-id="dbf26-114">*MSCAP_SEL_RESERVED3*</span></span> 
  
> <span data-ttu-id="dbf26-115">Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dbf26-115">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="dbf26-116">*MSCAP_SEL_RESTRICTION*</span><span class="sxs-lookup"><span data-stu-id="dbf26-116">*MSCAP_SEL_RESTRICTION*</span></span> 
  
> <span data-ttu-id="dbf26-117">Funktionen zur Unterstützung von Einschränkungen in einem Speicher.</span><span class="sxs-lookup"><span data-stu-id="dbf26-117">Capabilities about supporting restrictions on a store.</span></span>
    

