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
ms.openlocfilehash: d90f502e2cd7f97ac273ebecedbd0363097b1d60
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584954"
---
# <a name="imapisupportspooleryield"></a><span data-ttu-id="d25cb-103">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="d25cb-103">IMAPISupport::SpoolerYield</span></span>

  
  
<span data-ttu-id="d25cb-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d25cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d25cb-105">Bietet Kontrolle über die CPU auf die MAPI-Warteschlange, damit sie alle Aufgaben ausführen kann, notwendig hält.</span><span class="sxs-lookup"><span data-stu-id="d25cb-105">Gives control of the CPU to the MAPI spooler so that it can perform any tasks it considers necessary.</span></span>
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d25cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d25cb-106">Parameters</span></span>

 <span data-ttu-id="d25cb-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d25cb-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d25cb-108">Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="d25cb-108">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d25cb-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="d25cb-109">Return value</span></span>

<span data-ttu-id="d25cb-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d25cb-110">S_OK</span></span> 
  
> <span data-ttu-id="d25cb-111">Der Transportdienst veröffentlicht erfolgreich CPU.</span><span class="sxs-lookup"><span data-stu-id="d25cb-111">The transport provider successfully released the CPU.</span></span>
    
<span data-ttu-id="d25cb-112">MAPI_W_CANCEL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="d25cb-112">MAPI_W_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="d25cb-113">Weist der Adressbuchhierarchie So beenden Sie die Zustellung der Nachricht an alle Empfänger, die noch nicht erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="d25cb-113">Instructs the transport provider to stop the delivery of the message to any recipients that have not yet received it.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d25cb-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="d25cb-114">Remarks</span></span>

<span data-ttu-id="d25cb-115">Die **IMAPISupport::SpoolerYield** -Methode wird für Transport Anbieter Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="d25cb-115">The **IMAPISupport::SpoolerYield** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="d25cb-116">Transportanbieter Aufrufen **SpoolerYield** , um die MAPI-Warteschlange, die erforderliche Verarbeitung bezwecken zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="d25cb-116">Transport providers call **SpoolerYield** to allow the MAPI spooler to accomplish any necessary processing.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d25cb-117">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="d25cb-117">Notes to callers</span></span>

<span data-ttu-id="d25cb-118">Rufen Sie **SpoolerYield** , wenn Sie langer Vorgänge ausführen, die angehalten werden können.</span><span class="sxs-lookup"><span data-stu-id="d25cb-118">Call **SpoolerYield** when you are performing lengthy operations that can be paused.</span></span> <span data-ttu-id="d25cb-119">Dadurch können Vordergrund während eines langen Vorgangs, wie die Zustellung an eine große Empfängerliste über Datenverkehrsaufkommen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d25cb-119">This allows foreground applications to run during a long operation, such as delivery to a large recipient list across a busy network.</span></span> 
  
<span data-ttu-id="d25cb-120">Wenn **SpoolerYield** mit MAPI_W_CANCEL_MESSAGE zurückgibt, wurde die MAPI-Warteschlange festgestellt, dass die Nachricht nicht mehr gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d25cb-120">If **SpoolerYield** returns with MAPI_W_CANCEL_MESSAGE, the MAPI spooler has determined that the message should no longer be sent.</span></span> <span data-ttu-id="d25cb-121">Geben Sie nach Möglichkeit MAPI_E_USER_CANCEL an die aufrufende Prozess und beenden, zurück.</span><span class="sxs-lookup"><span data-stu-id="d25cb-121">Return MAPI_E_USER_CANCEL to your calling process and exit, if possible.</span></span> 
  
<span data-ttu-id="d25cb-122">Weitere Informationen dazu, die MAPI-Warteschlange Zurückhalten finden Sie unter [Interaktion mit der MAPI-Warteschlange](interacting-with-the-mapi-spooler.md).</span><span class="sxs-lookup"><span data-stu-id="d25cb-122">For more information about yielding to the MAPI spooler, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d25cb-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d25cb-123">See also</span></span>



[<span data-ttu-id="d25cb-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d25cb-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

