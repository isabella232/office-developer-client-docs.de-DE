---
title: HandsOffAfterSave Zustand
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4bc4d680903d81b51a39ed39db3861597443d116
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791823"
---
# <a name="handsoffaftersave-state"></a><span data-ttu-id="8e45a-103">HandsOffAfterSave Zustand</span><span class="sxs-lookup"><span data-stu-id="8e45a-103">HandsOffAfterSave State</span></span>

  
  
<span data-ttu-id="8e45a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e45a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8e45a-105">Der Zustand HandsOffAfterSave ist Teil des Prozesses zum Speichern des Inhalts eines Formulars dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="8e45a-105">The HandsOffAfterSave state is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="8e45a-106">In diesem Status sollte das Form-Objekt sehen davon ab, die speicherinterne Kopien der Werte der Eigenschaften für die Nachricht, ändern, da es möglicherweise nicht eine weitere Möglichkeit, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="8e45a-106">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="8e45a-107">In der folgenden Tabelle werden die zulässigen Übergänge aus dem Status HandsOffAfterSave beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8e45a-107">The following table describes allowed transitions from the HandsOffAfterSave state.</span></span>
  
|<span data-ttu-id="8e45a-108">**IPersistMessage-Methode**</span><span class="sxs-lookup"><span data-stu-id="8e45a-108">**IPersistMessage method**</span></span>|<span data-ttu-id="8e45a-109">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="8e45a-109">**Action**</span></span>|<span data-ttu-id="8e45a-110">**Neue Zustand**</span><span class="sxs-lookup"><span data-stu-id="8e45a-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8e45a-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ NULL)</span><span class="sxs-lookup"><span data-stu-id="8e45a-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="8e45a-112">Eingebettete Objekte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8e45a-112">Open any embedded objects.</span></span> <span data-ttu-id="8e45a-113">Die Daten in der Nachricht in _pMessage_ gespeichert werden unbedingt die Nachricht in der vorherigen Aufruf der [IPersistMessage::Save](ipersistmessage-save.md) identisch sein.</span><span class="sxs-lookup"><span data-stu-id="8e45a-113">The data in the message stored in  _pMessage_ is guaranteed to be the same as the message in the previous [IPersistMessage::Save](ipersistmessage-save.md) call.</span></span> <span data-ttu-id="8e45a-114">Wenn der Anruf **SaveCompleted** erfolgreich ist, geben Sie die normalen Zustand.</span><span class="sxs-lookup"><span data-stu-id="8e45a-114">If the **SaveCompleted** call succeeds, enter the Normal state.</span></span> <span data-ttu-id="8e45a-115">Andernfalls legen Sie den letzten Fehler auf E_OUTOFMEMORY und bleiben Sie in der HandsOffAfterSave Zustand.</span><span class="sxs-lookup"><span data-stu-id="8e45a-115">Otherwise, set the last error to E_OUTOFMEMORY and stay in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="8e45a-116">[Normal](normal-state.md) oder HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="8e45a-116">[Normal](normal-state.md) or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="8e45a-117">**IPersistMessage::SaveCompleted** (_pMessage ==_ NULL)</span><span class="sxs-lookup"><span data-stu-id="8e45a-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="8e45a-118">Legen Sie den letzten Fehler auf E_INVALIDARG oder E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="8e45a-118">Set the last error to E_INVALIDARG or E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="8e45a-119">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="8e45a-119">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="8e45a-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Speichern**oder [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span><span class="sxs-lookup"><span data-stu-id="8e45a-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, or [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span></span> <br/> |<span data-ttu-id="8e45a-121">Legen Sie den letzten Fehler auf und zurückgeben Sie E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="8e45a-121">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="8e45a-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="8e45a-122">HandsOffAfterSave</span></span>  <br/> |
|[<span data-ttu-id="8e45a-123">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="8e45a-123">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="8e45a-124">Laden Sie das Form-Objekt mit Daten aus der Zielnachricht.</span><span class="sxs-lookup"><span data-stu-id="8e45a-124">Load the form object with data from the target message.</span></span> <span data-ttu-id="8e45a-125">Dieses Anrufs kann auftreten, wenn das Form-Objekt an der nächsten oder der vorherigen Nachricht in einem Ordner geht.</span><span class="sxs-lookup"><span data-stu-id="8e45a-125">This call can occur when the form object is going to the next or previous message in a folder.</span></span>  <br/> |<span data-ttu-id="8e45a-126">Standard</span><span class="sxs-lookup"><span data-stu-id="8e45a-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="8e45a-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8e45a-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="8e45a-128">Geben Sie den letzten Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="8e45a-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="8e45a-129">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="8e45a-129">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="8e45a-130">Andere [IPersistMessage: IUnknown](ipersistmessageiunknown.md) Methoden oder Methoden aus anderen Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8e45a-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="8e45a-131">Legen Sie den letzten Fehler auf und zurückgeben Sie E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="8e45a-131">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="8e45a-132">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="8e45a-132">HandsOffAfterSave</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e45a-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e45a-133">See also</span></span>



[<span data-ttu-id="8e45a-134">Formular Staaten</span><span class="sxs-lookup"><span data-stu-id="8e45a-134">Form States</span></span>](form-states.md)

