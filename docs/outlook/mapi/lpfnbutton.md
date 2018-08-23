---
title: LPFNBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPFNBUTTON
api_type:
- COM
ms.assetid: cb91ae1d-1ea8-4f02-a1f1-f2a356a71477
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3b302de68f27e85c67430f82bd3e2c33009600e9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591352"
---
# <a name="lpfnbutton"></a><span data-ttu-id="2d89a-103">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="2d89a-103">LPFNBUTTON</span></span>

  
  
<span data-ttu-id="2d89a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d89a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d89a-105">Definiert eine Rückruffunktion, die MAPI-aufrufen, um ein optional Schaltflächensteuerelement im Dialogfeld Adressbuch eine Adresse zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2d89a-105">Defines a callback function that MAPI calls to activate an optional button control in an address book dialog box.</span></span> <span data-ttu-id="2d89a-106">Diese Schaltfläche ist in der Regel eine Schaltfläche **Details** .</span><span class="sxs-lookup"><span data-stu-id="2d89a-106">This button is typically a **Details** button.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2d89a-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="2d89a-107">Header file:</span></span>  <br/> |<span data-ttu-id="2d89a-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2d89a-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2d89a-109">Definierte Funktion von implementiert:</span><span class="sxs-lookup"><span data-stu-id="2d89a-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="2d89a-110">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="2d89a-110">Service providers</span></span>  <br/> |
|<span data-ttu-id="2d89a-111">Definierte Funktion aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="2d89a-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="2d89a-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="2d89a-112">MAPI</span></span>  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="2d89a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d89a-113">Parameters</span></span>

 <span data-ttu-id="2d89a-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="2d89a-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="2d89a-115">[in] Behandeln von der übergeordneten Windows für alle Dialogfelder oder Fenster, die diese Funktion zeigt.</span><span class="sxs-lookup"><span data-stu-id="2d89a-115">[in] Handle of the parent windows for any dialog boxes or windows this function displays.</span></span>
    
 <span data-ttu-id="2d89a-116">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="2d89a-116">_lpvContext_</span></span>
  
> <span data-ttu-id="2d89a-117">[in] Zeiger auf einen beliebigen Wert wird an die Rückruffunktion übergeben, wenn MAPI aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2d89a-117">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="2d89a-118">Dieser Wert kann eine an die Clientanwendung Vielfache von-Adresse dar.</span><span class="sxs-lookup"><span data-stu-id="2d89a-118">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="2d89a-119">In der Regel stellt _LpvContext_ für C++-Code einen Zeiger auf ein C++-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2d89a-119">Typically, for C++ code,  _lpvContext_ represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="2d89a-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="2d89a-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="2d89a-121">[in] Größe des Eintrags-ID, die auf das durch den Parameter _LpSelection_ in Bytes.</span><span class="sxs-lookup"><span data-stu-id="2d89a-121">[in] Size, in bytes, of the entry identifier pointed to by the  _lpSelection_ parameter.</span></span> 
    
 <span data-ttu-id="2d89a-122">_lpSelection_</span><span class="sxs-lookup"><span data-stu-id="2d89a-122">_lpSelection_</span></span>
  
> <span data-ttu-id="2d89a-123">[in] Zeiger auf die Eintrags-ID die Auswahl im Dialogfeld definieren.</span><span class="sxs-lookup"><span data-stu-id="2d89a-123">[in] Pointer to the entry identifier defining the selection in the dialog box.</span></span>
    
 <span data-ttu-id="2d89a-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2d89a-124">_ulFlags_</span></span>
  
> <span data-ttu-id="2d89a-125">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="2d89a-125">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2d89a-126">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="2d89a-126">Return value</span></span>

<span data-ttu-id="2d89a-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="2d89a-127">S_OK</span></span> 
  
> <span data-ttu-id="2d89a-128">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="2d89a-128">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2d89a-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2d89a-129">Remarks</span></span>

<span data-ttu-id="2d89a-130">Clientanwendungen rufen Sie eine Rückruffunktion basierend auf den **LPFNBUTTON** Prototyp so definieren Sie eine Schaltfläche in einem Dialogfeld Details.</span><span class="sxs-lookup"><span data-stu-id="2d89a-130">Client applications call a callback function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="2d89a-131">Der Client übergibt einen Zeiger auf die Callback-Funktion in der [IAddrBook::Details](iaddrbook-details.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2d89a-131">The client passes a pointer to the callback function in calls to the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="2d89a-132">Dienstanbieter anrufen basierte auf den **LPFNBUTTON** Prototyp so definieren Sie eine Schaltfläche in einem Dialogfeld Details Hook-Funktion.</span><span class="sxs-lookup"><span data-stu-id="2d89a-132">Service providers call a hook function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="2d89a-133">Der Anbieter übergibt einen Zeiger auf diese Hook-Funktion in der [IMAPISupport::Details](imapisupport-details.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2d89a-133">The provider passes a pointer to this hook function in calls to the [IMAPISupport::Details](imapisupport-details.md) method.</span></span> 
  
<span data-ttu-id="2d89a-134">In beiden Fällen Ruft, wenn das Dialogfeld angezeigt wird und der Benutzer die Schaltfläche definierte wählt, MAPI **LPFNBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="2d89a-134">In both cases, when the dialog box is displayed and the user chooses the defined button, MAPI calls **LPFNBUTTON**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2d89a-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d89a-135">See also</span></span>



[<span data-ttu-id="2d89a-136">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="2d89a-136">BuildDisplayTable</span></span>](builddisplaytable.md)

