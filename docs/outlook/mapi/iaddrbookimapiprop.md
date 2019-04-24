---
title: IAddrBook IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook
api_type:
- COM
ms.assetid: 9ccacbc0-10d5-40f9-a12b-d090a21d0d49
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: da71e9dd5f2fc20bb1daf528f4466ea29507bf06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341377"
---
# <a name="iaddrbook--imapiprop"></a><span data-ttu-id="2a0f2-103">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2a0f2-103">IAddrBook : IMAPIProp</span></span>

  
  
<span data-ttu-id="2a0f2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a0f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a0f2-105">Unterstützt den Zugriff auf das MAPI-Adressbuch und enthält Vorgänge wie das Anzeigen allgemeiner Dialogfelder; Öffnen von Containern, Messaging Benutzern und Verteilerlisten; und durchführen der Namensauflösung.</span><span class="sxs-lookup"><span data-stu-id="2a0f2-105">Supports access to the MAPI address book and includes operations such as displaying common dialog boxes; opening containers, messaging users, and distribution lists; and performing name resolution.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2a0f2-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="2a0f2-106">Header file:</span></span>  <br/> |<span data-ttu-id="2a0f2-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="2a0f2-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="2a0f2-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="2a0f2-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="2a0f2-109">Adressbuch Objekte</span><span class="sxs-lookup"><span data-stu-id="2a0f2-109">Address book objects</span></span>  <br/> |
|<span data-ttu-id="2a0f2-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="2a0f2-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="2a0f2-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="2a0f2-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="2a0f2-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="2a0f2-112">Called by:</span></span>  <br/> |<span data-ttu-id="2a0f2-113">Client Anwendungen, Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="2a0f2-113">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="2a0f2-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="2a0f2-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2a0f2-115">IID_IAddrBook</span><span class="sxs-lookup"><span data-stu-id="2a0f2-115">IID_IAddrBook</span></span>  <br/> |
|<span data-ttu-id="2a0f2-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="2a0f2-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="2a0f2-117">LPADRBOOK</span><span class="sxs-lookup"><span data-stu-id="2a0f2-117">LPADRBOOK</span></span>  <br/> |
|<span data-ttu-id="2a0f2-118">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="2a0f2-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="2a0f2-119">Nicht schreibbar</span><span class="sxs-lookup"><span data-stu-id="2a0f2-119">Not writable</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2a0f2-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="2a0f2-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2a0f2-121">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="2a0f2-121">OpenEntry</span></span>](iaddrbook-openentry.md) <br/> |<span data-ttu-id="2a0f2-122">Öffnet einen Adressbucheintrag und gibt einen Zeiger auf eine Schnittstelle zurück, die für den Zugriff auf den Eintrag verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2a0f2-122">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>  <br/> |
|[<span data-ttu-id="2a0f2-123">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="2a0f2-123">CompareEntryIDs</span></span>](iaddrbook-compareentryids.md) <br/> |<span data-ttu-id="2a0f2-124">Vergleicht zwei Eintrags-IDs, die zu einem bestimmten Adressbuchanbieter gehören, um zu bestimmen, ob Sie auf dasselbe Adressbuchobjekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="2a0f2-124">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span>  <br/> |
|[<span data-ttu-id="2a0f2-125">Beraten</span><span class="sxs-lookup"><span data-stu-id="2a0f2-125">Advise</span></span>](iaddrbook-advise.md) <br/> |<span data-ttu-id="2a0f2-126">Registriert einen Client oder Dienstanbieter für den Empfang von Benachrichtigungen zu Änderungen an einem oder mehreren Einträgen im Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="2a0f2-126">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>  <br/> |
|[<span data-ttu-id="2a0f2-127">Unadvise</span><span class="sxs-lookup"><span data-stu-id="2a0f2-127">Unadvise</span></span>](iaddrbook-unadvise.md) <br/> |<span data-ttu-id="2a0f2-128">Bricht eine zuvor für einen Adressbucheintrag eingerichtete Benachrichtigungs Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="2a0f2-128">Cancels a notification registration previously established for an address book entry.</span></span>  <br/> |
|[<span data-ttu-id="2a0f2-129">CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="2a0f2-129">CreateOneOff</span></span>](iaddrbook-createoneoff.md) <br/> |<span data-ttu-id="2a0f2-130">Erstellt eine Eintrags-ID für eine einmalige Adresse.</span><span class="sxs-lookup"><span data-stu-id="2a0f2-130">Creates an entry identifier for a one-off address.</span></span>  <br/> |
|[<span data-ttu-id="2a0f2-131">NeuEintrag</span><span class="sxs-lookup"><span data-stu-id="2a0f2-131">NewEntry</span></span>](iaddrbook-newentry.md) <br/> |<span data-ttu-id="2a0f2-132">Fügt einen neuen Empfänger zu einem Adressbuchcontainer oder zur Empfängerliste einer ausgehenden Nachricht hinzu.</span><span class="sxs-lookup"><span data-stu-id="2a0f2-132">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="2a0f2-133">ResolveName</span><span class="sxs-lookup"><span data-stu-id="2a0f2-133">ResolveName</span></span>](iaddrbook-resolvename.md) <br/> |<span data-ttu-id="2a0f2-134">Führt eine Namensauflösung durch und weist Empfängern in einer Empfängerliste Eintragsbezeichner zu.</span><span class="sxs-lookup"><span data-stu-id="2a0f2-134">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>  <br/> |
|[<span data-ttu-id="2a0f2-135">Adresse</span><span class="sxs-lookup"><span data-stu-id="2a0f2-135">Address</span></span>](iaddrbook-address.md) <br/> |<span data-ttu-id="2a0f2-136">Zeigt das Dialogfeld Outlook-Adressbuch an.</span><span class="sxs-lookup"><span data-stu-id="2a0f2-136">Displays the Outlook address book dialog box.</span></span>  <br/> |
|[<span data-ttu-id="2a0f2-137">Details</span><span class="sxs-lookup"><span data-stu-id="2a0f2-137">Details</span></span>](iaddrbook-details.md) <br/> |<span data-ttu-id="2a0f2-138">Zeigt ein Dialogfeld an, in dem Details zu einem bestimmten Adressbucheintrag angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2a0f2-138">Displays a dialog box that shows details about a particular address book entry.</span></span>  <br/> |
|<span data-ttu-id="2a0f2-139">**RecipOptions**</span><span class="sxs-lookup"><span data-stu-id="2a0f2-139">**RecipOptions**</span></span> <br/> | <span data-ttu-id="2a0f2-140">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="2a0f2-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="2a0f2-141">**QueryDefaultRecipOpt**</span><span class="sxs-lookup"><span data-stu-id="2a0f2-141">**QueryDefaultRecipOpt**</span></span> <br/> | <span data-ttu-id="2a0f2-142">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="2a0f2-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="2a0f2-143">GetPAB</span><span class="sxs-lookup"><span data-stu-id="2a0f2-143">GetPAB</span></span>](iaddrbook-getpab.md) <br/> |<span data-ttu-id="2a0f2-144">Gibt den Eintragsbezeichner des Containers zurück, der als persönliches Adressbuch (PAB) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2a0f2-144">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="2a0f2-145">SetPAB</span><span class="sxs-lookup"><span data-stu-id="2a0f2-145">SetPAB</span></span>](iaddrbook-setpab.md) <br/> |<span data-ttu-id="2a0f2-146">Legt einen bestimmten Container als persönliches Adressbuch (PAB) fest.</span><span class="sxs-lookup"><span data-stu-id="2a0f2-146">Designates a particular container as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="2a0f2-147">GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="2a0f2-147">GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md) <br/> |<span data-ttu-id="2a0f2-148">Gibt die Eintrags-ID für den anfänglichen Adressbuchcontainer zurück.</span><span class="sxs-lookup"><span data-stu-id="2a0f2-148">Returns the entry identifier for the initial address book container.</span></span>  <br/> |
|[<span data-ttu-id="2a0f2-149">SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="2a0f2-149">SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md) <br/> |<span data-ttu-id="2a0f2-150">Legt den angegebenen Container als Standard-Adressbuchcontainer fest, der zunächst zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2a0f2-150">Establishes the specified container as the default address book container that is initially made available.</span></span>  <br/> |
|[<span data-ttu-id="2a0f2-151">GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="2a0f2-151">GetSearchPath</span></span>](iaddrbook-getsearchpath.md) <br/> |<span data-ttu-id="2a0f2-152">Gibt eine sortierte Liste von Eintrags Bezeichnern der Container zurück, die in den von der ResolveName-Methode initiierten namens Auflösungsprozess eingeschlossen werden sollen. [](iaddrbook-resolvename.md)</span><span class="sxs-lookup"><span data-stu-id="2a0f2-152">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [ResolveName](iaddrbook-resolvename.md) method.</span></span>  <br/> |
|[<span data-ttu-id="2a0f2-153">SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="2a0f2-153">SetSearchPath</span></span>](iaddrbook-setsearchpath.md) <br/> |<span data-ttu-id="2a0f2-154">Legt einen neuen Suchpfad im Profil fest, der für den Prozess der Namensauflösung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2a0f2-154">Sets a new search path in the profile that is used for the name resolution process.</span></span>  <br/> |
|[<span data-ttu-id="2a0f2-155">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="2a0f2-155">PrepareRecips</span></span>](iaddrbook-preparerecips.md) <br/> |<span data-ttu-id="2a0f2-156">Bereitet eine Empfängerliste für die spätere Verwendung durch das Messagingsystem vor.</span><span class="sxs-lookup"><span data-stu-id="2a0f2-156">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2a0f2-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a0f2-157">See also</span></span>



[<span data-ttu-id="2a0f2-158">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="2a0f2-158">MAPI Interfaces</span></span>](mapi-interfaces.md)

