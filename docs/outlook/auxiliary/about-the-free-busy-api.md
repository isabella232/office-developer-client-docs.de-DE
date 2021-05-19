---
title: Informationen zur Frei/Gebucht-API
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: Die Frei/Gebucht-API ermöglicht E-Mail-Anbietern, Frei/Gebucht-Statusinformationen für angegebene Benutzerkonten innerhalb eines angegebenen Zeitbereichs zur Verfügung zu stellen.
ms.openlocfilehash: 1bcd191b57238771ede6f035216fe3997e82e03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433759"
---
# <a name="about-the-freebusy-api"></a><span data-ttu-id="9d2cc-103">Informationen zur Frei/Gebucht-API</span><span class="sxs-lookup"><span data-stu-id="9d2cc-103">About the Free/Busy API</span></span>

<span data-ttu-id="9d2cc-104">Die Frei/Gebucht-API ermöglicht E-Mail-Anbietern, Frei/Gebucht-Statusinformationen für angegebene Benutzerkonten innerhalb eines angegebenen Zeitbereichs zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-104">The Free/Busy API allows mail providers to provide free/busy status information for specified user accounts within a specified time range.</span></span> <span data-ttu-id="9d2cc-105">Der Frei/Gebucht-Status eines Zeitblocks im Kalender eines Benutzers ist einer der folgenden: out-of-office, busy, tentative oder free.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-105">The free/busy status of a block of time on a user's calendar is one of the following: out-of-office, busy, tentative, or free.</span></span>
  
## <a name="create-a-freebusy-provider"></a><span data-ttu-id="9d2cc-106">Erstellen eines Frei/Gebucht-Anbieters</span><span class="sxs-lookup"><span data-stu-id="9d2cc-106">Create a free/busy provider</span></span>

<span data-ttu-id="9d2cc-107">Um E-Mail-Benutzern Frei/Gebucht-Informationen zur Verfügung zu stellen, erstellt ein E-Mail-Anbieter einen Frei/Gebucht-Anbieter und registriert Outlook.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-107">To provide free/busy information to mail users, a mail provider creates a free/busy provider and registers it with Outlook.</span></span> <span data-ttu-id="9d2cc-108">Der Frei/Gebucht-Anbieter muss die folgenden Schnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-108">The free/busy provider must implement the following interfaces.</span></span> <span data-ttu-id="9d2cc-109">Beachten Sie, dass eine Reihe von Mitgliedern in diesen Schnittstellen nicht unterstützt wird und die angegebenen Rückgabewerte zurückgeben müssen.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-109">Note that a number of members in these interfaces are not supported and must return the specified return values.</span></span> <span data-ttu-id="9d2cc-110">Insbesondere unterstützt die Frei/Gebucht-API keinen Schreibzugriff auf Frei/Gebucht-Informationen und delegiert den Zugriff auf Konten.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-110">In particular, the Free/Busy API does not support write access to free/busy information and delegate access to accounts.</span></span>
  
- <span data-ttu-id="9d2cc-111">[IFreeBusySupport](ifreebusysupport.md) – Diese Schnittstelle unterstützt die Spezifikation von Schnittstellen, die auf Frei/Gebucht-Daten für bestimmte Benutzer zugreifen.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-111">[IFreeBusySupport](ifreebusysupport.md) —This interface supports specification of interfaces that access free/busy data for specified users.</span></span> <span data-ttu-id="9d2cc-112">Es verwendet [FBUser,](fbuser.md) um einen Benutzer zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-112">It uses [FBUser](fbuser.md) to identify a user.</span></span> 
    
