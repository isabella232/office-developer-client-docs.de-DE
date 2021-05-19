---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Gibt an, dass eine Kopie einer Nachricht auf dem Server für ein POP-Konto gespeichert wird.
ms.openlocfilehash: e1bbddea0f10c07d630676960d1b330f6055e137
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410945"
---
# <a name="prop_pop_leave_on_server"></a><span data-ttu-id="322dc-103">PROP_POP_LEAVE_ON_SERVER</span><span class="sxs-lookup"><span data-stu-id="322dc-103">PROP_POP_LEAVE_ON_SERVER</span></span>

<span data-ttu-id="322dc-104">Gibt an, dass eine Kopie einer Nachricht auf dem Server für ein POP-Konto gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="322dc-104">Specifies leaving a copy of a message on the server for a POP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="322dc-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="322dc-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="322dc-106">Kennung:</span><span class="sxs-lookup"><span data-stu-id="322dc-106">Identifier:</span></span>  <br/> |<span data-ttu-id="322dc-107">0x1000</span><span class="sxs-lookup"><span data-stu-id="322dc-107">0x1000</span></span>  <br/> |
|<span data-ttu-id="322dc-108">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="322dc-108">Property type:</span></span>  <br/> |<span data-ttu-id="322dc-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="322dc-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="322dc-110">Eigenschaftstag:</span><span class="sxs-lookup"><span data-stu-id="322dc-110">Property tag:</span></span>  <br/> |<span data-ttu-id="322dc-111">0x10000003</span><span class="sxs-lookup"><span data-stu-id="322dc-111">0x10000003</span></span>  <br/> |
|<span data-ttu-id="322dc-112">Zugriff:</span><span class="sxs-lookup"><span data-stu-id="322dc-112">Access:</span></span>  <br/> |<span data-ttu-id="322dc-113">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="322dc-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="322dc-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="322dc-114">Remarks</span></span>

<span data-ttu-id="322dc-115">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="322dc-115">The following table lists the possible values.</span></span> <span data-ttu-id="322dc-116">Weitere Informationen zu den Konstanten finden Sie unter Konstanten [(Kontoverwaltungs-API).](constants-account-management-api.md)</span><span class="sxs-lookup"><span data-stu-id="322dc-116">See [Constants (Account management API)](constants-account-management-api.md) for more information on the constants.</span></span> 
  
|<span data-ttu-id="322dc-117">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="322dc-117">**Possible values**</span></span>|<span data-ttu-id="322dc-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="322dc-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="322dc-119">**LEAVE_ON_SERVER**</span><span class="sxs-lookup"><span data-stu-id="322dc-119">**LEAVE_ON_SERVER**</span></span> <br/> |<span data-ttu-id="322dc-120">Hinterlässt eine Kopie der Nachricht auf dem POP-Server, nachdem die Nachricht auf ein Gerät heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="322dc-120">Leaves a copy of the message on the POP server after downloading the message to a device.</span></span>  <br/> |
|<span data-ttu-id="322dc-121">**REMOVE_AFTER**</span><span class="sxs-lookup"><span data-stu-id="322dc-121">**REMOVE_AFTER**</span></span> <br/> |<span data-ttu-id="322dc-122">Entfernt die Nachricht vom POP-Server, nachdem sie auf ein Gerät heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="322dc-122">Removes the message from the POP server after downloading it to a device.</span></span>  <br/> |
|<span data-ttu-id="322dc-123">**REMOVE_ON_NUKE**</span><span class="sxs-lookup"><span data-stu-id="322dc-123">**REMOVE_ON_NUKE**</span></span> <br/> |<span data-ttu-id="322dc-124">Entfernt die Nachricht vom POP-Server erst, nachdem der Benutzer die Nachricht aus dem Ordner "Gelöschte Elemente" gelöscht hat.</span><span class="sxs-lookup"><span data-stu-id="322dc-124">Removes the message from the POP server only after the user deletes the message from the Deleted Items folder.</span></span>  <br/> |
|<span data-ttu-id="322dc-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span><span class="sxs-lookup"><span data-stu-id="322dc-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span></span>  <br/> |<span data-ttu-id="322dc-126">Ruft die Anzahl der Tage ab, nach denen die Nachricht vom POP-Server entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="322dc-126">Gets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
|<span data-ttu-id="322dc-127">**SET_REMOVE_AFTER_DAYS**( _Tage_)</span><span class="sxs-lookup"><span data-stu-id="322dc-127">**SET_REMOVE_AFTER_DAYS**( _days_)</span></span>  <br/> |<span data-ttu-id="322dc-128">Legt die Anzahl der Tage fest, nach denen die Nachricht vom POP-Server entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="322dc-128">Sets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="322dc-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="322dc-129">See also</span></span>

- [<span data-ttu-id="322dc-130">Verwalten des Nachrichtendownloads für POP3-Konten</span><span class="sxs-lookup"><span data-stu-id="322dc-130">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="322dc-131">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="322dc-131">Constants (Account management API)</span></span>](constants-account-management-api.md)

