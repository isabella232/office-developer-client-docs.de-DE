---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3cb110fdcbbd88e494c44ba2ed73cc26674638ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420024"
---
# <a name="mapiofflineadviseinfo"></a><span data-ttu-id="e17bb-103">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="e17bb-103">MAPIOFFLINE_ADVISEINFO</span></span>
 
<span data-ttu-id="e17bb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e17bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e17bb-105">Enthält Informationen zu **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)** to Register Callback for an Offline Object.</span><span class="sxs-lookup"><span data-stu-id="e17bb-105">Provides information to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** to register callback for an offline object.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e17bb-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="e17bb-106">Quick info</span></span>

<span data-ttu-id="e17bb-107">Weitere Informationen finden Sie unter **IMAPIOfflineMgr:: Advise**.</span><span class="sxs-lookup"><span data-stu-id="e17bb-107">See **IMAPIOfflineMgr::Advise**.</span></span> 
  
```cpp
typedef struct 
{ 
      ULONG                   ulSize; 
      ULONG                   ulClientToken; 
      MAPIOFFLINE_CALLBACK_TYPE     CallbackType; 
      IUnknown*               pCallback; 
      ULONG                   ulAdviseTypes; 
      ULONG                   ulStateMask; 
} MAPIOFFLINE_ADVISEINFO;
```

## <a name="members"></a><span data-ttu-id="e17bb-108">Members</span><span class="sxs-lookup"><span data-stu-id="e17bb-108">Members</span></span>

<span data-ttu-id="e17bb-109">_ulSize_: die Größe von **MAPIOFFLINE_ADVISEINFO**.</span><span class="sxs-lookup"><span data-stu-id="e17bb-109">_ulSize_: The size of **MAPIOFFLINE_ADVISEINFO**.</span></span> 
    
<span data-ttu-id="e17bb-110">_ulClientToken_: ein vom Client definiertes Token zu einem Rückruf.</span><span class="sxs-lookup"><span data-stu-id="e17bb-110">_ulClientToken_: A token defined by the client about a callback.</span></span> <span data-ttu-id="e17bb-111">Es ist das *ulClientToken* -Element der **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** -Struktur, die an **[IMAPIOfflineNotify:: notify](imapiofflinenotify-notify.md)** übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e17bb-111">It is the *ulClientToken* member of the **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** structure passed to **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**.</span></span> 
    
<span data-ttu-id="e17bb-112">_CallbackType_: Typ des anzulegenden Rückrufs.</span><span class="sxs-lookup"><span data-stu-id="e17bb-112">_CallbackType_: Type of callback to make.</span></span>
    
   -  <span data-ttu-id="e17bb-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="e17bb-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span></span> 
    
   - <span data-ttu-id="e17bb-114">Der Rückruftyp erfolgt per Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="e17bb-114">The type of callback is by notification.</span></span> <span data-ttu-id="e17bb-115">Dies ist der einzige unterstützte Rückruftyp.</span><span class="sxs-lookup"><span data-stu-id="e17bb-115">This is the only supported type of callback.</span></span>  <span data-ttu-id="e17bb-116">*pCallback* muss die Schnittstelle **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="e17bb-116">*pCallback*  must indicate the interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="e17bb-117">_pCallback_: Schnittstelle für Rückruf.</span><span class="sxs-lookup"><span data-stu-id="e17bb-117">_pCallback_: Interface to use for callback.</span></span> <span data-ttu-id="e17bb-118">Dies ist die Implementierung von **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** durch den Client.</span><span class="sxs-lookup"><span data-stu-id="e17bb-118">This is the client's implementation of **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="e17bb-119">_ulAdviseTypes_: die Art der Beratung, wie durch die Bedingung für die Beratung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e17bb-119">_ulAdviseTypes_: The types of advise, as identified by the condition for advising.</span></span> <span data-ttu-id="e17bb-120">Der einzige unterstützte Typ ist MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span><span class="sxs-lookup"><span data-stu-id="e17bb-120">The only supported type is MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span></span>
    
<span data-ttu-id="e17bb-121">_ulStateMask_: der einzige unterstützte Status ist MAPIOFFLINE_STATE_ALL.</span><span class="sxs-lookup"><span data-stu-id="e17bb-121">_ulStateMask_: The only supported state is MAPIOFFLINE_STATE_ALL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e17bb-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e17bb-122">See also</span></span>

- [<span data-ttu-id="e17bb-123">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="e17bb-123">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)
- [<span data-ttu-id="e17bb-124">Informationen zur Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="e17bb-124">About the Offline State API</span></span>](about-the-offline-state-api.md) 
- [<span data-ttu-id="e17bb-125">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="e17bb-125">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="e17bb-126">MAPIOFFLINE_CALLBACK_TYPE</span><span class="sxs-lookup"><span data-stu-id="e17bb-126">MAPIOFFLINE_CALLBACK_TYPE</span></span>](mapioffline_callback_type.md)

