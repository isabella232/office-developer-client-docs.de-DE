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
# <a name="itnefencoderecips"></a><span data-ttu-id="85da1-103">ITnef::EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="85da1-103">ITnef::EncodeRecips</span></span>

  
  
<span data-ttu-id="85da1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85da1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85da1-105">Codiert eine Ansicht für die Empfängertabelle einer Nachricht im TNEF-Datenstrom (Transport-Neutral Encapsulation Format) für die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="85da1-105">Encodes a view for a message's recipient table in the Transport-Neutral Encapsulation Format (TNEF) data stream for the message.</span></span>
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a><span data-ttu-id="85da1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="85da1-106">Parameters</span></span>

 <span data-ttu-id="85da1-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="85da1-107">_ulFlags_</span></span>
  
> <span data-ttu-id="85da1-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="85da1-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="85da1-109">_lpRecipientTable_</span><span class="sxs-lookup"><span data-stu-id="85da1-109">_lpRecipientTable_</span></span>
  
> <span data-ttu-id="85da1-110">in Ein Zeiger auf die Empfängertabelle, für die die Ansicht codiert ist.</span><span class="sxs-lookup"><span data-stu-id="85da1-110">[in] A pointer to the recipient table for which the view is encoded.</span></span> <span data-ttu-id="85da1-111">Der _lpRecipientTable_ -Parameter kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="85da1-111">The  _lpRecipientTable_ parameter can be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="85da1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85da1-112">Return value</span></span>

<span data-ttu-id="85da1-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="85da1-113">S_OK</span></span> 
  
> <span data-ttu-id="85da1-114">Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="85da1-114">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="85da1-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85da1-115">Remarks</span></span>

<span data-ttu-id="85da1-116">Transport Anbieter, Nachrichtenspeicher Anbieter und Gateways rufen die **ITnef:: EncodeRecips** -Methode auf, um die TNEF-Codierung für eine bestimmte Empfänger Tabellenansicht durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="85da1-116">Transport providers, message store providers, and gateways call the **ITnef::EncodeRecips** method to perform TNEF encoding for a particular recipient table view.</span></span> <span data-ttu-id="85da1-117">Die TNEF-Codierung ist beispielsweise nützlich, wenn ein Anbieter oder ein Gateway eine bestimmte Spaltengruppe, Sortierreihenfolge oder Einschränkung für die Empfängertabelle erfordert.</span><span class="sxs-lookup"><span data-stu-id="85da1-117">TNEF encoding is useful, for example, if a provider or gateway requires a particular column set, sort order, or restriction for the recipient table.</span></span> 
  
<span data-ttu-id="85da1-118">Ein Anbieter oder Gateway übergibt die Tabellenansicht, die im Parameter _lpRecipientTable_ codiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="85da1-118">A provider or gateway passes the table view to be encoded in the  _lpRecipientTable_ parameter.</span></span> <span data-ttu-id="85da1-119">Die TNEF-Implementierung codiert die Empfängertabelle mit der angegebenen Ansicht, wobei der angegebene Spaltensatz, die Sortierreihenfolge, die Einschränkung und die Position verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85da1-119">The TNEF implementation encodes the recipient table with the given view, using the given column set, sort order, restriction, and position.</span></span> <span data-ttu-id="85da1-120">Wenn ein Anbieter oder ein Gateway in _LPRECIPIENTTABLE_NULL übergibt, ruft TNEF die Empfängertabelle aus der zu codierenden Nachricht mithilfe der [IMessage::](imessage-getrecipienttable.md) getrecipientable-Methode ab und verarbeitet jede Zeile der Tabelle im TNEF-Stream mithilfe der Aktuelle Einstellungen der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="85da1-120">If a provider or gateway passes NULL in  _lpRecipientTable_, TNEF gets the recipient table from the message being encoded by using the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, and processes every row of the table into the TNEF stream by using the table's current settings.</span></span> 
  
<span data-ttu-id="85da1-121">Das Aufrufen von **EncodeRecips** mit NULL in _lpRecipientTable_ codiert daher alle Nachrichtenempfänger und entspricht dem Aufrufen der [ITnef::](itnef-addprops.md) AddProps-Methode mit dem TNEF_PROP_INCLUDE-Flag im _ulFlags_ -Parameter und dem **PR_ MESSAGE_RECIPIENTS** ([pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md))-Eigenschaft im _lpPropList_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="85da1-121">Calling **EncodeRecips** with NULL in  _lpRecipientTable_ thus encodes all message recipients and is equivalent to calling the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag in its  _ulFlags_ parameter and the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in its  _lpPropList_ parameter.</span></span> 
  
<span data-ttu-id="85da1-122">Beachten Sie, dass es selten erforderlich ist, **EncodeRecips** aufzurufen, es sei denn, eine bestimmte Empfänger Tabellenansicht muss codiert werden.</span><span class="sxs-lookup"><span data-stu-id="85da1-122">Note that it is rarely necessary to call **EncodeRecips** unless there is a requirement to encode a particular recipient table view.</span></span> <span data-ttu-id="85da1-123">Ausländische Messagingsysteme verfügen fast immer über Einrichtungen für die Verarbeitung von Empfängerlisten, die leistungsfähig genug sind, um die allgemeinen Anforderungen der Codierung von Empfängerlisten zu bewältigen. Daher benötigen diese Systeme für diesen Zweck fast nie TNEF.</span><span class="sxs-lookup"><span data-stu-id="85da1-123">Foreign messaging systems almost always have facilities for handling recipient lists that are powerful enough to handle the common needs of encoding recipient lists; therefore, these systems almost never require TNEF for this purpose.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="85da1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85da1-124">See also</span></span>



[<span data-ttu-id="85da1-125">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="85da1-125">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="85da1-126">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="85da1-126">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="85da1-127">Kanonische Pidtagmessagerecipients (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="85da1-127">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="85da1-128">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="85da1-128">ITnef : IUnknown</span></span>](itnefiunknown.md)

