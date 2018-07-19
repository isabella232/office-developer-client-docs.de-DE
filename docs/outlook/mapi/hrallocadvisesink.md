---
title: HrAllocAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrAllocAdviseSink
api_type:
- HeaderDef
ms.assetid: 1dd460e6-ce95-4fef-bb5e-8d778c9716d5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5a5e736e8be1120f5fb90048f01fdc8a44479060
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791895"
---
# <a name="hrallocadvisesink"></a><span data-ttu-id="2e034-103">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="2e034-103">HrAllocAdviseSink</span></span>

  
  
<span data-ttu-id="2e034-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2e034-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2e034-105">Erstellt eine Advise-Empfängerobjekt, wenn ein Kontext die aufrufende Implementierung und eine Rückruffunktion, die ausgelöst werden, indem eine Benachrichtigung angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2e034-105">Creates an advise sink object, given a context specified by the calling implementation and a callback function to be triggered by an event notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2e034-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="2e034-106">Header file:</span></span>  <br/> |<span data-ttu-id="2e034-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2e034-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2e034-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="2e034-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2e034-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2e034-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2e034-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="2e034-110">Called by:</span></span>  <br/> |<span data-ttu-id="2e034-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="2e034-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="2e034-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e034-112">Parameters</span></span>

 <span data-ttu-id="2e034-113">_lpfnCallback_</span><span class="sxs-lookup"><span data-stu-id="2e034-113">_lpfnCallback_</span></span>
  
> <span data-ttu-id="2e034-114">[in] Zeiger auf eine Rückruffunktion, die basierend auf den [NOTIFCALLBACK](notifcallback.md) Prototyp, die MAPI angerufen, wenn eine Benachrichtigungsereignis tritt ein, für die neu erstellte advise-Empfänger.</span><span class="sxs-lookup"><span data-stu-id="2e034-114">[in] Pointer to a callback function based on the [NOTIFCALLBACK](notifcallback.md) prototype that MAPI is to call when a notification event occurs for the newly created advise sink.</span></span> 
    
 <span data-ttu-id="2e034-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="2e034-115">_lpvContext_</span></span>
  
> <span data-ttu-id="2e034-116">[in] Zeiger auf Daten des Anrufers an der Callback-Funktion beim Aufrufen von MAPI übergeben.</span><span class="sxs-lookup"><span data-stu-id="2e034-116">[in] Pointer to caller data passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="2e034-117">Die Anrufer Daten können eine Adresse Vielfache an den Client oder Anbieter von darstellen.</span><span class="sxs-lookup"><span data-stu-id="2e034-117">The caller data can represent an address of significance to the client or provider.</span></span> <span data-ttu-id="2e034-118">In der Regel stellt der _LpvContext_ -Parameter für C++-Code einen Zeiger auf die Adresse eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="2e034-118">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to the address of an object.</span></span> 
    
 <span data-ttu-id="2e034-119">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="2e034-119">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="2e034-120">[out] Zeiger auf einen Zeiger auf eine Advise-Empfängerobjekt.</span><span class="sxs-lookup"><span data-stu-id="2e034-120">[out] Pointer to a pointer to an advise sink object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2e034-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e034-121">Return value</span></span>

<span data-ttu-id="2e034-122">None.</span><span class="sxs-lookup"><span data-stu-id="2e034-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e034-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e034-123">Remarks</span></span>

<span data-ttu-id="2e034-124">Um die **HrAllocAdviseSink** -Funktion verwenden, können Sie eine Clientanwendung oder Dienstanbieter erstellt ein Objekt Erhalt von Benachrichtigungen, erstellt eine Benachrichtigung Callback-Funktion basierend auf den [NOTIFCALLBACK](notifcallback.md) Funktionsprototyp, der mit diesem Objekt wechselt, auf und übergibt einen Zeiger auf das Objekt in der **HrAllocAdviseSink** -Funktion als _LpvContext_ Wert.</span><span class="sxs-lookup"><span data-stu-id="2e034-124">To use the **HrAllocAdviseSink** function, a client application or service provider creates an object to receive notifications, creates a notification callback function based on the [NOTIFCALLBACK](notifcallback.md) function prototype that goes with that object, and passes a pointer to the object in the **HrAllocAdviseSink** function as the  _lpvContext_ value.</span></span> <span data-ttu-id="2e034-125">Auf diese Weise führt eine Benachrichtigung. und als Teil der Benachrichtigung, MAPI-Aufrufen die Callback-Funktion mit dem Mauszeiger Objekt als Kontext aus.</span><span class="sxs-lookup"><span data-stu-id="2e034-125">Doing so performs a notification; and as part of the notification process, MAPI calls the callback function with the object pointer as the context.</span></span> 
  
<span data-ttu-id="2e034-126">MAPI implementierte eine Benachrichtigung Engine asynchron an.</span><span class="sxs-lookup"><span data-stu-id="2e034-126">MAPI implements its notification engine asynchronously.</span></span> <span data-ttu-id="2e034-127">In C++ kann die Benachrichtigung Callback-Methode eines Objekts sein.</span><span class="sxs-lookup"><span data-stu-id="2e034-127">In C++, the notification callback can be an object method.</span></span> <span data-ttu-id="2e034-128">Wenn das Objekt, das die Benachrichtigung generiert nicht vorhanden, wird des Clients oder Anbieter Anfordern einer Benachrichtigung muss eine separate Referenzzähler für dieses Objekt für des Objekts behalten advise-Empfänger.</span><span class="sxs-lookup"><span data-stu-id="2e034-128">If the object generating the notification is not present, the client or provider requesting notification must keep a separate reference count for that object for the object's advise sink.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="2e034-129">**HrAllocAdviseSink** sollte nur selten verwendet werden. Es ist sicherer für Clients zum Erstellen ihrer eigenen Advise-senken.</span><span class="sxs-lookup"><span data-stu-id="2e034-129">**HrAllocAdviseSink** should be used sparingly; it is safer for clients to create their own advise sinks.</span></span> 
  

