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
ms.openlocfilehash: d8caa503e557d35e259db743505d39ea4809dbfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437651"
---
# <a name="itnefencoderecips"></a><span data-ttu-id="b660e-103">ITnef::EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="b660e-103">ITnef::EncodeRecips</span></span>

  
  
<span data-ttu-id="b660e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b660e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b660e-105">Codiert eine Ansicht für die Empfängertabelle einer Nachricht im Transport-Neutral Encapsulation Format (TNEF)-Datenstrom für die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b660e-105">Encodes a view for a message's recipient table in the Transport-Neutral Encapsulation Format (TNEF) data stream for the message.</span></span>
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a><span data-ttu-id="b660e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b660e-106">Parameters</span></span>

 <span data-ttu-id="b660e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b660e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b660e-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="b660e-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="b660e-109">_lpRecipientTable_</span><span class="sxs-lookup"><span data-stu-id="b660e-109">_lpRecipientTable_</span></span>
  
> <span data-ttu-id="b660e-110">[in] Ein Zeiger auf die Empfängertabelle, für die die Ansicht codiert ist.</span><span class="sxs-lookup"><span data-stu-id="b660e-110">[in] A pointer to the recipient table for which the view is encoded.</span></span> <span data-ttu-id="b660e-111">Der  _lpRecipientTable-Parameter_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b660e-111">The  _lpRecipientTable_ parameter can be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b660e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b660e-112">Return value</span></span>

<span data-ttu-id="b660e-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="b660e-113">S_OK</span></span> 
  
> <span data-ttu-id="b660e-114">Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b660e-114">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b660e-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b660e-115">Remarks</span></span>

<span data-ttu-id="b660e-116">Transportanbieter, Nachrichtenspeicheranbieter und Gateways rufen die **ITnef::EncodeRecips-Methode** auf, um die TNEF-Codierung für eine bestimmte Empfängertabellesansicht durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="b660e-116">Transport providers, message store providers, and gateways call the **ITnef::EncodeRecips** method to perform TNEF encoding for a particular recipient table view.</span></span> <span data-ttu-id="b660e-117">Die TNEF-Codierung ist z. B. hilfreich, wenn ein Anbieter oder Gateway einen bestimmten Spaltensatz, eine Sortierreihenfolge oder eine Einschränkung für die Empfängertabelle erfordert.</span><span class="sxs-lookup"><span data-stu-id="b660e-117">TNEF encoding is useful, for example, if a provider or gateway requires a particular column set, sort order, or restriction for the recipient table.</span></span> 
  
<span data-ttu-id="b660e-118">Ein Anbieter oder Gateway übergibt die Tabellenansicht, die im  _lpRecipientTable-Parameter codiert werden_ soll.</span><span class="sxs-lookup"><span data-stu-id="b660e-118">A provider or gateway passes the table view to be encoded in the  _lpRecipientTable_ parameter.</span></span> <span data-ttu-id="b660e-119">Die TNEF-Implementierung codiert die Empfängertabelle mit der angegebenen Ansicht mithilfe der angegebenen Spaltensatz, Sortierreihenfolge, Einschränkung und Position.</span><span class="sxs-lookup"><span data-stu-id="b660e-119">The TNEF implementation encodes the recipient table with the given view, using the given column set, sort order, restriction, and position.</span></span> <span data-ttu-id="b660e-120">Wenn ein Anbieter oder Gateway NULL in  _lpRecipientTable_ übergibt, ruft TNEF die Empfängertabelle aus der Nachricht ab, die mithilfe der [IMessage::GetRecipientTable-Methode](imessage-getrecipienttable.md) codiert wird, und verarbeitet jede Zeile der Tabelle mithilfe der aktuellen Einstellungen der Tabelle in den TNEF-Stream.</span><span class="sxs-lookup"><span data-stu-id="b660e-120">If a provider or gateway passes NULL in  _lpRecipientTable_, TNEF gets the recipient table from the message being encoded by using the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, and processes every row of the table into the TNEF stream by using the table's current settings.</span></span> 
  
<span data-ttu-id="b660e-121">Das Aufrufen von **EncodeRecips** mit NULL in _lpRecipientTable_ codiert daher alle Nachrichtenempfänger und entspricht dem Aufrufen der [ITnef::AddProps-Methode](itnef-addprops.md) mit dem TNEF_PROP_INCLUDE-Flag im _ulFlags-Parameter_ und der **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))-Eigenschaft im _lpPropList-Parameter._</span><span class="sxs-lookup"><span data-stu-id="b660e-121">Calling **EncodeRecips** with NULL in  _lpRecipientTable_ thus encodes all message recipients and is equivalent to calling the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag in its  _ulFlags_ parameter and the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in its  _lpPropList_ parameter.</span></span> 
  
<span data-ttu-id="b660e-122">Beachten Sie, dass es selten erforderlich **ist, EncodeRecips** aufzugeben, es sei denn, es ist erforderlich, eine bestimmte Empfängertabelle zu codieren.</span><span class="sxs-lookup"><span data-stu-id="b660e-122">Note that it is rarely necessary to call **EncodeRecips** unless there is a requirement to encode a particular recipient table view.</span></span> <span data-ttu-id="b660e-123">Fremde Messagingsysteme verfügen fast immer über Möglichkeiten zum Behandeln von Empfängerlisten, die leistungsfähig genug sind, um die allgemeinen Anforderungen der Codierung von Empfängerlisten zu erfüllen. Daher benötigen diese Systeme zu diesem Zweck fast nie TNEF.</span><span class="sxs-lookup"><span data-stu-id="b660e-123">Foreign messaging systems almost always have facilities for handling recipient lists that are powerful enough to handle the common needs of encoding recipient lists; therefore, these systems almost never require TNEF for this purpose.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b660e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b660e-124">See also</span></span>



[<span data-ttu-id="b660e-125">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="b660e-125">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="b660e-126">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="b660e-126">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="b660e-127">PidTagMessageRecipients (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b660e-127">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="b660e-128">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b660e-128">ITnef : IUnknown</span></span>](itnefiunknown.md)

