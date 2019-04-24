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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329037"
---
# <a name="imapisupportspooleryield"></a><span data-ttu-id="eee6b-103">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="eee6b-103">IMAPISupport::SpoolerYield</span></span>

  
  
<span data-ttu-id="eee6b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eee6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eee6b-105">Gibt die CPU-Steuerung für den MAPI-Spooler an, sodass Sie alle für erforderlich erachteten Aufgaben ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="eee6b-105">Gives control of the CPU to the MAPI spooler so that it can perform any tasks it considers necessary.</span></span>
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="eee6b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eee6b-106">Parameters</span></span>

 <span data-ttu-id="eee6b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eee6b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="eee6b-108">Reserviert muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="eee6b-108">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eee6b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eee6b-109">Return value</span></span>

<span data-ttu-id="eee6b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="eee6b-110">S_OK</span></span> 
  
> <span data-ttu-id="eee6b-111">Der Transportanbieter hat die CPU erfolgreich veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="eee6b-111">The transport provider successfully released the CPU.</span></span>
    
<span data-ttu-id="eee6b-112">MAPI_W_CANCEL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="eee6b-112">MAPI_W_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="eee6b-113">Weist den Transportanbieter an, die Übermittlung der Nachricht an Empfänger zu beenden, die Sie noch nicht erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="eee6b-113">Instructs the transport provider to stop the delivery of the message to any recipients that have not yet received it.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eee6b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eee6b-114">Remarks</span></span>

<span data-ttu-id="eee6b-115">Die **IMAPISupport:: SpoolerYield** -Methode wird für Support Objekte des Transportanbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="eee6b-115">The **IMAPISupport::SpoolerYield** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="eee6b-116">Transport Anbieter rufen **SpoolerYield** auf, damit der MAPI-Spooler alle erforderlichen Verarbeitungsschritte ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="eee6b-116">Transport providers call **SpoolerYield** to allow the MAPI spooler to accomplish any necessary processing.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="eee6b-117">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="eee6b-117">Notes to callers</span></span>

<span data-ttu-id="eee6b-118">Rufen Sie **SpoolerYield** auf, wenn Sie längere Vorgänge ausführen, die angehalten werden können.</span><span class="sxs-lookup"><span data-stu-id="eee6b-118">Call **SpoolerYield** when you are performing lengthy operations that can be paused.</span></span> <span data-ttu-id="eee6b-119">Auf diese Weise können vordergrundanwendungen während eines langen Betriebs ausgeführt werden, beispielsweise die Übertragung an eine große Empfängerliste in einem belebten Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="eee6b-119">This allows foreground applications to run during a long operation, such as delivery to a large recipient list across a busy network.</span></span> 
  
<span data-ttu-id="eee6b-120">Wenn **SpoolerYield** mit MAPI_W_CANCEL_MESSAGE zurückgibt, hat der MAPI-Spooler festgestellt, dass die Nachricht nicht mehr gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="eee6b-120">If **SpoolerYield** returns with MAPI_W_CANCEL_MESSAGE, the MAPI spooler has determined that the message should no longer be sent.</span></span> <span data-ttu-id="eee6b-121">Geben Sie MAPI_E_USER_CANCEL an den Anruf Prozess zurück, und beenden Sie, wenn möglich.</span><span class="sxs-lookup"><span data-stu-id="eee6b-121">Return MAPI_E_USER_CANCEL to your calling process and exit, if possible.</span></span> 
  
<span data-ttu-id="eee6b-122">Weitere Informationen zur Angabe des MAPI-Spoolers finden Sie unter [interagieren mit dem MAPI](interacting-with-the-mapi-spooler.md)-Spooler.</span><span class="sxs-lookup"><span data-stu-id="eee6b-122">For more information about yielding to the MAPI spooler, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eee6b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eee6b-123">See also</span></span>



[<span data-ttu-id="eee6b-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="eee6b-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

