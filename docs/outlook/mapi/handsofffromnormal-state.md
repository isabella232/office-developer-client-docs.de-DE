---
title: Status „HandsOffFromNormal“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d0b7baf4ab17d12145170961a43ca4be252146a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791831"
---
# <a name="handsofffromnormal-state"></a><span data-ttu-id="12037-103">Status „HandsOffFromNormal“</span><span class="sxs-lookup"><span data-stu-id="12037-103">HandsOffFromNormal State</span></span>

  
  
<span data-ttu-id="12037-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="12037-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="12037-105">Der Zustand HandsOffFromNormal ist auf den Status [HandsOffAfterSave](handsoffaftersave-state.md) sehr ähnlich.</span><span class="sxs-lookup"><span data-stu-id="12037-105">The HandsOffFromNormal state is very similar to the [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> <span data-ttu-id="12037-106">Es ist Teil des Prozesses zum Speichern des Inhalts eines Formulars dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="12037-106">It is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="12037-107">In diesem Status sollte das Form-Objekt sehen davon ab, die speicherinterne Kopien der Werte der Eigenschaften für die Nachricht, ändern, da es möglicherweise nicht eine weitere Möglichkeit, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="12037-107">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="12037-108">In der folgenden Tabelle werden die zulässigen Übergänge aus dem Status HandsOffFromNormal beschrieben.</span><span class="sxs-lookup"><span data-stu-id="12037-108">The following table describes allowed transitions from the HandsOffFromNormal state.</span></span> 
  
|<span data-ttu-id="12037-109">IPersistMessage **-Methode **</span><span class="sxs-lookup"><span data-stu-id="12037-109">****IPersistMessage** method**</span></span>|<span data-ttu-id="12037-110">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="12037-110">**Action**</span></span>|<span data-ttu-id="12037-111">**Neue Zustand**</span><span class="sxs-lookup"><span data-stu-id="12037-111">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="12037-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ NULL)</span><span class="sxs-lookup"><span data-stu-id="12037-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="12037-113">Ersetzen Sie das Meldungsobjekt Nachricht durch _pMessage_, der Ersatz für die Nachricht durch den vorherigen Aufruf [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="12037-113">Replace the message object's message with  _pMessage_, which is the replacement for the message revoked by the previous call to [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md).</span></span> <span data-ttu-id="12037-114">Die Daten in die neue Nachricht ist dieselbe wie die gesperrten Nachricht garantiert.</span><span class="sxs-lookup"><span data-stu-id="12037-114">The data in the new message is guaranteed to be the same as in the revoked message.</span></span> <span data-ttu-id="12037-115">Die Nachricht nicht als clean gekennzeichnet werden soll, und sollte nach diesem Aufruf [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="12037-115">The message should not be marked as clean, nor should [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) be called after this call.</span></span> <span data-ttu-id="12037-116">Wenn der **SaveCompleted** Aufruf erfolgreich ist, geben Sie den [normalen](normal-state.md) Zustand.</span><span class="sxs-lookup"><span data-stu-id="12037-116">If the **SaveCompleted** call succeeds, enter the [Normal](normal-state.md) state.</span></span> <span data-ttu-id="12037-117">Bleiben Sie andernfalls den Status HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="12037-117">Otherwise, stay in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="12037-118">Normal oder HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="12037-118">Normal or HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="12037-119">**IPersistMessage::SaveCompleted** (_pMessage ==_ NULL)</span><span class="sxs-lookup"><span data-stu-id="12037-119">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="12037-120">Legen Sie den letzten Fehler auf E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="12037-120">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="12037-121">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="12037-121">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="12037-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md)oder [IPersistMessage::Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="12037-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="12037-123">Legen Sie den letzten Fehler auf E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="12037-123">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="12037-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="12037-124">HandsOffFromNormal</span></span>  <br/> |
|[<span data-ttu-id="12037-125">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="12037-125">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="12037-126">Geben Sie den letzten Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="12037-126">Return the last error.</span></span>  <br/> |<span data-ttu-id="12037-127">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="12037-127">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="12037-128">Andere [IPersistMessage: IUnknown](ipersistmessageiunknown.md) Methoden oder Methoden aus anderen Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="12037-128">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="12037-129">Legen Sie den letzten Fehler auf E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="12037-129">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="12037-130">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="12037-130">HandsOffFromNormal</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="12037-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12037-131">See also</span></span>



[<span data-ttu-id="12037-132">Formularstatus</span><span class="sxs-lookup"><span data-stu-id="12037-132">Form States</span></span>](form-states.md)

