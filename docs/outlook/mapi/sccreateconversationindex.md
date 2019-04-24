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
ms.openlocfilehash: 385660889c40e5f59dfc015ad92ce6a1398ab0cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351324"
---
# <a name="sccreateconversationindex"></a><span data-ttu-id="f447f-103">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="f447f-103">ScCreateConversationIndex</span></span>

  
  
<span data-ttu-id="f447f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f447f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f447f-105">Gibt an, wo in einem Nachrichtenthread eine Nachricht gehört.</span><span class="sxs-lookup"><span data-stu-id="f447f-105">Indicates where in a message thread a message belongs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f447f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f447f-106">Header file:</span></span>  <br/> |<span data-ttu-id="f447f-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="f447f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f447f-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f447f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f447f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f447f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f447f-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="f447f-110">Called by:</span></span>  <br/> |<span data-ttu-id="f447f-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f447f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a><span data-ttu-id="f447f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f447f-112">Parameters</span></span>

 <span data-ttu-id="f447f-113">_cbParent_</span><span class="sxs-lookup"><span data-stu-id="f447f-113">_cbParent_</span></span>
  
> <span data-ttu-id="f447f-114">in Die Anzahl der Bytes im übergeordneten Unterhaltungsindex.</span><span class="sxs-lookup"><span data-stu-id="f447f-114">[in] Count of bytes in the parent conversation index.</span></span>
    
 <span data-ttu-id="f447f-115">_lpbParent_</span><span class="sxs-lookup"><span data-stu-id="f447f-115">_lpbParent_</span></span>
  
> <span data-ttu-id="f447f-116">in Zeiger auf Bytes im übergeordneten Unterhaltungsindex.</span><span class="sxs-lookup"><span data-stu-id="f447f-116">[in] Pointer to bytes in the parent conversation index.</span></span> <span data-ttu-id="f447f-117">Dies ist möglicherweise NULL, wenn _cbParent_ NULL ist.</span><span class="sxs-lookup"><span data-stu-id="f447f-117">This may be NULL if  _cbParent_ is zero.</span></span> 
    
 <span data-ttu-id="f447f-118">_lpcbIndex_</span><span class="sxs-lookup"><span data-stu-id="f447f-118">_lpcbIndex_</span></span>
  
> <span data-ttu-id="f447f-119">Out Zeiger auf die Anzahl von Bytes im neuen unter Haltungs Index, der vom Aufruf zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f447f-119">[out] Pointer to the count of bytes in the new conversation index returned by the call.</span></span> 
    
 <span data-ttu-id="f447f-120">_lppbIndex_</span><span class="sxs-lookup"><span data-stu-id="f447f-120">_lppbIndex_</span></span>
  
> <span data-ttu-id="f447f-121">Out Zeiger auf einen Zeiger auf den neuen unter Haltungs Index, der vom Aufruf zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f447f-121">[out] Pointer to a pointer to the new conversation index returned by the call.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f447f-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f447f-122">Return value</span></span>

<span data-ttu-id="f447f-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="f447f-123">S_OK</span></span> 
  
> <span data-ttu-id="f447f-124">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="f447f-124">The call succeeded and has returned the expected value or values.</span></span>
    

