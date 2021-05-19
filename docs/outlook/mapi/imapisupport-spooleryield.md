---
title: IMAPISupportSpoolerYield
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerYield
api_type:
- COM
ms.assetid: f5c6ba8f-4ef5-4d60-b4e6-5b9160ec4e99
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f6cdebf82d8b84ada3d029865867c5192af90b0d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409909"
---
# <a name="imapisupportspooleryield"></a><span data-ttu-id="2a5f1-103">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="2a5f1-103">IMAPISupport::SpoolerYield</span></span>

  
  
<span data-ttu-id="2a5f1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a5f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a5f1-105">Gibt dem MAPI-Spooler die Kontrolle über die CPU, sodass er alle für erforderlich erachteten Aufgaben ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="2a5f1-105">Gives control of the CPU to the MAPI spooler so that it can perform any tasks it considers necessary.</span></span>
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="2a5f1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a5f1-106">Parameters</span></span>

 <span data-ttu-id="2a5f1-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2a5f1-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2a5f1-108">Reserviert; muss null sein.</span><span class="sxs-lookup"><span data-stu-id="2a5f1-108">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2a5f1-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a5f1-109">Return value</span></span>

<span data-ttu-id="2a5f1-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="2a5f1-110">S_OK</span></span> 
  
> <span data-ttu-id="2a5f1-111">Der Transportanbieter hat die CPU erfolgreich freigegeben.</span><span class="sxs-lookup"><span data-stu-id="2a5f1-111">The transport provider successfully released the CPU.</span></span>
    
<span data-ttu-id="2a5f1-112">MAPI_W_CANCEL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="2a5f1-112">MAPI_W_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="2a5f1-113">Der Transportanbieter wird angewiesen, die Zustellung der Nachricht an alle Empfänger zu beenden, die sie noch nicht empfangen haben.</span><span class="sxs-lookup"><span data-stu-id="2a5f1-113">Instructs the transport provider to stop the delivery of the message to any recipients that have not yet received it.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2a5f1-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2a5f1-114">Remarks</span></span>

<span data-ttu-id="2a5f1-115">Die **IMAPISupport::SpoolerYield-Methode** wird für Unterstützungsobjekte des Transportanbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="2a5f1-115">The **IMAPISupport::SpoolerYield** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="2a5f1-116">Transportanbieter rufen **SpoolerYield auf,** damit der MAPI-Spooler alle erforderlichen Verarbeitungsschritte ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="2a5f1-116">Transport providers call **SpoolerYield** to allow the MAPI spooler to accomplish any necessary processing.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2a5f1-117">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="2a5f1-117">Notes to callers</span></span>

<span data-ttu-id="2a5f1-118">Rufen **Sie SpoolerYield auf,** wenn Sie langwierige Vorgänge ausführen, die angehalten werden können.</span><span class="sxs-lookup"><span data-stu-id="2a5f1-118">Call **SpoolerYield** when you are performing lengthy operations that can be paused.</span></span> <span data-ttu-id="2a5f1-119">Dadurch können Vordergrundanwendungen während eines langen Vorgangs ausgeführt werden, z. B. die Zustellung an eine große Empfängerliste über ein ausgelastetes Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="2a5f1-119">This allows foreground applications to run during a long operation, such as delivery to a large recipient list across a busy network.</span></span> 
  
<span data-ttu-id="2a5f1-120">Wenn **SpoolerYield** mit MAPI_W_CANCEL_MESSAGE zurückgibt, hat der MAPI-Spooler festgestellt, dass die Nachricht nicht mehr gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a5f1-120">If **SpoolerYield** returns with MAPI_W_CANCEL_MESSAGE, the MAPI spooler has determined that the message should no longer be sent.</span></span> <span data-ttu-id="2a5f1-121">Geben MAPI_E_USER_CANCEL Zurück zu Ihrem Anrufprozess zurück, und beenden Sie sie, wenn möglich.</span><span class="sxs-lookup"><span data-stu-id="2a5f1-121">Return MAPI_E_USER_CANCEL to your calling process and exit, if possible.</span></span> 
  
<span data-ttu-id="2a5f1-122">Weitere Informationen zum Nachgeben an den MAPI-Spooler finden Sie unter [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span><span class="sxs-lookup"><span data-stu-id="2a5f1-122">For more information about yielding to the MAPI spooler, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2a5f1-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a5f1-123">See also</span></span>



[<span data-ttu-id="2a5f1-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="2a5f1-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

