---
title: HandsOffAfterSave-Status
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 85630965c7e78e6fa76e348bfe98cc9060665057
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406605"
---
# <a name="handsoffaftersave-state"></a><span data-ttu-id="0eb75-103">HandsOffAfterSave-Status</span><span class="sxs-lookup"><span data-stu-id="0eb75-103">HandsOffAfterSave State</span></span>

  
  
<span data-ttu-id="0eb75-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0eb75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0eb75-105">Der HandsOffAfterSave-Zustand ist Teil des Prozesses zum Speichern des Inhalts eines Formulars in einem permanenten Speicher.</span><span class="sxs-lookup"><span data-stu-id="0eb75-105">The HandsOffAfterSave state is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="0eb75-106">Wenn Sie in diesem Zustand sind, sollte das Form-Objekt keine Änderungen an den in-Memory-Kopien von Werten der Eigenschaften der Nachricht vornehmen, da es möglicherweise keine weitere Möglichkeit gibt, diese Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="0eb75-106">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="0eb75-107">In der folgenden Tabelle werden zulässige Übergänge vom HandsOffAfterSave-Status beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0eb75-107">The following table describes allowed transitions from the HandsOffAfterSave state.</span></span>
  
|<span data-ttu-id="0eb75-108">**IPersistMessage-Methode**</span><span class="sxs-lookup"><span data-stu-id="0eb75-108">**IPersistMessage method**</span></span>|<span data-ttu-id="0eb75-109">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="0eb75-109">**Action**</span></span>|<span data-ttu-id="0eb75-110">**Neuer Status**</span><span class="sxs-lookup"><span data-stu-id="0eb75-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0eb75-111">[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ null)</span><span class="sxs-lookup"><span data-stu-id="0eb75-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="0eb75-112">Öffnen Sie eingebettete Objekte.</span><span class="sxs-lookup"><span data-stu-id="0eb75-112">Open any embedded objects.</span></span> <span data-ttu-id="0eb75-113">Die Daten in der in _pMessage_ gespeicherten Nachricht werden mit der Nachricht im vorherigen [IPersistMessage:: Save](ipersistmessage-save.md) -Aufruf identisch sein.</span><span class="sxs-lookup"><span data-stu-id="0eb75-113">The data in the message stored in  _pMessage_ is guaranteed to be the same as the message in the previous [IPersistMessage::Save](ipersistmessage-save.md) call.</span></span> <span data-ttu-id="0eb75-114">Wenn der **SaveCompleted** -Aufruf erfolgreich ist, geben Sie den normalen Status ein.</span><span class="sxs-lookup"><span data-stu-id="0eb75-114">If the **SaveCompleted** call succeeds, enter the Normal state.</span></span> <span data-ttu-id="0eb75-115">Andernfalls legen Sie den letzten Fehler auf E_OUTOFMEMORY und bleiben im HandsOffAfterSave-Zustand.</span><span class="sxs-lookup"><span data-stu-id="0eb75-115">Otherwise, set the last error to E_OUTOFMEMORY and stay in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="0eb75-116">[Normal](normal-state.md) oder HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="0eb75-116">[Normal](normal-state.md) or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="0eb75-117">**IPersistMessage:: SaveCompleted** (_pMessage = =_ null)</span><span class="sxs-lookup"><span data-stu-id="0eb75-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="0eb75-118">Legen Sie den letzten Fehler auf E_INVALIDARG oder E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="0eb75-118">Set the last error to E_INVALIDARG or E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="0eb75-119">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="0eb75-119">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="0eb75-120">[IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**oder [IPersistMessage:: InitNew](ipersistmessage-initnew.md)</span><span class="sxs-lookup"><span data-stu-id="0eb75-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, or [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span></span> <br/> |<span data-ttu-id="0eb75-121">Legen Sie den letzten Fehler an und geben Sie E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="0eb75-121">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="0eb75-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="0eb75-122">HandsOffAfterSave</span></span>  <br/> |
|[<span data-ttu-id="0eb75-123">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="0eb75-123">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="0eb75-124">Laden Sie das Form-Objekt mit Daten aus der Zielnachricht.</span><span class="sxs-lookup"><span data-stu-id="0eb75-124">Load the form object with data from the target message.</span></span> <span data-ttu-id="0eb75-125">Dieser Aufruf kann auftreten, wenn das Form-Objekt zur nächsten oder vorherigen Nachricht in einem Ordner geht.</span><span class="sxs-lookup"><span data-stu-id="0eb75-125">This call can occur when the form object is going to the next or previous message in a folder.</span></span>  <br/> |<span data-ttu-id="0eb75-126">Normal</span><span class="sxs-lookup"><span data-stu-id="0eb75-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="0eb75-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0eb75-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="0eb75-128">Zurückgeben des letzten Fehlers.</span><span class="sxs-lookup"><span data-stu-id="0eb75-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="0eb75-129">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="0eb75-129">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="0eb75-130">Andere [IPersistMessage: IUnknown](ipersistmessageiunknown.md) -Methoden oder Methoden von anderen Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0eb75-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="0eb75-131">Legen Sie den letzten Fehler an und geben Sie E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="0eb75-131">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="0eb75-132">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="0eb75-132">HandsOffAfterSave</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0eb75-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0eb75-133">See also</span></span>



[<span data-ttu-id="0eb75-134">Formular Status</span><span class="sxs-lookup"><span data-stu-id="0eb75-134">Form States</span></span>](form-states.md)

