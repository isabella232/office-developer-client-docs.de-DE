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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 385660889c40e5f59dfc015ad92ce6a1398ab0cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415656"
---
# <a name="sccreateconversationindex"></a><span data-ttu-id="d7898-103">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="d7898-103">ScCreateConversationIndex</span></span>

  
  
<span data-ttu-id="d7898-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7898-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7898-105">Gibt an, wo in einem Nachrichtenthread eine Nachricht gehört.</span><span class="sxs-lookup"><span data-stu-id="d7898-105">Indicates where in a message thread a message belongs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d7898-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d7898-106">Header file:</span></span>  <br/> |<span data-ttu-id="d7898-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="d7898-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d7898-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="d7898-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d7898-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d7898-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d7898-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="d7898-110">Called by:</span></span>  <br/> |<span data-ttu-id="d7898-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="d7898-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a><span data-ttu-id="d7898-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7898-112">Parameters</span></span>

 <span data-ttu-id="d7898-113">_cbParent_</span><span class="sxs-lookup"><span data-stu-id="d7898-113">_cbParent_</span></span>
  
> <span data-ttu-id="d7898-114">in Die Anzahl der Bytes im übergeordneten Unterhaltungsindex.</span><span class="sxs-lookup"><span data-stu-id="d7898-114">[in] Count of bytes in the parent conversation index.</span></span>
    
 <span data-ttu-id="d7898-115">_lpbParent_</span><span class="sxs-lookup"><span data-stu-id="d7898-115">_lpbParent_</span></span>
  
> <span data-ttu-id="d7898-116">in Zeiger auf Bytes im übergeordneten Unterhaltungsindex.</span><span class="sxs-lookup"><span data-stu-id="d7898-116">[in] Pointer to bytes in the parent conversation index.</span></span> <span data-ttu-id="d7898-117">Dies ist möglicherweise NULL, wenn _cbParent_ NULL ist.</span><span class="sxs-lookup"><span data-stu-id="d7898-117">This may be NULL if  _cbParent_ is zero.</span></span> 
    
 <span data-ttu-id="d7898-118">_lpcbIndex_</span><span class="sxs-lookup"><span data-stu-id="d7898-118">_lpcbIndex_</span></span>
  
> <span data-ttu-id="d7898-119">Out Zeiger auf die Anzahl von Bytes im neuen unter Haltungs Index, der vom Aufruf zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d7898-119">[out] Pointer to the count of bytes in the new conversation index returned by the call.</span></span> 
    
 <span data-ttu-id="d7898-120">_lppbIndex_</span><span class="sxs-lookup"><span data-stu-id="d7898-120">_lppbIndex_</span></span>
  
> <span data-ttu-id="d7898-121">Out Zeiger auf einen Zeiger auf den neuen unter Haltungs Index, der vom Aufruf zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d7898-121">[out] Pointer to a pointer to the new conversation index returned by the call.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d7898-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7898-122">Return value</span></span>

<span data-ttu-id="d7898-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="d7898-123">S_OK</span></span> 
  
> <span data-ttu-id="d7898-124">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="d7898-124">The call succeeded and has returned the expected value or values.</span></span>
    

