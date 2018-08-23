---
title: MAPIINIT_0
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIINIT_0
api_type:
- COM
ms.assetid: 70739711-ff43-407d-bc8b-6baf7a476fef
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1eb4d7ac8d0287388a1bb76185f23636eddcf809
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591674"
---
# <a name="mapiinit0"></a><span data-ttu-id="a57b4-103">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="a57b4-103">MAPIINIT_0</span></span>

  
  
<span data-ttu-id="a57b4-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a57b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a57b4-105">Optionen für die Funktion ["MAPIInitialize"](mapiinitialize.md) übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a57b4-105">Conveys options to the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a57b4-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a57b4-106">Header file:</span></span>  <br/> |<span data-ttu-id="a57b4-107">MAPIX. H</span><span class="sxs-lookup"><span data-stu-id="a57b4-107">MAPIX.H</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulVersion;
  ULONG ulFlags;
} MAPIINIT_0, FAR *LPMAPIINIT_0;

```

## <a name="members"></a><span data-ttu-id="a57b4-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="a57b4-108">Members</span></span>

 <span data-ttu-id="a57b4-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="a57b4-109">**ulVersion**</span></span>
  
> <span data-ttu-id="a57b4-110">Ein Ganzzahlwert, der die Versionsnummer der **MAPIINIT_0** Struktur darstellt.</span><span class="sxs-lookup"><span data-stu-id="a57b4-110">An integer value that represents the version number of the **MAPIINIT_0** structure.</span></span> <span data-ttu-id="a57b4-111">Das **UlVersion** -Element ist für die zukünftige Erweiterung und die Version der MAPI-Schnittstelle stellt keine dar.</span><span class="sxs-lookup"><span data-stu-id="a57b4-111">The **ulVersion** member is for future expansion and does not represent the version of the MAPI interface.</span></span> <span data-ttu-id="a57b4-112">Derzeit muss **UlVersion** auf MAPI_INIT_VERSION festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="a57b4-112">Currently, **ulVersion** must be set to MAPI_INIT_VERSION.</span></span> 
    
 <span data-ttu-id="a57b4-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="a57b4-113">**ulFlags**</span></span>
  
> <span data-ttu-id="a57b4-114">Die Bitmaske Flags verwendet, um die Initialisierung der MAPI-Sitzung zu steuern.</span><span class="sxs-lookup"><span data-stu-id="a57b4-114">The bitmask of flags used to control the initialization of the MAPI session.</span></span> <span data-ttu-id="a57b4-115">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a57b4-115">The following flags can be set:</span></span>
    
<span data-ttu-id="a57b4-116">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="a57b4-116">MAPI_MULTITHREAD_NOTIFICATIONS</span></span> 
  
> <span data-ttu-id="a57b4-117">MAPI sollte mit einem Thread dedizierte Benachrichtigung anstelle des ersten Threads verwendet, um das Aufrufen von **"MAPIInitialize"** Behandeln von Benachrichtigungen generieren.</span><span class="sxs-lookup"><span data-stu-id="a57b4-117">MAPI should generate notifications using a thread dedicated to notification handling instead of the first thread used to call **MAPIInitialize**.</span></span>
    
<span data-ttu-id="a57b4-118">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="a57b4-118">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="a57b4-119">Der Anrufer wird als Windows-Dienst ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a57b4-119">The caller is running as a Windows service.</span></span> <span data-ttu-id="a57b4-120">Anrufer, die wie ein Windows-Dienst nicht dieses Flag festlegen sollten nicht ausgeführt werden; Anrufer, die als Dienst ausgeführt werden, müssen dieses Flag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a57b4-120">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span>
    
<span data-ttu-id="a57b4-121">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="a57b4-121">MAPI_NO_COINIT</span></span>
  
> <span data-ttu-id="a57b4-122">Das Flag MAPI_NO_COINT so festgelegt, dass **"MAPIInitialize"** nicht versucht, mit einem Aufruf von [CoInitialize](http://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx)COM initialisieren.</span><span class="sxs-lookup"><span data-stu-id="a57b4-122">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](http://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx).</span></span> <span data-ttu-id="a57b4-123">Wenn eine **MAPIINIT_0** -Struktur mit _UlFlags_ auf MAPI_NO_COINIT festgelegt in **"MAPIInitialize"** übergeben wird, wird MAPI wird vorausgesetzt, dass COM bereits initialisiert wurde, und den Aufruf von **CoInitialize**umgangen wird.</span><span class="sxs-lookup"><span data-stu-id="a57b4-123">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and will bypass the call to **CoInitialize**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a57b4-124">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="a57b4-124">Remarks</span></span>

<span data-ttu-id="a57b4-125">Multithread-Clients sollte das MAPI_MULTITHREAD_NOTIFICATIONS Flag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a57b4-125">Multithreaded clients should set the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> <span data-ttu-id="a57b4-126">Wenn das Flag nicht festgelegt ist, werden Benachrichtigungen auf dem Thread verwendet, um den ersten Aufrufen **"MAPIInitialize"** generiert.</span><span class="sxs-lookup"><span data-stu-id="a57b4-126">If the flag is not set, notifications are generated on the thread used to make the first call to **MAPIInitialize**.</span></span> 
  
<span data-ttu-id="a57b4-127">Weitere Informationen, wann dieses Flag festgelegt und wie Threadsicherheit in einer Clientdatenbank implementieren finden Sie unter [Threading in MAPI](threading-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="a57b4-127">For more information about when to set this flag and how to implement thread safety in a client, see [Threading in MAPI](threading-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a57b4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a57b4-128">See also</span></span>



[<span data-ttu-id="a57b4-129">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="a57b4-129">MAPIInitialize</span></span>](mapiinitialize.md)


[<span data-ttu-id="a57b4-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="a57b4-130">MAPI Structures</span></span>](mapi-structures.md)

