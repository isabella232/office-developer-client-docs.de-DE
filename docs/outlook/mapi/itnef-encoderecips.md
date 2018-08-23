---
title: ITnefEncodeRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.EncodeRecips
api_type:
- COM
ms.assetid: b3ce4b0e-4f48-4a7e-a30c-c4754bccb12c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6324dcc567aee48f190f8568c6c94b5ee87c731f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584566"
---
# <a name="itnefencoderecips"></a><span data-ttu-id="9814c-103">ITnef::EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="9814c-103">ITnef::EncodeRecips</span></span>

  
  
<span data-ttu-id="9814c-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9814c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9814c-105">Codiert eine Ansicht für die Empfänger einer Nachricht-Tabelle in der Datenstrom Transport-Neutral Encapsulation Format (TNEF) für die Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="9814c-105">Encodes a view for a message's recipient table in the Transport-Neutral Encapsulation Format (TNEF) data stream for the message.</span></span>
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a><span data-ttu-id="9814c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9814c-106">Parameters</span></span>

 <span data-ttu-id="9814c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9814c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9814c-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="9814c-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="9814c-109">_lpRecipientTable_</span><span class="sxs-lookup"><span data-stu-id="9814c-109">_lpRecipientTable_</span></span>
  
> <span data-ttu-id="9814c-110">[in] Ein Zeiger auf die Empfänger Tabelle, für die die Ansicht codiert ist.</span><span class="sxs-lookup"><span data-stu-id="9814c-110">[in] A pointer to the recipient table for which the view is encoded.</span></span> <span data-ttu-id="9814c-111">Der Parameter _LpRecipientTable_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="9814c-111">The  _lpRecipientTable_ parameter can be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9814c-112">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="9814c-112">Return value</span></span>

<span data-ttu-id="9814c-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="9814c-113">S_OK</span></span> 
  
> <span data-ttu-id="9814c-114">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9814c-114">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9814c-115">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="9814c-115">Remarks</span></span>

<span data-ttu-id="9814c-116">Transport-Anbieter, Nachricht-Anbieter und Gateways Aufruf der **ITnef::EncodeRecips** -Methode zum Ausführen von TNEF-Codierung für eine bestimmte Empfänger Tabelle-Ansicht.</span><span class="sxs-lookup"><span data-stu-id="9814c-116">Transport providers, message store providers, and gateways call the **ITnef::EncodeRecips** method to perform TNEF encoding for a particular recipient table view.</span></span> <span data-ttu-id="9814c-117">TNEF-Codierung ist nützlich, beispielsweise wenn für einen Anbieter oder ein Gateway einer bestimmten Spalte festlegen, die Sortierreihenfolge oder die Einschränkung für die Empfänger Tabelle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9814c-117">TNEF encoding is useful, for example, if a provider or gateway requires a particular column set, sort order, or restriction for the recipient table.</span></span> 
  
<span data-ttu-id="9814c-118">Einen Anbieter oder Gateway übergibt die Tabellenansicht im Parameter _LpRecipientTable_ codiert werden.</span><span class="sxs-lookup"><span data-stu-id="9814c-118">A provider or gateway passes the table view to be encoded in the  _lpRecipientTable_ parameter.</span></span> <span data-ttu-id="9814c-119">Die TNEF-Implementierung codiert Empfänger Tabelle, indem Sie die angegebene Ansicht, mit der angegebenen Spalte festlegen, Sortierreihenfolge, Einschränkung und Position.</span><span class="sxs-lookup"><span data-stu-id="9814c-119">The TNEF implementation encodes the recipient table with the given view, using the given column set, sort order, restriction, and position.</span></span> <span data-ttu-id="9814c-120">Wenn Sie einen Anbieter oder Gateway NULL _LpRecipientTable_übergibt, TNEF Ruft die Empfänger Tabelle aus der Nachricht mit der [IMessage::GetRecipientTable](imessage-getrecipienttable.md) -Methode codiert und verarbeitet jede Zeile der Tabelle in die TNEF-Stream mithilfe der Tabelle des aktuellen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="9814c-120">If a provider or gateway passes NULL in  _lpRecipientTable_, TNEF gets the recipient table from the message being encoded by using the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, and processes every row of the table into the TNEF stream by using the table's current settings.</span></span> 
  
<span data-ttu-id="9814c-121">Aufrufen von **EncodeRecips** mit NULL in _LpRecipientTable_ daher codiert alle Empfänger der Nachricht und entspricht dem Aufrufen der [ITnef::AddProps](itnef-addprops.md) -Methode mit dem TNEF_PROP_INCLUDE-Flag in seiner _UlFlags_ -Parameter und der **PR_ MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))-Eigenschaft im Parameter _LpPropList_ .</span><span class="sxs-lookup"><span data-stu-id="9814c-121">Calling **EncodeRecips** with NULL in  _lpRecipientTable_ thus encodes all message recipients and is equivalent to calling the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag in its  _ulFlags_ parameter and the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in its  _lpPropList_ parameter.</span></span> 
  
<span data-ttu-id="9814c-122">Beachten Sie, dass es nur selten **EncodeRecips** aufrufen, es sei denn, es eine Voraussetzung zum Codieren von einer bestimmten Empfänger Tabellenansicht ist erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9814c-122">Note that it is rarely necessary to call **EncodeRecips** unless there is a requirement to encode a particular recipient table view.</span></span> <span data-ttu-id="9814c-123">Fremde Messagingsysteme haben fast immer Funktionen für die Verarbeitung der Empfängerlisten, die leistungsstark genug, um den allgemeinen Anforderungen Codierung Empfängerlisten zu behandeln sind. Diese Systeme erfordern deshalb fast nie TNEF für diesen Zweck.</span><span class="sxs-lookup"><span data-stu-id="9814c-123">Foreign messaging systems almost always have facilities for handling recipient lists that are powerful enough to handle the common needs of encoding recipient lists; therefore, these systems almost never require TNEF for this purpose.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9814c-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9814c-124">See also</span></span>



[<span data-ttu-id="9814c-125">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="9814c-125">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="9814c-126">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="9814c-126">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="9814c-127">PidTagMessageRecipients (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9814c-127">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="9814c-128">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9814c-128">ITnef : IUnknown</span></span>](itnefiunknown.md)

