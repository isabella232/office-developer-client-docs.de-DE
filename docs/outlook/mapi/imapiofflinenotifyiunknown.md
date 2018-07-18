---
title: IMAPIOfflineNotify IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify
api_type:
- COM
ms.assetid: a593d2a1-29f8-7e23-85bf-02fa3cfebe1b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 37f21c438a0a337eecf5c15a27a0b891d19bcfb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792255"
---
# <a name="imapiofflinenotify--iunknown"></a><span data-ttu-id="27b32-103">IMAPIOfflineNotify : IUnknown</span><span class="sxs-lookup"><span data-stu-id="27b32-103">IMAPIOfflineNotify : IUnknown</span></span>

  
  
<span data-ttu-id="27b32-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="27b32-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="27b32-105">Senden von Benachrichtigungen Rückrufe an einen Client unterstützt Microsoft Outlook 2010 und Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="27b32-105">Supports Microsoft Outlook 2010 and Microsoft Outlook 2013 in sending notification callbacks to a client.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27b32-106">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="27b32-106">Provided by:</span></span>  <br/> |<span data-ttu-id="27b32-107">Client</span><span class="sxs-lookup"><span data-stu-id="27b32-107">Client</span></span>  <br/> |
|<span data-ttu-id="27b32-108">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="27b32-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="27b32-109">IID_IMAPIOfflineNotify</span><span class="sxs-lookup"><span data-stu-id="27b32-109">IID_IMAPIOfflineNotify</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="27b32-110">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="27b32-110">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="27b32-111">Benachrichtigen</span><span class="sxs-lookup"><span data-stu-id="27b32-111">Notify</span></span>](imapiofflinenotify-notify.md) <br/> |<span data-ttu-id="27b32-112">Sendet Benachrichtigungen an einen Client zu Änderungen in Verbindungsstatus.</span><span class="sxs-lookup"><span data-stu-id="27b32-112">Sends notifications to a client about changes in connection state.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27b32-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27b32-113">Remarks</span></span>

<span data-ttu-id="27b32-114">Der Client muss diese Schnittstelle implementieren und einen Zeiger darauf als Mitglied in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** übergeben, beim Einrichten von Rückrufe mit **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="27b32-114">The client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="27b32-115">Anschließend werden Outlook 2010 oder Outlook 2013 können diese Schnittstelle verwenden, um die Benachrichtigung Rückrufe an den Client gesendet.</span><span class="sxs-lookup"><span data-stu-id="27b32-115">Subsequently, Outlook 2010 or Outlook 2013 will be able to use this interface to send notification callbacks to the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="27b32-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27b32-116">See also</span></span>



[<span data-ttu-id="27b32-117">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="27b32-117">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="27b32-118">Informationen zu der Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="27b32-118">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="27b32-119">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="27b32-119">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="27b32-120">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="27b32-120">MAPIOFFLINE_ADVISEINFO</span></span>](mapioffline_adviseinfo.md)

