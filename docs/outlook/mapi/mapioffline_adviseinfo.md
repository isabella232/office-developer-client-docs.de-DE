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
ms.openlocfilehash: 82869fa479ebe8a4d7b1881cec5d5c243b7d7957
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565095"
---
# <a name="mapiofflineadviseinfo"></a><span data-ttu-id="bac77-103">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="bac77-103">MAPIOFFLINE_ADVISEINFO</span></span>
 
<span data-ttu-id="bac77-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bac77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bac77-105">Enthält Informationen zu **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** Rückruf für ein offline-Objekt zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="bac77-105">Provides information to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** to register callback for an offline object.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="bac77-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="bac77-106">Quick info</span></span>

<span data-ttu-id="bac77-107">Finden Sie unter **IMAPIOfflineMgr::Advise**.</span><span class="sxs-lookup"><span data-stu-id="bac77-107">See **IMAPIOfflineMgr::Advise**.</span></span> 
  
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

## <a name="members"></a><span data-ttu-id="bac77-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="bac77-108">Members</span></span>

<span data-ttu-id="bac77-109">_UlSize_: die Größe des **MAPIOFFLINE_ADVISEINFO**.</span><span class="sxs-lookup"><span data-stu-id="bac77-109">_ulSize_: The size of **MAPIOFFLINE_ADVISEINFO**.</span></span> 
    
<span data-ttu-id="bac77-110">_UlClientToken_: ein Token vom Client über einen Rückruf definiert.</span><span class="sxs-lookup"><span data-stu-id="bac77-110">_ulClientToken_: A token defined by the client about a callback.</span></span> <span data-ttu-id="bac77-111">Ist die *UlClientToken* Mitglied die **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** Struktur **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** übergeben.</span><span class="sxs-lookup"><span data-stu-id="bac77-111">It is the *ulClientToken* member of the **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** structure passed to **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**.</span></span> 
    
<span data-ttu-id="bac77-112">_CallbackType_: Typ des Rückrufs vornehmen.</span><span class="sxs-lookup"><span data-stu-id="bac77-112">_CallbackType_: Type of callback to make.</span></span>
    
   -  <span data-ttu-id="bac77-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="bac77-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span></span> 
    
   - <span data-ttu-id="bac77-114">Der Typ des Rückrufs ist durch Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="bac77-114">The type of callback is by notification.</span></span> <span data-ttu-id="bac77-115">Dies ist die einzige unterstützte Art von Rückruf.</span><span class="sxs-lookup"><span data-stu-id="bac77-115">This is the only supported type of callback.</span></span>  <span data-ttu-id="bac77-116">*pCallback* muss die Schnittstelle **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bac77-116">*pCallback*  must indicate the interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="bac77-117">_pCallback_: Schnittstelle für den Rückruf verwenden.</span><span class="sxs-lookup"><span data-stu-id="bac77-117">_pCallback_: Interface to use for callback.</span></span> <span data-ttu-id="bac77-118">Dies ist die Client-Implementierung von **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="bac77-118">This is the client's implementation of **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="bac77-119">_UlAdviseTypes_: die Typen der Advise, wie durch die Bedingung für die mit dem Hinweis identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bac77-119">_ulAdviseTypes_: The types of advise, as identified by the condition for advising.</span></span> <span data-ttu-id="bac77-120">Der einzige unterstützte Typ ist MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span><span class="sxs-lookup"><span data-stu-id="bac77-120">The only supported type is MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span></span>
    
<span data-ttu-id="bac77-121">_UlStateMask_: der einzige unterstützte Zustand MAPIOFFLINE_STATE_ALL ist.</span><span class="sxs-lookup"><span data-stu-id="bac77-121">_ulStateMask_: The only supported state is MAPIOFFLINE_STATE_ALL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bac77-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bac77-122">See also</span></span>

- [<span data-ttu-id="bac77-123">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="bac77-123">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)
- [<span data-ttu-id="bac77-124">Informationen zu der Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="bac77-124">About the Offline State API</span></span>](about-the-offline-state-api.md) 
- [<span data-ttu-id="bac77-125">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="bac77-125">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="bac77-126">MAPIOFFLINE_CALLBACK_TYPE</span><span class="sxs-lookup"><span data-stu-id="bac77-126">MAPIOFFLINE_CALLBACK_TYPE</span></span>](mapioffline_callback_type.md)

