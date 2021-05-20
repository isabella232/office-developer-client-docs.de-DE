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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 940cf0cf377f1b38071df5e3c300ccb7d685e5a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439877"
---
# <a name="imapiofflinenotify--iunknown"></a><span data-ttu-id="12287-103">IMAPIOfflineNotify : IUnknown</span><span class="sxs-lookup"><span data-stu-id="12287-103">IMAPIOfflineNotify : IUnknown</span></span>

  
  
<span data-ttu-id="12287-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12287-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12287-105">Unterstützt Microsoft Outlook 2010 und Microsoft Outlook 2013 beim Senden von Benachrichtigungsrückrufen an einen Client.</span><span class="sxs-lookup"><span data-stu-id="12287-105">Supports Microsoft Outlook 2010 and Microsoft Outlook 2013 in sending notification callbacks to a client.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="12287-106">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="12287-106">Provided by:</span></span>  <br/> |<span data-ttu-id="12287-107">Client</span><span class="sxs-lookup"><span data-stu-id="12287-107">Client</span></span>  <br/> |
|<span data-ttu-id="12287-108">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="12287-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="12287-109">IID_IMAPIOfflineNotify</span><span class="sxs-lookup"><span data-stu-id="12287-109">IID_IMAPIOfflineNotify</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="12287-110">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="12287-110">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="12287-111">Notify</span><span class="sxs-lookup"><span data-stu-id="12287-111">Notify</span></span>](imapiofflinenotify-notify.md) <br/> |<span data-ttu-id="12287-112">Sendet Benachrichtigungen über Änderungen im Verbindungsstatus an einen Client.</span><span class="sxs-lookup"><span data-stu-id="12287-112">Sends notifications to a client about changes in connection state.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12287-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="12287-113">Remarks</span></span>

<span data-ttu-id="12287-114">Der Client muss diese Schnittstelle implementieren und einen Zeiger als Mitglied **[in](mapioffline_adviseinfo.md)** MAPIOFFLINE_ADVISEINFO beim Einrichten von Rückrufen mit **[IMAPIOfflineMgr::Advise übergeben.](imapiofflinemgr-advise.md)**</span><span class="sxs-lookup"><span data-stu-id="12287-114">The client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="12287-115">Anschließend können Outlook 2010 oder Outlook 2013 diese Schnittstelle verwenden, um Benachrichtigungsrückrufe an den Client zu senden.</span><span class="sxs-lookup"><span data-stu-id="12287-115">Subsequently, Outlook 2010 or Outlook 2013 will be able to use this interface to send notification callbacks to the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="12287-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12287-116">See also</span></span>



[<span data-ttu-id="12287-117">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="12287-117">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="12287-118">Informationen zur Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="12287-118">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="12287-119">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="12287-119">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="12287-120">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="12287-120">MAPIOFFLINE_ADVISEINFO</span></span>](mapioffline_adviseinfo.md)

