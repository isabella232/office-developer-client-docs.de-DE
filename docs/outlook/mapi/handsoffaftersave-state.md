---
title: Status „HandsOffAfterSave“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 274e7206171e1874e3625896952f861d25f3b382
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564535"
---
# <a name="handsoffaftersave-state"></a><span data-ttu-id="d0e28-103">Status „HandsOffAfterSave“</span><span class="sxs-lookup"><span data-stu-id="d0e28-103">HandsOffAfterSave State</span></span>

  
  
<span data-ttu-id="d0e28-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0e28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0e28-105">Der Zustand HandsOffAfterSave ist Teil des Prozesses zum Speichern des Inhalts eines Formulars dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="d0e28-105">The HandsOffAfterSave state is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="d0e28-106">In diesem Status sollte das Form-Objekt sehen davon ab, die speicherinterne Kopien der Werte der Eigenschaften für die Nachricht, ändern, da es möglicherweise nicht eine weitere Möglichkeit, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d0e28-106">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="d0e28-107">In der folgenden Tabelle werden die zulässigen Übergänge aus dem Status HandsOffAfterSave beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d0e28-107">The following table describes allowed transitions from the HandsOffAfterSave state.</span></span>
  
|<span data-ttu-id="d0e28-108">**IPersistMessage-Methode**</span><span class="sxs-lookup"><span data-stu-id="d0e28-108">**IPersistMessage method**</span></span>|<span data-ttu-id="d0e28-109">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="d0e28-109">**Action**</span></span>|<span data-ttu-id="d0e28-110">**Neue Zustand**</span><span class="sxs-lookup"><span data-stu-id="d0e28-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d0e28-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ NULL)</span><span class="sxs-lookup"><span data-stu-id="d0e28-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="d0e28-112">Eingebettete Objekte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d0e28-112">Open any embedded objects.</span></span> <span data-ttu-id="d0e28-113">Die Daten in der Nachricht in _pMessage_ gespeichert werden unbedingt die Nachricht in der vorherigen Aufruf der [IPersistMessage::Save](ipersistmessage-save.md) identisch sein.</span><span class="sxs-lookup"><span data-stu-id="d0e28-113">The data in the message stored in  _pMessage_ is guaranteed to be the same as the message in the previous [IPersistMessage::Save](ipersistmessage-save.md) call.</span></span> <span data-ttu-id="d0e28-114">Wenn der Anruf **SaveCompleted** erfolgreich ist, geben Sie die normalen Zustand.</span><span class="sxs-lookup"><span data-stu-id="d0e28-114">If the **SaveCompleted** call succeeds, enter the Normal state.</span></span> <span data-ttu-id="d0e28-115">Andernfalls legen Sie den letzten Fehler auf E_OUTOFMEMORY und bleiben Sie in der HandsOffAfterSave Zustand.</span><span class="sxs-lookup"><span data-stu-id="d0e28-115">Otherwise, set the last error to E_OUTOFMEMORY and stay in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="d0e28-116">[Normal](normal-state.md) oder HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="d0e28-116">[Normal](normal-state.md) or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="d0e28-117">**IPersistMessage::SaveCompleted** (_pMessage ==_ NULL)</span><span class="sxs-lookup"><span data-stu-id="d0e28-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="d0e28-118">Legen Sie den letzten Fehler auf E_INVALIDARG oder E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="d0e28-118">Set the last error to E_INVALIDARG or E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="d0e28-119">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="d0e28-119">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="d0e28-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Speichern**oder [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span><span class="sxs-lookup"><span data-stu-id="d0e28-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, or [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span></span> <br/> |<span data-ttu-id="d0e28-121">Legen Sie den letzten Fehler auf und zurückgeben Sie E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="d0e28-121">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="d0e28-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="d0e28-122">HandsOffAfterSave</span></span>  <br/> |
|[<span data-ttu-id="d0e28-123">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="d0e28-123">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="d0e28-124">Laden Sie das Form-Objekt mit Daten aus der Zielnachricht.</span><span class="sxs-lookup"><span data-stu-id="d0e28-124">Load the form object with data from the target message.</span></span> <span data-ttu-id="d0e28-125">Dieses Anrufs kann auftreten, wenn das Form-Objekt an der nächsten oder der vorherigen Nachricht in einem Ordner geht.</span><span class="sxs-lookup"><span data-stu-id="d0e28-125">This call can occur when the form object is going to the next or previous message in a folder.</span></span>  <br/> |<span data-ttu-id="d0e28-126">Standard</span><span class="sxs-lookup"><span data-stu-id="d0e28-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="d0e28-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d0e28-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="d0e28-128">Geben Sie den letzten Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="d0e28-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="d0e28-129">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="d0e28-129">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="d0e28-130">Andere [IPersistMessage: IUnknown](ipersistmessageiunknown.md) Methoden oder Methoden aus anderen Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d0e28-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="d0e28-131">Legen Sie den letzten Fehler auf und zurückgeben Sie E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="d0e28-131">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="d0e28-132">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="d0e28-132">HandsOffAfterSave</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0e28-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0e28-133">See also</span></span>



[<span data-ttu-id="d0e28-134">Formularstatus</span><span class="sxs-lookup"><span data-stu-id="d0e28-134">Form States</span></span>](form-states.md)

