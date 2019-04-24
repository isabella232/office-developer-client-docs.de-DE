---
title: IXPLogonEndMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.EndMessage
api_type:
- COM
ms.assetid: bb29e6a0-7a92-46eb-bbeb-6f2df6ac6d21
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 03eccfe27c6f93e42ee01a34fbf5df766c145cf1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357351"
---
# <a name="ixplogonendmessage"></a><span data-ttu-id="d91ee-103">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="d91ee-103">IXPLogon::EndMessage</span></span>

  
  
<span data-ttu-id="d91ee-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d91ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d91ee-105">Informiert den Transportanbieter darüber, dass der MAPI-Spooler seine Verarbeitung für eine ausgehende Nachricht abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="d91ee-105">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d91ee-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d91ee-106">Parameters</span></span>

 <span data-ttu-id="d91ee-107">_ulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="d91ee-107">_ulMsgRef_</span></span>
  
> <span data-ttu-id="d91ee-108">in Ein Nachrichten spezifischer Verweiswert, der in einem früheren Aufruf der [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) -Methode abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="d91ee-108">[in] A message-specific reference value that was obtained in an earlier call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> 
    
 <span data-ttu-id="d91ee-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="d91ee-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="d91ee-110">Out Eine Bitmaske von Flags, die dem MAPI-Spooler mitteilen, was er mit der Nachricht tun soll.</span><span class="sxs-lookup"><span data-stu-id="d91ee-110">[out] A bitmask of flags that indicates to the MAPI spooler what it should do with the message.</span></span> <span data-ttu-id="d91ee-111">Wenn keine Flags festgelegt sind, wurde die Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="d91ee-111">If no flags are set, the message has been sent.</span></span> <span data-ttu-id="d91ee-112">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d91ee-112">The following flags can be set:</span></span>
    
<span data-ttu-id="d91ee-113">END_DONT_RESEND</span><span class="sxs-lookup"><span data-stu-id="d91ee-113">END_DONT_RESEND</span></span> 
  
> <span data-ttu-id="d91ee-114">Der Transportanbieter verfügt jetzt über alle erforderlichen Informationen zu dieser Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d91ee-114">The transport provider has all the information it needs about this message for now.</span></span> <span data-ttu-id="d91ee-115">Wenn der Transportanbieter Weitere Informationen benötigt oder wenn er die Nachricht gesendet hat, benachrichtigt er den MAPI-Spooler durch Aufrufen der [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) -Methode mit dem NOTIFY_SENTDEFERRED-Flag und durch übergeben der Eintrags-ID der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d91ee-115">When the transport provider requires more information or when it has sent the message, it notifies the MAPI spooler by calling the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag and by passing the message's entry identifier.</span></span> 
    
<span data-ttu-id="d91ee-116">END_RESEND_LATER</span><span class="sxs-lookup"><span data-stu-id="d91ee-116">END_RESEND_LATER</span></span> 
  
> <span data-ttu-id="d91ee-117">Der Transportanbieter sendet die Nachricht nicht zum aktuellen Zeitpunkt aus Gründen, die keine Fehlerbedingungen sind.</span><span class="sxs-lookup"><span data-stu-id="d91ee-117">The transport provider is not sending the message at the current time for reasons that are not error conditions.</span></span> <span data-ttu-id="d91ee-118">Der Transportanbieter sollte später erneut aufgerufen werden, um die Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="d91ee-118">The transport provider should be called again later to send the message.</span></span>
    
<span data-ttu-id="d91ee-119">END_RESEND_NOW</span><span class="sxs-lookup"><span data-stu-id="d91ee-119">END_RESEND_NOW</span></span> 
  
> <span data-ttu-id="d91ee-120">Der Transportanbieter muss die an ihn übergebene Nachricht in einem [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methodenaufruf neu starten.</span><span class="sxs-lookup"><span data-stu-id="d91ee-120">The transport provider needs to restart the message passed to it in an [IMessage::SubmitMessage](imessage-submitmessage.md) method call.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d91ee-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d91ee-121">Return value</span></span>

<span data-ttu-id="d91ee-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="d91ee-122">S_OK</span></span> 
  
> <span data-ttu-id="d91ee-123">Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d91ee-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d91ee-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d91ee-124">Remarks</span></span>

<span data-ttu-id="d91ee-125">Die MAPI-Warteschlange ruft die **IXPLogon:: EndMessage** -Methode auf, nachdem Sie die Verarbeitung abgeschlossen hat, die für die Bereitstellung erweiterter Zustellungs-oder Unzustellbarkeits Informationen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d91ee-125">The MAPI spooler calls the **IXPLogon::EndMessage** method after it completes the processing involved in providing extended delivery or nondelivery information.</span></span> 
  
<span data-ttu-id="d91ee-126">Sobald dieser Aufruf zurückgegeben wird, ist der Wert im _ulMsgRef_ -Parameter für diese Nachricht nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="d91ee-126">Once this call returns, the value in the  _ulMsgRef_ parameter is no longer valid for this message.</span></span> <span data-ttu-id="d91ee-127">Der Transportanbieter kann denselben Wert für eine zukünftige Nachricht wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="d91ee-127">The transport provider can reuse the same value on a future message.</span></span> 
  
<span data-ttu-id="d91ee-128">Alle Objekte, die der Transportanbieter während der Übertragung einer Nachricht öffnet, sollten freigegeben werden, bevor der **EndMessage** -Aufruf zurückgegeben wird, mit Ausnahme des Message-Objekts, das vom MAPI-Spooler an den Transportanbieter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d91ee-128">All objects that the transport provider opens during the transfer of a message should be released before the **EndMessage** call returns, with the exception of the message object that the MAPI spooler passes to the transport provider.</span></span> <span data-ttu-id="d91ee-129">Das vom MAPI-Spooler übergebene Nachrichtenobjekt ist nach dem **EndMessage** -Aufruf ungültig.</span><span class="sxs-lookup"><span data-stu-id="d91ee-129">The message object passed by the MAPI spooler is invalid after the **EndMessage** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d91ee-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d91ee-130">See also</span></span>



[<span data-ttu-id="d91ee-131">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="d91ee-131">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="d91ee-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="d91ee-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="d91ee-133">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="d91ee-133">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="d91ee-134">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d91ee-134">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