- <span data-ttu-id="9d2cc-113">[IFreeBusyData](ifreebusydata.md) – Diese Schnittstelle ruft einen Zeitraum für einen bestimmten Benutzer ab und legt diesen fest und gibt eine Schnittstelle zum Aufzählen von Frei/Gebucht-Datenblöcken innerhalb dieses Zeitbereichs zurück.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-113">[IFreeBusyData](ifreebusydata.md) —This interface gets and sets a time range for a given user and returns an interface for enumerating free/busy blocks of data within this time range.</span></span> <span data-ttu-id="9d2cc-114">Es verwendet relative Zeit, um diesen Zeitraum zu erhalten und zu legen.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-114">It uses relative time to get and set this time range.</span></span> <span data-ttu-id="9d2cc-115">Weitere Informationen finden Sie unter [Verwenden der relativen Zeit für den Zugriff auf Frei/Gebucht-Daten.](how-to-use-relative-time-to-access-free-busy-data.md)</span><span class="sxs-lookup"><span data-stu-id="9d2cc-115">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
- <span data-ttu-id="9d2cc-116">[IEnumFBBlock](ienumfbblock.md) – Diese Schnittstelle unterstützt den Zugriff auf und das Aufzählen von Frei/Gebucht-Datenblöcken für einen Benutzer innerhalb eines Zeitbereichs.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-116">[IEnumFBBlock](ienumfbblock.md) —This interface supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="9d2cc-117">Eine Enumeration enthält Frei/Gebucht-Blöcke, die den Frei/Gebucht-Status von Zeiträumen im Kalender eines Benutzers innerhalb eines Zeitbereichs angeben (angegeben durch [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span><span class="sxs-lookup"><span data-stu-id="9d2cc-117">An enumeration contains free/busy blocks that indicate the free/busy status of periods of time on a user's calendar, within a time range (specified by [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span></span> <span data-ttu-id="9d2cc-118">Elemente in einem Kalender, z. B. Termine und Besprechungsanfragen, Formularblöcke in der Enumeration.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-118">Items on a calendar, such as appointments and meeting requests, form blocks in the enumeration.</span></span> <span data-ttu-id="9d2cc-119">Elemente, die im Kalender nebeneinander liegen und den gleichen Frei/Gebucht-Status haben, werden zu einem einzelnen Block kombiniert.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-119">Items that are adjacent to one another on the calendar and have the same free/busy status are combined to form one single block.</span></span> <span data-ttu-id="9d2cc-120">Ein kostenloser Zeitraum in einem Kalender bildet auch einen Block.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-120">A free period of time on a calendar also forms a block.</span></span> <span data-ttu-id="9d2cc-121">Daher hätten keine zwei aufeinander folgenden Blöcke in einer Enumeration den gleichen Frei/Gebucht-Status.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-121">Therefore, no two consecutive blocks in an enumeration would have the same free/busy status.</span></span> <span data-ttu-id="9d2cc-122">Diese Blöcke überlappen sich nicht in der Zeit.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-122">These blocks do not overlap in time.</span></span> <span data-ttu-id="9d2cc-123">Wenn in einem Kalender überlappende Elemente enthalten sind, führt Outlook diese Elemente zu nicht überlappenden Frei/Gebucht-Blöcken in der Enumeration basierend auf dieser Rangfolge zusammen: out-of-office, busy, tentative.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-123">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span> 
  
<span data-ttu-id="9d2cc-124">Um den Frei/Gebucht-Anbieter bei Outlook registrieren zu können, sollte der E-Mail-Anbieter die folgenden Schritte tun:</span><span class="sxs-lookup"><span data-stu-id="9d2cc-124">To register the free/busy provider with Outlook, the mail provider should do the following:</span></span>
  
1. <span data-ttu-id="9d2cc-125">Registrieren Sie den Frei/Gebucht-Anbieter bei COM, indem Sie eine CLSID bereitstellen, die den Zugriff auf die Implementierung von **IFreeBusySupport durch den Anbieter ermöglicht.**</span><span class="sxs-lookup"><span data-stu-id="9d2cc-125">Register the free/busy provider with COM, providing a CLSID that allows access to the provider's implementation of **IFreeBusySupport**.</span></span> 
    
2. <span data-ttu-id="9d2cc-126">Teilen Outlook, dass der Frei/Gebucht-Anbieter vorhanden ist, indem Sie den folgenden Schlüssel (wobei die Version von Outlook) in der `<xx.x>` Systemregistrierung festlegen:</span><span class="sxs-lookup"><span data-stu-id="9d2cc-126">Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   <span data-ttu-id="9d2cc-127">Wenn der Transportanbieter beispielsweise SMTP ist, legen Sie den folgenden Schlüssel auf die Daten in der folgenden Tabelle, um den Anbieter bei Microsoft Outlook 2010 zu registrieren:</span><span class="sxs-lookup"><span data-stu-id="9d2cc-127">For example, if the transport provider is SMTP, to register the provider with Microsoft Outlook 2010, set the following key to the data in the following table:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |<span data-ttu-id="9d2cc-128">Name</span><span class="sxs-lookup"><span data-stu-id="9d2cc-128">Name</span></span> |<span data-ttu-id="9d2cc-129">Typ</span><span class="sxs-lookup"><span data-stu-id="9d2cc-129">Type</span></span> |<span data-ttu-id="9d2cc-130">Wert</span><span class="sxs-lookup"><span data-stu-id="9d2cc-130">Value</span></span> |
   |:-----|:-----|:-----|
   |<span data-ttu-id="9d2cc-131">SMTP</span><span class="sxs-lookup"><span data-stu-id="9d2cc-131">SMTP</span></span>  |<span data-ttu-id="9d2cc-132">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9d2cc-132">REG_SZ</span></span>  |<span data-ttu-id="9d2cc-133">{CLSID für die jeweilige Implementierung von IFreeBusySupport}</span><span class="sxs-lookup"><span data-stu-id="9d2cc-133">{CLSID for respective implementation of IFreeBusySupport}</span></span>  |
   
   <span data-ttu-id="9d2cc-134">In diesem Szenario erstellt Outlook die COM-Klasse und verwendet sie zum Abrufen von Frei/Gebucht-Informationen für smtp-E-Mail-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-134">In this scenario, Outlook co-creates the COM class and uses it to retrieve free/busy information for any SMTP mail users.</span></span>
    
