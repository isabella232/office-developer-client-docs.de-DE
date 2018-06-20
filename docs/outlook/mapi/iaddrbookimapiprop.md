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
ms.openlocfilehash: 0e39f2603a1eef45c456b7fb58744b79c6b75f16
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792007"
---
# <a name="iaddrbook--imapiprop"></a><span data-ttu-id="2c923-103">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2c923-103">IAddrBook : IMAPIProp</span></span>

  
  
<span data-ttu-id="2c923-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2c923-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2c923-105">Unterstützt den Zugriff auf das MAPI-Adressbuch und enthält Vorgänge wie das allgemeine Dialogfelder anzeigen. Öffnen von Containern und messaging-Benutzer und Verteilerlisten; und namensauflösung ausführen.</span><span class="sxs-lookup"><span data-stu-id="2c923-105">Supports access to the MAPI address book and includes operations such as displaying common dialog boxes; opening containers, messaging users, and distribution lists; and performing name resolution.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2c923-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="2c923-106">Header file:</span></span>  <br/> |<span data-ttu-id="2c923-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="2c923-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="2c923-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="2c923-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="2c923-109">Address Book-Objekten</span><span class="sxs-lookup"><span data-stu-id="2c923-109">Address book objects</span></span>  <br/> |
|<span data-ttu-id="2c923-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="2c923-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="2c923-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="2c923-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="2c923-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="2c923-112">Called by:</span></span>  <br/> |<span data-ttu-id="2c923-113">Dienstanbieter-Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="2c923-113">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="2c923-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="2c923-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2c923-115">IID_IAddrBook</span><span class="sxs-lookup"><span data-stu-id="2c923-115">IID_IAddrBook</span></span>  <br/> |
|<span data-ttu-id="2c923-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="2c923-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="2c923-117">LPADRBOOK</span><span class="sxs-lookup"><span data-stu-id="2c923-117">LPADRBOOK</span></span>  <br/> |
|<span data-ttu-id="2c923-118">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="2c923-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="2c923-119">Nicht geschrieben</span><span class="sxs-lookup"><span data-stu-id="2c923-119">Not writable</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2c923-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="2c923-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2c923-121">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="2c923-121">OpenEntry</span></span>](iaddrbook-openentry.md) <br/> |<span data-ttu-id="2c923-122">Öffnet ein Adressbuch Adresseintrag, und gibt einen Zeiger auf eine Schnittstelle, die den Eintrag Zugriff auf verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2c923-122">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>  <br/> |
|[<span data-ttu-id="2c923-123">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="2c923-123">CompareEntryIDs</span></span>](iaddrbook-compareentryids.md) <br/> |<span data-ttu-id="2c923-124">Vergleicht zwei Eintragsbezeichner, die gehören zu einer bestimmten Adressbuchanbieter um festzustellen, ob diese auf das gleiche Address Book-Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="2c923-124">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span>  <br/> |
|[<span data-ttu-id="2c923-125">Beraten</span><span class="sxs-lookup"><span data-stu-id="2c923-125">Advise</span></span>](iaddrbook-advise.md) <br/> |<span data-ttu-id="2c923-126">Registriert einen Client oder Dienstanbieter Erhalt von Benachrichtigungen zu Änderungen an einen oder mehrere Einträge im Adressbuch an.</span><span class="sxs-lookup"><span data-stu-id="2c923-126">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>  <br/> |
|[<span data-ttu-id="2c923-127">Heben Sie diesen Vorgang</span><span class="sxs-lookup"><span data-stu-id="2c923-127">Unadvise</span></span>](iaddrbook-unadvise.md) <br/> |<span data-ttu-id="2c923-128">Benachrichtigungsregistrierung eines für einen Adresseintrag Adressbuch zuvor eingerichtet werden abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="2c923-128">Cancels a notification registration previously established for an address book entry.</span></span>  <br/> |
|[<span data-ttu-id="2c923-129">CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="2c923-129">CreateOneOff</span></span>](iaddrbook-createoneoff.md) <br/> |<span data-ttu-id="2c923-130">Erstellt einen Eintrag Bezeichner für eine einmalige Adresse.</span><span class="sxs-lookup"><span data-stu-id="2c923-130">Creates an entry identifier for a one-off address.</span></span>  <br/> |
|[<span data-ttu-id="2c923-131">NewEntry</span><span class="sxs-lookup"><span data-stu-id="2c923-131">NewEntry</span></span>](iaddrbook-newentry.md) <br/> |<span data-ttu-id="2c923-132">Fügt einen neuen Empfänger um eine Adressbuchcontainer oder die Empfängerliste von ausgehenden Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="2c923-132">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="2c923-133">ResolveName</span><span class="sxs-lookup"><span data-stu-id="2c923-133">ResolveName</span></span>](iaddrbook-resolvename.md) <br/> |<span data-ttu-id="2c923-134">Führt Namensresolution Eintragsbezeichner an Empfänger in der Empfängerliste zuweisen.</span><span class="sxs-lookup"><span data-stu-id="2c923-134">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>  <br/> |
|[<span data-ttu-id="2c923-135">Address</span><span class="sxs-lookup"><span data-stu-id="2c923-135">Address</span></span>](iaddrbook-address.md) <br/> |<span data-ttu-id="2c923-136">Zeigt das Dialogfeld Adressbuch von Outlook-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="2c923-136">Displays the Outlook address book dialog box.</span></span>  <br/> |
|[<span data-ttu-id="2c923-137">Details</span><span class="sxs-lookup"><span data-stu-id="2c923-137">Details</span></span>](iaddrbook-details.md) <br/> |<span data-ttu-id="2c923-138">Zeigt ein Dialogfeld, das Details zu einem bestimmten Buch Adresseintrag anzeigt.</span><span class="sxs-lookup"><span data-stu-id="2c923-138">Displays a dialog box that shows details about a particular address book entry.</span></span>  <br/> |
|<span data-ttu-id="2c923-139">**RecipOptions**</span><span class="sxs-lookup"><span data-stu-id="2c923-139">**RecipOptions**</span></span> <br/> | <span data-ttu-id="2c923-140">*Nicht unterstützte oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="2c923-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="2c923-141">**QueryDefaultRecipOpt**</span><span class="sxs-lookup"><span data-stu-id="2c923-141">**QueryDefaultRecipOpt**</span></span> <br/> | <span data-ttu-id="2c923-142">*Nicht unterstützte oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="2c923-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="2c923-143">GetPAB</span><span class="sxs-lookup"><span data-stu-id="2c923-143">GetPAB</span></span>](iaddrbook-getpab.md) <br/> |<span data-ttu-id="2c923-144">Gibt die Eintrags-ID des Containers, die als das persönliche Adressbuch (PAB) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2c923-144">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="2c923-145">SetPAB</span><span class="sxs-lookup"><span data-stu-id="2c923-145">SetPAB</span></span>](iaddrbook-setpab.md) <br/> |<span data-ttu-id="2c923-146">Legt einen bestimmten Container als das persönliche Adressbuch (PAB) fest.</span><span class="sxs-lookup"><span data-stu-id="2c923-146">Designates a particular container as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="2c923-147">GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="2c923-147">GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md) <br/> |<span data-ttu-id="2c923-148">Gibt die Eintrags-ID für die anfängliche Adressbuchcontainer zurück.</span><span class="sxs-lookup"><span data-stu-id="2c923-148">Returns the entry identifier for the initial address book container.</span></span>  <br/> |
|[<span data-ttu-id="2c923-149">SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="2c923-149">SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md) <br/> |<span data-ttu-id="2c923-150">Richtet den angegebenen Container als Standard-Adressbuchcontainer, die Anfangs verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="2c923-150">Establishes the specified container as the default address book container that is initially made available.</span></span>  <br/> |
|[<span data-ttu-id="2c923-151">GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="2c923-151">GetSearchPath</span></span>](iaddrbook-getsearchpath.md) <br/> |<span data-ttu-id="2c923-152">Gibt eine geordnete Liste von Eintrags-IDs der Container in der [ResolveName](iaddrbook-resolvename.md) -Methode initiiert Vorgang der Lösung enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="2c923-152">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [ResolveName](iaddrbook-resolvename.md) method.</span></span>  <br/> |
|[<span data-ttu-id="2c923-153">SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="2c923-153">SetSearchPath</span></span>](iaddrbook-setsearchpath.md) <br/> |<span data-ttu-id="2c923-154">Legt einen neuen Pfad für die Suche in das Profil, das für den Vorgang der Lösung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2c923-154">Sets a new search path in the profile that is used for the name resolution process.</span></span>  <br/> |
|[<span data-ttu-id="2c923-155">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="2c923-155">PrepareRecips</span></span>](iaddrbook-preparerecips.md) <br/> |<span data-ttu-id="2c923-156">Bereitet eine Empfängerliste zur späteren Verwendung von messaging-System.</span><span class="sxs-lookup"><span data-stu-id="2c923-156">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2c923-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c923-157">See also</span></span>



[<span data-ttu-id="2c923-158">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="2c923-158">MAPI Interfaces</span></span>](mapi-interfaces.md)

