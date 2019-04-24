---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Gibt an, dass eine Kopie einer Nachricht auf dem Server für ein POP-Konto hinterlassen werden soll.
ms.openlocfilehash: e1bbddea0f10c07d630676960d1b330f6055e137
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326488"
---
# <a name="proppopleaveonserver"></a><span data-ttu-id="f3610-103">PROP_POP_LEAVE_ON_SERVER</span><span class="sxs-lookup"><span data-stu-id="f3610-103">PROP_POP_LEAVE_ON_SERVER</span></span>

<span data-ttu-id="f3610-104">Gibt an, dass eine Kopie einer Nachricht auf dem Server für ein POP-Konto hinterlassen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3610-104">Specifies leaving a copy of a message on the server for a POP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f3610-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="f3610-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3610-106">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f3610-106">Identifier:</span></span>  <br/> |<span data-ttu-id="f3610-107">0x1000</span><span class="sxs-lookup"><span data-stu-id="f3610-107">0x1000</span></span>  <br/> |
|<span data-ttu-id="f3610-108">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="f3610-108">Property type:</span></span>  <br/> |<span data-ttu-id="f3610-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="f3610-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="f3610-110">Property-Tag:</span><span class="sxs-lookup"><span data-stu-id="f3610-110">Property tag:</span></span>  <br/> |<span data-ttu-id="f3610-111">0x10000003</span><span class="sxs-lookup"><span data-stu-id="f3610-111">0x10000003</span></span>  <br/> |
|<span data-ttu-id="f3610-112">Access</span><span class="sxs-lookup"><span data-stu-id="f3610-112">Access:</span></span>  <br/> |<span data-ttu-id="f3610-113">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3610-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3610-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3610-114">Remarks</span></span>

<span data-ttu-id="f3610-115">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f3610-115">The following table lists the possible values.</span></span> <span data-ttu-id="f3610-116">Weitere Informationen zu den Konstanten finden Sie unter [Constants (Account Management API)](constants-account-management-api.md) .</span><span class="sxs-lookup"><span data-stu-id="f3610-116">See [Constants (Account management API)](constants-account-management-api.md) for more information on the constants.</span></span> 
  
|<span data-ttu-id="f3610-117">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="f3610-117">**Possible values**</span></span>|<span data-ttu-id="f3610-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f3610-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3610-119">**LEAVE_ON_SERVER**</span><span class="sxs-lookup"><span data-stu-id="f3610-119">**LEAVE_ON_SERVER**</span></span> <br/> |<span data-ttu-id="f3610-120">HinTerlässt eine Kopie der Nachricht auf dem POP-Server nach dem Herunterladen der Nachricht auf ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="f3610-120">Leaves a copy of the message on the POP server after downloading the message to a device.</span></span>  <br/> |
|<span data-ttu-id="f3610-121">**REMOVE_AFTER**</span><span class="sxs-lookup"><span data-stu-id="f3610-121">**REMOVE_AFTER**</span></span> <br/> |<span data-ttu-id="f3610-122">Entfernt die Nachricht vom POP-Server, nachdem Sie Sie auf ein Gerät heruntergeladen hat.</span><span class="sxs-lookup"><span data-stu-id="f3610-122">Removes the message from the POP server after downloading it to a device.</span></span>  <br/> |
|<span data-ttu-id="f3610-123">**REMOVE_ON_NUKE**</span><span class="sxs-lookup"><span data-stu-id="f3610-123">**REMOVE_ON_NUKE**</span></span> <br/> |<span data-ttu-id="f3610-124">Entfernt die Nachricht erst vom POP-Server, nachdem der Benutzer die Nachricht aus dem Ordner Gelöschte Elemente gelöscht hat.</span><span class="sxs-lookup"><span data-stu-id="f3610-124">Removes the message from the POP server only after the user deletes the message from the Deleted Items folder.</span></span>  <br/> |
|<span data-ttu-id="f3610-125">**GET_REMOVE_AFTER_DAYS** ( _UL_)</span><span class="sxs-lookup"><span data-stu-id="f3610-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span></span>  <br/> |<span data-ttu-id="f3610-126">Ruft die Anzahl der Tage ab, nach denen die Nachricht vom POP-Server entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f3610-126">Gets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
|<span data-ttu-id="f3610-127">**SET_REMOVE_AFTER_DAYS** ( _Tage_)</span><span class="sxs-lookup"><span data-stu-id="f3610-127">**SET_REMOVE_AFTER_DAYS**( _days_)</span></span>  <br/> |<span data-ttu-id="f3610-128">Legt die Anzahl der Tage fest, nach denen die Nachricht vom POP-Server entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f3610-128">Sets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f3610-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3610-129">See also</span></span>

- [<span data-ttu-id="f3610-130">Verwalten des Nachrichtendownloads für POP3-Konten</span><span class="sxs-lookup"><span data-stu-id="f3610-130">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="f3610-131">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="f3610-131">Constants (Account management API)</span></span>](constants-account-management-api.md)

