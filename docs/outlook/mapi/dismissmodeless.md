---
title: DISMISSMODELESS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DISMISSMODELESS
api_type:
- COM
ms.assetid: ef93ef3d-c159-40ae-9b8d-0af8a0567565
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c66ff2338eb5751dbffe392a6a26258fb1c89476
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565837"
---
# <a name="dismissmodeless"></a><span data-ttu-id="796aa-103">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="796aa-103">DISMISSMODELESS</span></span>

  
  
<span data-ttu-id="796aa-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="796aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="796aa-105">Definiert eine Rückruffunktion, die MAPI-aufrufen, wenn sie ein Dialogfeld ohne Modus Address Book geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="796aa-105">Defines a callback function that MAPI calls when it has dismissed a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="796aa-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="796aa-106">Header file:</span></span>  <br/> |<span data-ttu-id="796aa-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="796aa-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="796aa-108">Definierte Funktion von implementiert:</span><span class="sxs-lookup"><span data-stu-id="796aa-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="796aa-109">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="796aa-109">Client applications</span></span>  <br/> |
|<span data-ttu-id="796aa-110">Definierte Funktion aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="796aa-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="796aa-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="796aa-111">MAPI</span></span>  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="796aa-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="796aa-112">Parameters</span></span>

 <span data-ttu-id="796aa-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="796aa-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="796aa-114">[in] Einen implementierungsspezifischen Wert in der Regel für die Übergabe von Informationen zur Benutzeroberfläche auf eine Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="796aa-114">[in] An implementation-specific value typically used for passing user interface information to a function.</span></span> <span data-ttu-id="796aa-115">Beispielsweise wird in Microsoft Windows ein dieser Parameter ist das übergeordnete Fensterhandle für das Dialogfeld und vom Typ HWND in eine **ULONG_PTR**umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="796aa-115">For example, in Microsoft Windows this parameter is the parent window handle for the dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="796aa-116">Der Wert 0 gibt an, dass kein übergeordnetes Fenster vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="796aa-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="796aa-117">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="796aa-117">_lpvContext_</span></span>
  
> <span data-ttu-id="796aa-118">[in] Zeiger auf einen beliebigen Wert wird an die Rückruffunktion übergeben, wenn MAPI aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="796aa-118">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="796aa-119">Dieser Wert kann eine an die Clientanwendung Vielfache von-Adresse dar.</span><span class="sxs-lookup"><span data-stu-id="796aa-119">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="796aa-120">In der Regel ist _LpvContext_ für C++-Code einen Zeiger auf die Adresse des eine C++-Objektinstanz.</span><span class="sxs-lookup"><span data-stu-id="796aa-120">Typically, for C++ code,  _lpvContext_ is a pointer to the address of a C++ object instance.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="796aa-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="796aa-121">Return value</span></span>

<span data-ttu-id="796aa-122">Keine</span><span class="sxs-lookup"><span data-stu-id="796aa-122">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="796aa-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="796aa-123">Remarks</span></span>

<span data-ttu-id="796aa-124">Wenn die Client-Anwendung ein Dialogfeld ohne Modus Address Book aufruft, umfasst auch in seiner Windows Nachrichtenschleife einen Anruf an eine Funktion, die basierend auf den Prototyp [ACCELERATEABSDI](accelerateabsdi.md) , die überprüft und Zugriffstasten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="796aa-124">When the client application invokes a modeless address book dialog box, it includes in its Windows message loop a call to a function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype, which checks for and processes accelerator keys.</span></span> <span data-ttu-id="796aa-125">Wenn das Dialogfeld geschlossen wird, basiert MAPI-Aufrufe, die **DISMISSMODELESS** Funktion basiert, damit die Clientanwendung angehalten wird das Aufrufen der **ACCELERATEABSDI** Funktion.</span><span class="sxs-lookup"><span data-stu-id="796aa-125">When the dialog box is closed, MAPI calls the **DISMISSMODELESS** based function so that the client application will stop calling the **ACCELERATEABSDI** based function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="796aa-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="796aa-126">See also</span></span>



[<span data-ttu-id="796aa-127">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="796aa-127">ADRPARM</span></span>](adrparm.md)

