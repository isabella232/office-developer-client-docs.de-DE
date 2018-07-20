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
ms.openlocfilehash: c6192e6f92078f2f9bab0d55e9952d21ebb82af6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792759"
---
# <a name="iprofadmin--iunknown"></a><span data-ttu-id="40c72-103">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="40c72-103">IProfAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="40c72-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="40c72-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="40c72-105">Unterstützt die Verwaltung von Benutzerprofilen.</span><span class="sxs-lookup"><span data-stu-id="40c72-105">Supports the administration of profiles.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40c72-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="40c72-106">Header file:</span></span>  <br/> |<span data-ttu-id="40c72-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="40c72-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="40c72-108">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="40c72-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="40c72-109">Profile Administration-Objekt</span><span class="sxs-lookup"><span data-stu-id="40c72-109">Profile administration object</span></span>  <br/> |
|<span data-ttu-id="40c72-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="40c72-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="40c72-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="40c72-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="40c72-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="40c72-112">Called by:</span></span>  <br/> |<span data-ttu-id="40c72-113">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="40c72-113">Client applications</span></span>  <br/> |
|<span data-ttu-id="40c72-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="40c72-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="40c72-115">IID_IProfAdmin</span><span class="sxs-lookup"><span data-stu-id="40c72-115">IID_IProfAdmin</span></span>  <br/> |
|<span data-ttu-id="40c72-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="40c72-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="40c72-117">LPPROFADMIN</span><span class="sxs-lookup"><span data-stu-id="40c72-117">LPPROFADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="40c72-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="40c72-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="40c72-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="40c72-119">GetLastError</span></span>](iprofadmin-getlasterror.md) <br/> |<span data-ttu-id="40c72-120">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler enthält, die auf ein Profil Administration-Objekt aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="40c72-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span>  <br/> |
|[<span data-ttu-id="40c72-121">"GetProfileTable"</span><span class="sxs-lookup"><span data-stu-id="40c72-121">GetProfileTable</span></span>](iprofadmin-getprofiletable.md) <br/> |<span data-ttu-id="40c72-122">Bietet Zugriff auf die Benutzerprofildienst-Tabelle eine Tabelle mit Informationen zu allen verfügbaren Profilen.</span><span class="sxs-lookup"><span data-stu-id="40c72-122">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>  <br/> |
|[<span data-ttu-id="40c72-123">CreateProfile</span><span class="sxs-lookup"><span data-stu-id="40c72-123">CreateProfile</span></span>](iprofadmin-createprofile.md) <br/> |<span data-ttu-id="40c72-124">Erstellt ein neues Profil.</span><span class="sxs-lookup"><span data-stu-id="40c72-124">Creates a new profile.</span></span>  <br/> |
|[<span data-ttu-id="40c72-125">DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="40c72-125">DeleteProfile</span></span>](iprofadmin-deleteprofile.md) <br/> |<span data-ttu-id="40c72-126">Löscht ein Profil.</span><span class="sxs-lookup"><span data-stu-id="40c72-126">Deletes a profile.</span></span>  <br/> |
|[<span data-ttu-id="40c72-127">ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="40c72-127">ChangeProfilePassword</span></span>](iprofadmin-changeprofilepassword.md) <br/> |<span data-ttu-id="40c72-128">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="40c72-128">Deprecated.</span></span> <span data-ttu-id="40c72-129">Ändert das Kennwort für ein Profil.</span><span class="sxs-lookup"><span data-stu-id="40c72-129">Changes the password for a profile.</span></span>  <br/> |
|[<span data-ttu-id="40c72-130">CopyProfile</span><span class="sxs-lookup"><span data-stu-id="40c72-130">CopyProfile</span></span>](iprofadmin-copyprofile.md) <br/> |<span data-ttu-id="40c72-131">Kopiert ein Profil.</span><span class="sxs-lookup"><span data-stu-id="40c72-131">Copies a profile.</span></span>  <br/> |
|[<span data-ttu-id="40c72-132">RenameProfile</span><span class="sxs-lookup"><span data-stu-id="40c72-132">RenameProfile</span></span>](iprofadmin-renameprofile.md) <br/> |<span data-ttu-id="40c72-133">Weist einen neuen Namen zu einem Profil.</span><span class="sxs-lookup"><span data-stu-id="40c72-133">Assigns a new name to a profile.</span></span>  <br/> |
|[<span data-ttu-id="40c72-134">SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c72-134">SetDefaultProfile</span></span>](iprofadmin-setdefaultprofile.md) <br/> |<span data-ttu-id="40c72-135">Aktiviert oder deaktiviert eine Client-Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="40c72-135">Sets or clears a client's default profile.</span></span>  <br/> |
|[<span data-ttu-id="40c72-136">AdminServices</span><span class="sxs-lookup"><span data-stu-id="40c72-136">AdminServices</span></span>](iprofadmin-adminservices.md) <br/> |<span data-ttu-id="40c72-137">Bietet Zugriff auf ein Objekt "Message" Service Administration für die Änderung der Nachrichtendienste in einem Profil.</span><span class="sxs-lookup"><span data-stu-id="40c72-137">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="40c72-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40c72-138">See also</span></span>



[<span data-ttu-id="40c72-139">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="40c72-139">MAPI Interfaces</span></span>](mapi-interfaces.md)