<span data-ttu-id="9d2cc-135">Um ein Adressbuch und einen Transportanbieter zu unterstützen, die einen anderen Adresseintragstyp als SMTP verwenden, ändern Sie den  *Namen* entsprechend.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-135">To support an address book and transport provider that use an address entry type other than SMTP, change the  *Name* accordingly.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9d2cc-136">Während der Installation sollten Frei/Gebucht-Anbieter überprüfen, ob bereits eine Registrierungseinstellung für denselben Adresseintragstyp vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-136">During installation, free/busy providers should check whether a registry setting for the the same address entry type already exists.</span></span> <span data-ttu-id="9d2cc-137">In diesem Zustand sollte der Frei/Gebucht-Anbieter den aktuellen Anbieter für diesen Adresseintragstyp überschreiben und bei der Deinstallation in diesem Anbieter wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-137">If it does, the free/busy provider should overwrite the current provider for that address entry type, and restore to that provider when it uninstalls.</span></span> <span data-ttu-id="9d2cc-138">Wenn ein Benutzer jedoch mehrere Frei/Gebucht-Anbieter für denselben Adresseintragstyp installiert hat, sollte der Benutzer diese Anbieter in umgekehrter Reihenfolge als Installation deinstallieren (d. h. immer den neuesten Anbieter deinstallieren).</span><span class="sxs-lookup"><span data-stu-id="9d2cc-138">However, if a user has installed more than one free/busy provider for the same address entry type, the user should uninstall these providers in the reverse order as installation (that is, always uninstall the latest provider).</span></span> <span data-ttu-id="9d2cc-139">Andernfalls kann die Registrierung auf einen Anbieter verweisen, der bereits deinstalliert wurde.</span><span class="sxs-lookup"><span data-stu-id="9d2cc-139">Otherwise, the registry may point to a provider that has already been uninstalled.</span></span> 
  
## <a name="api-components"></a><span data-ttu-id="9d2cc-140">API-Komponenten</span><span class="sxs-lookup"><span data-stu-id="9d2cc-140">API components</span></span>

<span data-ttu-id="9d2cc-141">Die Frei/Gebucht-API umfasst die folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="9d2cc-141">The Free/Busy API includes the following components:</span></span>
  
### <a name="definitions"></a><span data-ttu-id="9d2cc-142">Definitionen</span><span class="sxs-lookup"><span data-stu-id="9d2cc-142">Definitions</span></span>

- [<span data-ttu-id="9d2cc-143">Konstanten (Frei/Gebucht-API)</span><span class="sxs-lookup"><span data-stu-id="9d2cc-143">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
    
### <a name="data-types"></a><span data-ttu-id="9d2cc-144">Datentypen</span><span class="sxs-lookup"><span data-stu-id="9d2cc-144">Data types</span></span>

- [<span data-ttu-id="9d2cc-145">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="9d2cc-145">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="9d2cc-146">FBStatus</span><span class="sxs-lookup"><span data-stu-id="9d2cc-146">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="9d2cc-147">FBUser</span><span class="sxs-lookup"><span data-stu-id="9d2cc-147">FBUser</span></span>](fbuser.md)
    
### <a name="interfaces"></a><span data-ttu-id="9d2cc-148">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9d2cc-148">Interfaces</span></span>

- [<span data-ttu-id="9d2cc-149">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="9d2cc-149">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="9d2cc-150">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="9d2cc-150">IFreeBusyData</span></span>](ifreebusydata.md)
- [<span data-ttu-id="9d2cc-151">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="9d2cc-151">IFreeBusySupport</span></span>](ifreebusysupport.md)
    

