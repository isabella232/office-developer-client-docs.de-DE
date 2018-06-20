---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Gibt an, wobei eine Kopie einer Nachricht auf dem Server für ein POP-Konto.
ms.openlocfilehash: 9f986ff60a5824ece0a8bb91619323b58ec8b87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791193"
---
# <a name="proppopleaveonserver"></a><span data-ttu-id="df6a2-103">PROP_POP_LEAVE_ON_SERVER</span><span class="sxs-lookup"><span data-stu-id="df6a2-103">PROP_POP_LEAVE_ON_SERVER</span></span>

<span data-ttu-id="df6a2-104">Gibt an, wobei eine Kopie einer Nachricht auf dem Server für ein POP-Konto.</span><span class="sxs-lookup"><span data-stu-id="df6a2-104">Specifies leaving a copy of a message on the server for a POP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="df6a2-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="df6a2-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df6a2-106">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="df6a2-106">Identifier:</span></span>  <br/> |<span data-ttu-id="df6a2-107">0 x 1000</span><span class="sxs-lookup"><span data-stu-id="df6a2-107">0x1000</span></span>  <br/> |
|<span data-ttu-id="df6a2-108">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="df6a2-108">Property type:</span></span>  <br/> |<span data-ttu-id="df6a2-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="df6a2-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="df6a2-110">Eigenschafts-Tag:</span><span class="sxs-lookup"><span data-stu-id="df6a2-110">Property tag:</span></span>  <br/> |<span data-ttu-id="df6a2-111">0x10000003</span><span class="sxs-lookup"><span data-stu-id="df6a2-111">0x10000003</span></span>  <br/> |
|<span data-ttu-id="df6a2-112">Access:</span><span class="sxs-lookup"><span data-stu-id="df6a2-112">Access:</span></span>  <br/> |<span data-ttu-id="df6a2-113">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="df6a2-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df6a2-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="df6a2-114">Remarks</span></span>

<span data-ttu-id="df6a2-115">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="df6a2-115">The following table lists the possible values.</span></span> <span data-ttu-id="df6a2-116">Weitere Informationen zu Konstanten finden Sie unter [Konstanten (Konto Management-API)](constants-account-management-api.md) .</span><span class="sxs-lookup"><span data-stu-id="df6a2-116">See [Constants (Account management API)](constants-account-management-api.md) for more information on the constants.</span></span> 
  
|<span data-ttu-id="df6a2-117">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="df6a2-117">**Possible values**</span></span>|<span data-ttu-id="df6a2-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="df6a2-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="df6a2-119">**LEAVE_ON_SERVER**</span><span class="sxs-lookup"><span data-stu-id="df6a2-119">**LEAVE_ON_SERVER**</span></span> <br/> |<span data-ttu-id="df6a2-120">Bewirkt, dass eine Kopie der Nachricht auf dem POP-Server nach dem Herunterladen der Nachricht zu einem Gerät.</span><span class="sxs-lookup"><span data-stu-id="df6a2-120">Leaves a copy of the message on the POP server after downloading the message to a device.</span></span>  <br/> |
|<span data-ttu-id="df6a2-121">**REMOVE_AFTER**</span><span class="sxs-lookup"><span data-stu-id="df6a2-121">**REMOVE_AFTER**</span></span> <br/> |<span data-ttu-id="df6a2-122">Entfernt die Nachricht vom POP-Server nach dem Herunterladen zu einem Gerät.</span><span class="sxs-lookup"><span data-stu-id="df6a2-122">Removes the message from the POP server after downloading it to a device.</span></span>  <br/> |
|<span data-ttu-id="df6a2-123">**REMOVE_ON_NUKE**</span><span class="sxs-lookup"><span data-stu-id="df6a2-123">**REMOVE_ON_NUKE**</span></span> <br/> |<span data-ttu-id="df6a2-124">Entfernt die Nachricht vom POP-Server, nur, nachdem der Benutzer die Nachricht aus dem Ordner Gelöschte Elemente löscht.</span><span class="sxs-lookup"><span data-stu-id="df6a2-124">Removes the message from the POP server only after the user deletes the message from the Deleted Items folder.</span></span>  <br/> |
|<span data-ttu-id="df6a2-125">**GET_REMOVE_AFTER_DAYS** ( _Ul_)</span><span class="sxs-lookup"><span data-stu-id="df6a2-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span></span>  <br/> |<span data-ttu-id="df6a2-126">Ruft die Anzahl der Tage nach denen die Nachricht vom POP-Server entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="df6a2-126">Gets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
|<span data-ttu-id="df6a2-127">**SET_REMOVE_AFTER_DAYS** ( _Tage_)</span><span class="sxs-lookup"><span data-stu-id="df6a2-127">**SET_REMOVE_AFTER_DAYS**( _days_)</span></span>  <br/> |<span data-ttu-id="df6a2-128">Legt die Anzahl der Tage nach denen die Nachricht vom POP-Server entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="df6a2-128">Sets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="df6a2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df6a2-129">See also</span></span>

- [<span data-ttu-id="df6a2-130">Verwalten von Nachricht downloads für POP3-Konten</span><span class="sxs-lookup"><span data-stu-id="df6a2-130">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="df6a2-131">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="df6a2-131">Constants (Account management API)</span></span>](constants-account-management-api.md)

