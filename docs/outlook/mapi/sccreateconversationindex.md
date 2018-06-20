---
title: ScCreateConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCreateConversationIndex
api_type:
- COM
ms.assetid: 3ccfc15d-f3c6-4c7b-b1cc-855af66036de
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 43765cddb2f06bfbe58e0a4000c7eadfdc5f3347
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795454"
---
# <a name="sccreateconversationindex"></a><span data-ttu-id="01f81-103">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="01f81-103">ScCreateConversationIndex</span></span>

  
  
<span data-ttu-id="01f81-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="01f81-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="01f81-105">Gibt an, in dem in einem Thread Nachricht eine Nachricht gehört.</span><span class="sxs-lookup"><span data-stu-id="01f81-105">Indicates where in a message thread a message belongs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01f81-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="01f81-106">Header file:</span></span>  <br/> |<span data-ttu-id="01f81-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="01f81-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="01f81-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="01f81-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="01f81-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="01f81-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="01f81-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="01f81-110">Called by:</span></span>  <br/> |<span data-ttu-id="01f81-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="01f81-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a><span data-ttu-id="01f81-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="01f81-112">Parameters</span></span>

 <span data-ttu-id="01f81-113">_cbParent_</span><span class="sxs-lookup"><span data-stu-id="01f81-113">_cbParent_</span></span>
  
> <span data-ttu-id="01f81-114">[in] Anzahl der Bytes in der übergeordneten Unterhaltung Index.</span><span class="sxs-lookup"><span data-stu-id="01f81-114">[in] Count of bytes in the parent conversation index.</span></span>
    
 <span data-ttu-id="01f81-115">_lpbParent_</span><span class="sxs-lookup"><span data-stu-id="01f81-115">_lpbParent_</span></span>
  
> <span data-ttu-id="01f81-116">[in] Zeiger auf Bytes im übergeordneten Unterhaltung Index.</span><span class="sxs-lookup"><span data-stu-id="01f81-116">[in] Pointer to bytes in the parent conversation index.</span></span> <span data-ttu-id="01f81-117">Dies kann NULL sein, wenn _CbParent_ gleich NULL ist.</span><span class="sxs-lookup"><span data-stu-id="01f81-117">This may be NULL if  _cbParent_ is zero.</span></span> 
    
 <span data-ttu-id="01f81-118">_lpcbIndex_</span><span class="sxs-lookup"><span data-stu-id="01f81-118">_lpcbIndex_</span></span>
  
> <span data-ttu-id="01f81-119">[out] Zeiger auf die Anzahl der Bytes in den neuen Unterhaltung Index durch den Aufruf zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="01f81-119">[out] Pointer to the count of bytes in the new conversation index returned by the call.</span></span> 
    
 <span data-ttu-id="01f81-120">_lppbIndex_</span><span class="sxs-lookup"><span data-stu-id="01f81-120">_lppbIndex_</span></span>
  
> <span data-ttu-id="01f81-121">[out] Zeiger auf einen Zeiger auf den neuen Unterhaltung Index durch den Aufruf zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="01f81-121">[out] Pointer to a pointer to the new conversation index returned by the call.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="01f81-122">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="01f81-122">Return value</span></span>

<span data-ttu-id="01f81-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="01f81-123">S_OK</span></span> 
  
> <span data-ttu-id="01f81-124">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="01f81-124">The call succeeded and has returned the expected value or values.</span></span>
    

