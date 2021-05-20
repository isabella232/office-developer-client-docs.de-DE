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
ms.openlocfilehash: 804bd23a148b942fd4580d1e3465fc1f65ff5978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431512"
---
# <a name="lpfnbutton"></a><span data-ttu-id="884cd-103">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="884cd-103">LPFNBUTTON</span></span>

  
  
<span data-ttu-id="884cd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="884cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="884cd-105">Definiert eine Rückruffunktion, die MAPI aufruft, um ein optionales Schaltflächensteuerelement in einem Adressbuchdialogfeld zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="884cd-105">Defines a callback function that MAPI calls to activate an optional button control in an address book dialog box.</span></span> <span data-ttu-id="884cd-106">Diese Schaltfläche ist in der Regel eine **Schaltfläche Details.**</span><span class="sxs-lookup"><span data-stu-id="884cd-106">This button is typically a **Details** button.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="884cd-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="884cd-107">Header file:</span></span>  <br/> |<span data-ttu-id="884cd-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="884cd-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="884cd-109">Definierte Funktion implementiert von:</span><span class="sxs-lookup"><span data-stu-id="884cd-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="884cd-110">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="884cd-110">Service providers</span></span>  <br/> |
|<span data-ttu-id="884cd-111">Definierte Funktion, die von:</span><span class="sxs-lookup"><span data-stu-id="884cd-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="884cd-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="884cd-112">MAPI</span></span>  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="884cd-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="884cd-113">Parameters</span></span>

 <span data-ttu-id="884cd-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="884cd-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="884cd-115">[in] Handle der übergeordneten Fenster für alle Dialogfelder oder Fenster, die diese Funktion anzeigt.</span><span class="sxs-lookup"><span data-stu-id="884cd-115">[in] Handle of the parent windows for any dialog boxes or windows this function displays.</span></span>
    
 <span data-ttu-id="884cd-116">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="884cd-116">_lpvContext_</span></span>
  
> <span data-ttu-id="884cd-117">[in] Zeiger auf einen beliebigen Wert, der an die Rückruffunktion übergeben wird, wenn MAPI ihn aufruft.</span><span class="sxs-lookup"><span data-stu-id="884cd-117">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="884cd-118">Dieser Wert kann eine Für die Clientanwendung wichtige Adresse darstellen.</span><span class="sxs-lookup"><span data-stu-id="884cd-118">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="884cd-119">In der Regel stellt  _lpvContext_ für C++-Code einen Zeiger auf ein C++-Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="884cd-119">Typically, for C++ code,  _lpvContext_ represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="884cd-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="884cd-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="884cd-121">[in] Größe des Eintragsbezeichners in Bytes, auf den der  _lpSelection-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="884cd-121">[in] Size, in bytes, of the entry identifier pointed to by the  _lpSelection_ parameter.</span></span> 
    
 <span data-ttu-id="884cd-122">_lpSelection_</span><span class="sxs-lookup"><span data-stu-id="884cd-122">_lpSelection_</span></span>
  
> <span data-ttu-id="884cd-123">[in] Zeiger auf den Eintragsbezeichner, der die Auswahl im Dialogfeld definiert.</span><span class="sxs-lookup"><span data-stu-id="884cd-123">[in] Pointer to the entry identifier defining the selection in the dialog box.</span></span>
    
 <span data-ttu-id="884cd-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="884cd-124">_ulFlags_</span></span>
  
> <span data-ttu-id="884cd-125">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="884cd-125">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="884cd-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="884cd-126">Return value</span></span>

<span data-ttu-id="884cd-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="884cd-127">S_OK</span></span> 
  
> <span data-ttu-id="884cd-128">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="884cd-128">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="884cd-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="884cd-129">Remarks</span></span>

<span data-ttu-id="884cd-130">Clientanwendungen rufen eine Rückruffunktion basierend auf dem **LPFNBUTTON-Prototyp** auf, um eine Schaltfläche in einem Detaildialogfeld zu definieren.</span><span class="sxs-lookup"><span data-stu-id="884cd-130">Client applications call a callback function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="884cd-131">Der Client übergibt einen Zeiger an die Rückruffunktion in Aufrufen der [IAddrBook::D etails-Methode.](iaddrbook-details.md)</span><span class="sxs-lookup"><span data-stu-id="884cd-131">The client passes a pointer to the callback function in calls to the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="884cd-132">Dienstanbieter rufen eine Hookfunktion basierend auf dem **LPFNBUTTON-Prototyp** auf, um eine Schaltfläche in einem Detaildialogfeld zu definieren.</span><span class="sxs-lookup"><span data-stu-id="884cd-132">Service providers call a hook function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="884cd-133">Der Anbieter übergibt einen Zeiger auf diese Hookfunktion in Aufrufen der [IMAPISupport::D etails-Methode.](imapisupport-details.md)</span><span class="sxs-lookup"><span data-stu-id="884cd-133">The provider passes a pointer to this hook function in calls to the [IMAPISupport::Details](imapisupport-details.md) method.</span></span> 
  
<span data-ttu-id="884cd-134">In beiden Fällen ruft MAPI **LPFNBUTTON** auf, wenn das Dialogfeld angezeigt wird und der Benutzer die definierte Schaltfläche aus wählt.</span><span class="sxs-lookup"><span data-stu-id="884cd-134">In both cases, when the dialog box is displayed and the user chooses the defined button, MAPI calls **LPFNBUTTON**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="884cd-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="884cd-135">See also</span></span>



[<span data-ttu-id="884cd-136">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="884cd-136">BuildDisplayTable</span></span>](builddisplaytable.md)

