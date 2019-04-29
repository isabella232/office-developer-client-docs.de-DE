---
title: IProfAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin
api_type:
- COM
ms.assetid: 274899cc-2894-4d99-84ec-f18121e856a0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cbdfba68490b1e756f277c6e552235368a86f310
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434116"
---
# <a name="iprofadmin--iunknown"></a><span data-ttu-id="9b600-103">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b600-103">IProfAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="9b600-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b600-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b600-105">Unterstützt die Verwaltung von Profilen.</span><span class="sxs-lookup"><span data-stu-id="9b600-105">Supports the administration of profiles.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b600-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9b600-106">Header file:</span></span>  <br/> |<span data-ttu-id="9b600-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="9b600-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="9b600-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="9b600-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="9b600-109">Profilverwaltungsobjekt</span><span class="sxs-lookup"><span data-stu-id="9b600-109">Profile administration object</span></span>  <br/> |
|<span data-ttu-id="9b600-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="9b600-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="9b600-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="9b600-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="9b600-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="9b600-112">Called by:</span></span>  <br/> |<span data-ttu-id="9b600-113">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="9b600-113">Client applications</span></span>  <br/> |
|<span data-ttu-id="9b600-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="9b600-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9b600-115">IID_IProfAdmin</span><span class="sxs-lookup"><span data-stu-id="9b600-115">IID_IProfAdmin</span></span>  <br/> |
|<span data-ttu-id="9b600-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="9b600-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="9b600-117">LPPROFADMIN</span><span class="sxs-lookup"><span data-stu-id="9b600-117">LPPROFADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9b600-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="9b600-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9b600-119">Getlasterroraufzurufen</span><span class="sxs-lookup"><span data-stu-id="9b600-119">GetLastError</span></span>](iprofadmin-getlasterror.md) <br/> |<span data-ttu-id="9b600-120">Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler enthält, der in einem Profilverwaltungsobjekt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="9b600-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span>  <br/> |
|[<span data-ttu-id="9b600-121">GetProfilable</span><span class="sxs-lookup"><span data-stu-id="9b600-121">GetProfileTable</span></span>](iprofadmin-getprofiletable.md) <br/> |<span data-ttu-id="9b600-122">Ermöglicht den Zugriff auf die Profiltabelle, eine Tabelle, die Informationen zu allen verfügbaren Profilen enthält.</span><span class="sxs-lookup"><span data-stu-id="9b600-122">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>  <br/> |
|[<span data-ttu-id="9b600-123">CreateProfile</span><span class="sxs-lookup"><span data-stu-id="9b600-123">CreateProfile</span></span>](iprofadmin-createprofile.md) <br/> |<span data-ttu-id="9b600-124">Erstellt ein neues Profil.</span><span class="sxs-lookup"><span data-stu-id="9b600-124">Creates a new profile.</span></span>  <br/> |
|[<span data-ttu-id="9b600-125">DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="9b600-125">DeleteProfile</span></span>](iprofadmin-deleteprofile.md) <br/> |<span data-ttu-id="9b600-126">Löscht ein Profil.</span><span class="sxs-lookup"><span data-stu-id="9b600-126">Deletes a profile.</span></span>  <br/> |
|[<span data-ttu-id="9b600-127">ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="9b600-127">ChangeProfilePassword</span></span>](iprofadmin-changeprofilepassword.md) <br/> |<span data-ttu-id="9b600-128">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="9b600-128">Deprecated.</span></span> <span data-ttu-id="9b600-129">Ändert das Kennwort für ein Profil.</span><span class="sxs-lookup"><span data-stu-id="9b600-129">Changes the password for a profile.</span></span>  <br/> |
|[<span data-ttu-id="9b600-130">CopyProfile</span><span class="sxs-lookup"><span data-stu-id="9b600-130">CopyProfile</span></span>](iprofadmin-copyprofile.md) <br/> |<span data-ttu-id="9b600-131">Kopiert ein Profil.</span><span class="sxs-lookup"><span data-stu-id="9b600-131">Copies a profile.</span></span>  <br/> |
|[<span data-ttu-id="9b600-132">RenameProfile</span><span class="sxs-lookup"><span data-stu-id="9b600-132">RenameProfile</span></span>](iprofadmin-renameprofile.md) <br/> |<span data-ttu-id="9b600-133">Weist einem Profil einen neuen Namen zu.</span><span class="sxs-lookup"><span data-stu-id="9b600-133">Assigns a new name to a profile.</span></span>  <br/> |
|[<span data-ttu-id="9b600-134">SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b600-134">SetDefaultProfile</span></span>](iprofadmin-setdefaultprofile.md) <br/> |<span data-ttu-id="9b600-135">Legt fest oder löscht das Standardprofil eines Clients.</span><span class="sxs-lookup"><span data-stu-id="9b600-135">Sets or clears a client's default profile.</span></span>  <br/> |
|[<span data-ttu-id="9b600-136">AdminServices</span><span class="sxs-lookup"><span data-stu-id="9b600-136">AdminServices</span></span>](iprofadmin-adminservices.md) <br/> |<span data-ttu-id="9b600-137">Ermöglicht den Zugriff auf ein Nachrichtendienst-Verwaltungsobjekt zum vornehmen von Änderungen an den Nachrichtendiensten in einem Profil.</span><span class="sxs-lookup"><span data-stu-id="9b600-137">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b600-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b600-138">See also</span></span>



[<span data-ttu-id="9b600-139">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9b600-139">MAPI Interfaces</span></span>](mapi-interfaces.md)

