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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417203"
---
# <a name="mscap_selector"></a><span data-ttu-id="8de8a-103">MSCAP_SELECTOR</span><span class="sxs-lookup"><span data-stu-id="8de8a-103">MSCAP_SELECTOR</span></span>

  
  
<span data-ttu-id="8de8a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8de8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8de8a-105">Gibt die Funktionen an, die für einen Speicher zurückzukehren sind.</span><span class="sxs-lookup"><span data-stu-id="8de8a-105">Specifies the capabilities to return for a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8de8a-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="8de8a-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="8de8a-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="8de8a-107">Members</span></span>

 <span data-ttu-id="8de8a-108">*MSCAP_SEL_RESERVED1*</span><span class="sxs-lookup"><span data-stu-id="8de8a-108">*MSCAP_SEL_RESERVED1*</span></span> 
  
> <span data-ttu-id="8de8a-109">Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8de8a-109">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="8de8a-110">*MSCAP_SEL_RESERVED2*</span><span class="sxs-lookup"><span data-stu-id="8de8a-110">*MSCAP_SEL_RESERVED2*</span></span> 
  
> <span data-ttu-id="8de8a-111">Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8de8a-111">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="8de8a-112">*MSCAP_SEL_FOLDER*</span><span class="sxs-lookup"><span data-stu-id="8de8a-112">*MSCAP_SEL_FOLDER*</span></span> 
  
> <span data-ttu-id="8de8a-113">Funktionen zum Unterstützen von Ordnern in einem Speicher.</span><span class="sxs-lookup"><span data-stu-id="8de8a-113">Capabilities about supporting folders on a store.</span></span>
    
 <span data-ttu-id="8de8a-114">*MSCAP_SEL_RESERVED3*</span><span class="sxs-lookup"><span data-stu-id="8de8a-114">*MSCAP_SEL_RESERVED3*</span></span> 
  
> <span data-ttu-id="8de8a-115">Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8de8a-115">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="8de8a-116">*MSCAP_SEL_RESTRICTION*</span><span class="sxs-lookup"><span data-stu-id="8de8a-116">*MSCAP_SEL_RESTRICTION*</span></span> 
  
> <span data-ttu-id="8de8a-117">Funktionen zur Unterstützung von Einschränkungen für einen Store.</span><span class="sxs-lookup"><span data-stu-id="8de8a-117">Capabilities about supporting restrictions on a store.</span></span>
    

