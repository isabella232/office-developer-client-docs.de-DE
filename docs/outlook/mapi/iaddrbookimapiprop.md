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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: da71e9dd5f2fc20bb1daf528f4466ea29507bf06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429824"
---
# <a name="iaddrbook--imapiprop"></a><span data-ttu-id="0ff98-103">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0ff98-103">IAddrBook : IMAPIProp</span></span>

  
  
<span data-ttu-id="0ff98-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ff98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ff98-105">Unterstützt den Zugriff auf das #A0 und umfasst Vorgänge wie das Anzeigen gängiger Dialogfelder. Öffnen von Containern, Messagingbenutzern und Verteilerlisten; und Durchführen der Namensauflösung.</span><span class="sxs-lookup"><span data-stu-id="0ff98-105">Supports access to the MAPI address book and includes operations such as displaying common dialog boxes; opening containers, messaging users, and distribution lists; and performing name resolution.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0ff98-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0ff98-106">Header file:</span></span>  <br/> |<span data-ttu-id="0ff98-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="0ff98-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="0ff98-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="0ff98-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="0ff98-109">Adressbuchobjekte</span><span class="sxs-lookup"><span data-stu-id="0ff98-109">Address book objects</span></span>  <br/> |
|<span data-ttu-id="0ff98-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="0ff98-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="0ff98-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="0ff98-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="0ff98-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="0ff98-112">Called by:</span></span>  <br/> |<span data-ttu-id="0ff98-113">Clientanwendungen, Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="0ff98-113">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="0ff98-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="0ff98-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0ff98-115">IID_IAddrBook</span><span class="sxs-lookup"><span data-stu-id="0ff98-115">IID_IAddrBook</span></span>  <br/> |
|<span data-ttu-id="0ff98-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="0ff98-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="0ff98-117">LPADRBOOK</span><span class="sxs-lookup"><span data-stu-id="0ff98-117">LPADRBOOK</span></span>  <br/> |
|<span data-ttu-id="0ff98-118">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="0ff98-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="0ff98-119">Nicht beschreibbar</span><span class="sxs-lookup"><span data-stu-id="0ff98-119">Not writable</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0ff98-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="0ff98-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0ff98-121">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="0ff98-121">OpenEntry</span></span>](iaddrbook-openentry.md) <br/> |<span data-ttu-id="0ff98-122">Öffnet einen Adressbucheintrag und gibt einen Zeiger auf eine Schnittstelle zurück, die für den Zugriff auf den Eintrag verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0ff98-122">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>  <br/> |
|[<span data-ttu-id="0ff98-123">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="0ff98-123">CompareEntryIDs</span></span>](iaddrbook-compareentryids.md) <br/> |<span data-ttu-id="0ff98-124">Vergleicht zwei Eintragsbezeichner, die zu einem bestimmten Adressbuchanbieter gehören, um zu bestimmen, ob sie auf dasselbe Adressbuchobjekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="0ff98-124">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span>  <br/> |
|[<span data-ttu-id="0ff98-125">Raten</span><span class="sxs-lookup"><span data-stu-id="0ff98-125">Advise</span></span>](iaddrbook-advise.md) <br/> |<span data-ttu-id="0ff98-126">Registriert einen Client oder Dienstanbieter, um Benachrichtigungen über Änderungen an einem oder mehreren Einträgen im Adressbuch zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ff98-126">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>  <br/> |
|[<span data-ttu-id="0ff98-127">Unadvise</span><span class="sxs-lookup"><span data-stu-id="0ff98-127">Unadvise</span></span>](iaddrbook-unadvise.md) <br/> |<span data-ttu-id="0ff98-128">Bricht eine Benachrichtigungsregistrierung ab, die zuvor für einen Adressbucheintrag eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="0ff98-128">Cancels a notification registration previously established for an address book entry.</span></span>  <br/> |
|[<span data-ttu-id="0ff98-129">CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="0ff98-129">CreateOneOff</span></span>](iaddrbook-createoneoff.md) <br/> |<span data-ttu-id="0ff98-130">Erstellt einen Eintragsbezeichner für eine eindeutige Adresse.</span><span class="sxs-lookup"><span data-stu-id="0ff98-130">Creates an entry identifier for a one-off address.</span></span>  <br/> |
|[<span data-ttu-id="0ff98-131">NewEntry</span><span class="sxs-lookup"><span data-stu-id="0ff98-131">NewEntry</span></span>](iaddrbook-newentry.md) <br/> |<span data-ttu-id="0ff98-132">Fügt einem Adressbuchcontainer oder der Empfängerliste einer ausgehenden Nachricht einen neuen Empfänger hinzu.</span><span class="sxs-lookup"><span data-stu-id="0ff98-132">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="0ff98-133">ResolveName</span><span class="sxs-lookup"><span data-stu-id="0ff98-133">ResolveName</span></span>](iaddrbook-resolvename.md) <br/> |<span data-ttu-id="0ff98-134">Führt die Namensauflösung durch und weist Empfängern in einer Empfängerliste Eintragsbezeichner zu.</span><span class="sxs-lookup"><span data-stu-id="0ff98-134">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>  <br/> |
|[<span data-ttu-id="0ff98-135">Adresse</span><span class="sxs-lookup"><span data-stu-id="0ff98-135">Address</span></span>](iaddrbook-address.md) <br/> |<span data-ttu-id="0ff98-136">Zeigt das Outlook Adressbuch an.</span><span class="sxs-lookup"><span data-stu-id="0ff98-136">Displays the Outlook address book dialog box.</span></span>  <br/> |
|[<span data-ttu-id="0ff98-137">Details</span><span class="sxs-lookup"><span data-stu-id="0ff98-137">Details</span></span>](iaddrbook-details.md) <br/> |<span data-ttu-id="0ff98-138">Zeigt ein Dialogfeld an, in dem Details zu einem bestimmten Adressbucheintrag angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0ff98-138">Displays a dialog box that shows details about a particular address book entry.</span></span>  <br/> |
|<span data-ttu-id="0ff98-139">**RecipOptions**</span><span class="sxs-lookup"><span data-stu-id="0ff98-139">**RecipOptions**</span></span> <br/> | <span data-ttu-id="0ff98-140">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="0ff98-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="0ff98-141">**QueryDefaultRecipOpt**</span><span class="sxs-lookup"><span data-stu-id="0ff98-141">**QueryDefaultRecipOpt**</span></span> <br/> | <span data-ttu-id="0ff98-142">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="0ff98-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="0ff98-143">GetPAB</span><span class="sxs-lookup"><span data-stu-id="0ff98-143">GetPAB</span></span>](iaddrbook-getpab.md) <br/> |<span data-ttu-id="0ff98-144">Gibt den Eintragsbezeichner des Containers zurück, der als persönliches Adressbuch (PAB) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0ff98-144">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="0ff98-145">SetPAB</span><span class="sxs-lookup"><span data-stu-id="0ff98-145">SetPAB</span></span>](iaddrbook-setpab.md) <br/> |<span data-ttu-id="0ff98-146">Bestimmt einen bestimmten Container als persönliches Adressbuch (PAB).</span><span class="sxs-lookup"><span data-stu-id="0ff98-146">Designates a particular container as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="0ff98-147">GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="0ff98-147">GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md) <br/> |<span data-ttu-id="0ff98-148">Gibt den Eintragsbezeichner für den anfänglichen Adressbuchcontainer zurück.</span><span class="sxs-lookup"><span data-stu-id="0ff98-148">Returns the entry identifier for the initial address book container.</span></span>  <br/> |
|[<span data-ttu-id="0ff98-149">SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="0ff98-149">SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md) <br/> |<span data-ttu-id="0ff98-150">Richtet den angegebenen Container als Standard-Adressbuchcontainer ein, der zunächst verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="0ff98-150">Establishes the specified container as the default address book container that is initially made available.</span></span>  <br/> |
|[<span data-ttu-id="0ff98-151">GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="0ff98-151">GetSearchPath</span></span>](iaddrbook-getsearchpath.md) <br/> |<span data-ttu-id="0ff98-152">Gibt eine geordnete Liste der Eintragsbezeichner der Container zurück, die in den von der [ResolveName-Methode](iaddrbook-resolvename.md) initiierten Namensauflösungsprozess einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0ff98-152">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [ResolveName](iaddrbook-resolvename.md) method.</span></span>  <br/> |
|[<span data-ttu-id="0ff98-153">SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="0ff98-153">SetSearchPath</span></span>](iaddrbook-setsearchpath.md) <br/> |<span data-ttu-id="0ff98-154">Legt einen neuen Suchpfad im Profil fest, der für den Namensauflösungsprozess verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0ff98-154">Sets a new search path in the profile that is used for the name resolution process.</span></span>  <br/> |
|[<span data-ttu-id="0ff98-155">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="0ff98-155">PrepareRecips</span></span>](iaddrbook-preparerecips.md) <br/> |<span data-ttu-id="0ff98-156">Bereitet eine Empfängerliste für die spätere Verwendung durch das Messagingsystem vor.</span><span class="sxs-lookup"><span data-stu-id="0ff98-156">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0ff98-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ff98-157">See also</span></span>



[<span data-ttu-id="0ff98-158">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0ff98-158">MAPI Interfaces</span></span>](mapi-interfaces.md)

