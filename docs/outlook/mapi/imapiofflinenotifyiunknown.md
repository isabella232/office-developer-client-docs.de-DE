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
ms.openlocfilehash: 940cf0cf377f1b38071df5e3c300ccb7d685e5a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270308"
---
# <a name="imapiofflinenotify--iunknown"></a><span data-ttu-id="1e193-103">IMAPIOfflineNotify : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1e193-103">IMAPIOfflineNotify : IUnknown</span></span>

  
  
<span data-ttu-id="1e193-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e193-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e193-105">Unterstützt Microsoft Outlook 2010 und Microsoft Outlook 2013 beim Senden von Benachrichtigungs Rückrufen an einen Client.</span><span class="sxs-lookup"><span data-stu-id="1e193-105">Supports Microsoft Outlook 2010 and Microsoft Outlook 2013 in sending notification callbacks to a client.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1e193-106">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="1e193-106">Provided by:</span></span>  <br/> |<span data-ttu-id="1e193-107">Client</span><span class="sxs-lookup"><span data-stu-id="1e193-107">Client</span></span>  <br/> |
|<span data-ttu-id="1e193-108">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="1e193-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1e193-109">IID_IMAPIOfflineNotify</span><span class="sxs-lookup"><span data-stu-id="1e193-109">IID_IMAPIOfflineNotify</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1e193-110">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="1e193-110">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1e193-111">Benachrichtigen</span><span class="sxs-lookup"><span data-stu-id="1e193-111">Notify</span></span>](imapiofflinenotify-notify.md) <br/> |<span data-ttu-id="1e193-112">Sendet Benachrichtigungen an einen Client über Änderungen im Verbindungsstatus.</span><span class="sxs-lookup"><span data-stu-id="1e193-112">Sends notifications to a client about changes in connection state.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e193-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e193-113">Remarks</span></span>

<span data-ttu-id="1e193-114">Der Client muss diese Schnittstelle implementieren und beim Einrichten von Rückrufen mithilfe von **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)** als Member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** einen Zeiger an diesen übergeben.</span><span class="sxs-lookup"><span data-stu-id="1e193-114">The client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="1e193-115">Anschließend kann Outlook 2010 oder Outlook 2013 diese Schnittstelle zum Senden von Benachrichtigungs Rückrufen an den Client verwenden.</span><span class="sxs-lookup"><span data-stu-id="1e193-115">Subsequently, Outlook 2010 or Outlook 2013 will be able to use this interface to send notification callbacks to the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1e193-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e193-116">See also</span></span>



[<span data-ttu-id="1e193-117">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="1e193-117">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="1e193-118">Informationen zur Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="1e193-118">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="1e193-119">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="1e193-119">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="1e193-120">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="1e193-120">MAPIOFFLINE_ADVISEINFO</span></span>](mapioffline_adviseinfo.md)

