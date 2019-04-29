---
title: Informationen zur Frei/Gebucht-API
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: Die Frei/Gebucht-API ermöglicht es e-Mail-Anbietern, frei/gebucht-Statusinformationen für bestimmte Benutzerkonten innerhalb eines angegebenen Zeitintervalls bereitzustellen.
ms.openlocfilehash: 1bcd191b57238771ede6f035216fe3997e82e03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433759"
---
# <a name="about-the-freebusy-api"></a><span data-ttu-id="12b9a-103">Informationen zur Frei/Gebucht-API</span><span class="sxs-lookup"><span data-stu-id="12b9a-103">About the Free/Busy API</span></span>

<span data-ttu-id="12b9a-104">Die Frei/Gebucht-API ermöglicht es e-Mail-Anbietern, frei/gebucht-Statusinformationen für bestimmte Benutzerkonten innerhalb eines angegebenen Zeitintervalls bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="12b9a-104">The Free/Busy API allows mail providers to provide free/busy status information for specified user accounts within a specified time range.</span></span> <span data-ttu-id="12b9a-105">Der Frei/Gebucht-Status eines Zeitblocks im Kalender eines Benutzers ist einer der folgenden: Abwesenheit, beschäftigt, mit Vorbehalt oder kostenlos.</span><span class="sxs-lookup"><span data-stu-id="12b9a-105">The free/busy status of a block of time on a user's calendar is one of the following: out-of-office, busy, tentative, or free.</span></span>
  
## <a name="create-a-freebusy-provider"></a><span data-ttu-id="12b9a-106">Erstellen eines frei/gebucht-Anbieters</span><span class="sxs-lookup"><span data-stu-id="12b9a-106">Create a free/busy provider</span></span>

<span data-ttu-id="12b9a-107">Um e-Mail-Benutzern frei/Gebucht-Informationen bereitzustellen, erstellt ein e-Mail-Anbieter einen frei/gebucht-Anbieter und registriert ihn in Outlook.</span><span class="sxs-lookup"><span data-stu-id="12b9a-107">To provide free/busy information to mail users, a mail provider creates a free/busy provider and registers it with Outlook.</span></span> <span data-ttu-id="12b9a-108">Der frei/gebucht-Anbieter muss die folgenden Schnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="12b9a-108">The free/busy provider must implement the following interfaces.</span></span> <span data-ttu-id="12b9a-109">Beachten Sie, dass eine Reihe von Elementen in diesen Schnittstellen nicht unterstützt wird und die angegebenen Rückgabewerte zurückgegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="12b9a-109">Note that a number of members in these interfaces are not supported and must return the specified return values.</span></span> <span data-ttu-id="12b9a-110">Insbesondere unterstützt die Frei/Gebucht-API keinen Schreibzugriff auf Frei/Gebucht-Informationen und delegieren den Zugriff auf Konten.</span><span class="sxs-lookup"><span data-stu-id="12b9a-110">In particular, the Free/Busy API does not support write access to free/busy information and delegate access to accounts.</span></span>
  
- <span data-ttu-id="12b9a-111">[IFreeBusySupport](ifreebusysupport.md) : Diese Schnittstelle unterstützt die Spezifikation von Schnittstellen, die auf Frei/Gebucht-Daten für bestimmte Benutzer zugreifen.</span><span class="sxs-lookup"><span data-stu-id="12b9a-111">[IFreeBusySupport](ifreebusysupport.md) —This interface supports specification of interfaces that access free/busy data for specified users.</span></span> <span data-ttu-id="12b9a-112">Es verwendet [FBUser](fbuser.md) , um einen Benutzer zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="12b9a-112">It uses [FBUser](fbuser.md) to identify a user.</span></span> 
    
- <span data-ttu-id="12b9a-113">[IFreeBusyData](ifreebusydata.md) – diese Schnittstelle Ruft einen Zeitbereich für einen bestimmten Benutzer ab und legt ihn fest und gibt eine Schnittstelle zum Auflisten von Frei/Gebucht-Datenblöcken innerhalb dieses Zeitintervalls zurück.</span><span class="sxs-lookup"><span data-stu-id="12b9a-113">[IFreeBusyData](ifreebusydata.md) —This interface gets and sets a time range for a given user and returns an interface for enumerating free/busy blocks of data within this time range.</span></span> <span data-ttu-id="12b9a-114">Es verwendet relative Zeit zum Abrufen und Festlegen dieses Zeitintervalls.</span><span class="sxs-lookup"><span data-stu-id="12b9a-114">It uses relative time to get and set this time range.</span></span> <span data-ttu-id="12b9a-115">Weitere Informationen finden Sie unter [Verwenden von relativer Zeit für den Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md).</span><span class="sxs-lookup"><span data-stu-id="12b9a-115">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
- <span data-ttu-id="12b9a-116">[IEnumFBBlock](ienumfbblock.md) : Diese Schnittstelle unterstützt den Zugriff auf und das Aufzählen von Frei/Gebucht-Datenblöcken für einen Benutzer innerhalb eines Zeitintervalls.</span><span class="sxs-lookup"><span data-stu-id="12b9a-116">[IEnumFBBlock](ienumfbblock.md) —This interface supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="12b9a-117">Eine Aufzählung enthält frei/gebucht-Blöcke, die den Frei/Gebucht-Status von Zeiträumen im Kalender eines Benutzers innerhalb eines Zeitintervalls angeben (angegeben durch [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md)).</span><span class="sxs-lookup"><span data-stu-id="12b9a-117">An enumeration contains free/busy blocks that indicate the free/busy status of periods of time on a user's calendar, within a time range (specified by [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span></span> <span data-ttu-id="12b9a-118">Elemente in einem Kalender, wie Termine und Besprechungsanfragen, Formular Blöcke in der Aufzählung.</span><span class="sxs-lookup"><span data-stu-id="12b9a-118">Items on a calendar, such as appointments and meeting requests, form blocks in the enumeration.</span></span> <span data-ttu-id="12b9a-119">Elemente, die sich nebeneinander im Kalender befinden und den gleichen Frei/Gebucht-Status aufweisen, werden zu einem einzigen Block kombiniert.</span><span class="sxs-lookup"><span data-stu-id="12b9a-119">Items that are adjacent to one another on the calendar and have the same free/busy status are combined to form one single block.</span></span> <span data-ttu-id="12b9a-120">Ein freier Zeitraum in einem Kalender bildet auch einen Block.</span><span class="sxs-lookup"><span data-stu-id="12b9a-120">A free period of time on a calendar also forms a block.</span></span> <span data-ttu-id="12b9a-121">Daher hätten keine zwei aufeinanderfolgenden Blöcke in einer Enumeration denselben Frei/Gebucht-Status.</span><span class="sxs-lookup"><span data-stu-id="12b9a-121">Therefore, no two consecutive blocks in an enumeration would have the same free/busy status.</span></span> <span data-ttu-id="12b9a-122">Diese Blöcke überlappen sich nicht rechtzeitig.</span><span class="sxs-lookup"><span data-stu-id="12b9a-122">These blocks do not overlap in time.</span></span> <span data-ttu-id="12b9a-123">Wenn sich überlappende Elemente in einem Kalender befinden, werden diese Elemente von Outlook zusammengeführt, um sich nicht überschneidende frei/gebucht-Blöcke in der Enumeration zu bilden, die auf dieser Rangfolge basieren: Abwesenheit, gebucht, mit Vorbehalt.</span><span class="sxs-lookup"><span data-stu-id="12b9a-123">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span> 
  
<span data-ttu-id="12b9a-124">Zum Registrieren des frei/gebucht-Anbieters in Outlook sollte der e-Mail-Anbieter folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="12b9a-124">To register the free/busy provider with Outlook, the mail provider should do the following:</span></span>
  
1. <span data-ttu-id="12b9a-125">Registrieren des frei/gebucht-Anbieters mit COM, Bereitstelleneiner CLSID, die den Zugriff auf die Implementierung von **IFreeBusySupport**durch den Anbieter ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="12b9a-125">Register the free/busy provider with COM, providing a CLSID that allows access to the provider's implementation of **IFreeBusySupport**.</span></span> 
    
2. <span data-ttu-id="12b9a-126">Lassen Sie Outlook wissen, dass der frei/gebucht-Anbieter vorhanden ist, indem Sie `<xx.x>` den folgenden Schlüssel (wobei die Version von Outlook darstellt) in der Systemregistrierung festlegen:</span><span class="sxs-lookup"><span data-stu-id="12b9a-126">Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   <span data-ttu-id="12b9a-127">Wenn der Transportanbieter beispielsweise SMTP ist, um den Anbieter bei Microsoft Outlook 2010 zu registrieren, legen Sie den folgenden Schlüssel auf die Daten in der folgenden Tabelle fest:</span><span class="sxs-lookup"><span data-stu-id="12b9a-127">For example, if the transport provider is SMTP, to register the provider with Microsoft Outlook 2010, set the following key to the data in the following table:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |<span data-ttu-id="12b9a-128">Name</span><span class="sxs-lookup"><span data-stu-id="12b9a-128">Name</span></span> |<span data-ttu-id="12b9a-129">Typ</span><span class="sxs-lookup"><span data-stu-id="12b9a-129">Type</span></span> |<span data-ttu-id="12b9a-130">Wert</span><span class="sxs-lookup"><span data-stu-id="12b9a-130">Value</span></span> |
   |:-----|:-----|:-----|
   |<span data-ttu-id="12b9a-131">SMTP</span><span class="sxs-lookup"><span data-stu-id="12b9a-131">SMTP</span></span>  |<span data-ttu-id="12b9a-132">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="12b9a-132">REG_SZ</span></span>  |<span data-ttu-id="12b9a-133">{CLSID für die jeweilige Implementierung von IFreeBusySupport}</span><span class="sxs-lookup"><span data-stu-id="12b9a-133">{CLSID for respective implementation of IFreeBusySupport}</span></span>  |
   
   <span data-ttu-id="12b9a-134">In diesem Szenario erstellt Outlook die COM-Klasse und verwendet Sie zum Abrufen von Frei/Gebucht-Informationen für beliebige SMTP-e-Mail-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="12b9a-134">In this scenario, Outlook co-creates the COM class and uses it to retrieve free/busy information for any SMTP mail users.</span></span>
    
<span data-ttu-id="12b9a-135">Um ein Adressbuch und einen Transportanbieter zu unterstützen, die einen anderen Adresseintragstyp als SMTP verwenden, ändern Sie den *Namen* entsprechend.</span><span class="sxs-lookup"><span data-stu-id="12b9a-135">To support an address book and transport provider that use an address entry type other than SMTP, change the  *Name* accordingly.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="12b9a-136">Während der Installation sollten frei/gebucht-Anbieter überprüfen, ob eine Registrierungseinstellung für den gleichen Adresseintragstyp bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="12b9a-136">During installation, free/busy providers should check whether a registry setting for the the same address entry type already exists.</span></span> <span data-ttu-id="12b9a-137">Wenn dies der Fall ist, sollte der frei/gebucht-Anbieter den aktuellen Anbieter für diesen Adresseintragstyp überschreiben und bei Deinstallationen bei diesem Anbieter wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="12b9a-137">If it does, the free/busy provider should overwrite the current provider for that address entry type, and restore to that provider when it uninstalls.</span></span> <span data-ttu-id="12b9a-138">Wenn jedoch ein Benutzer mehr als einen frei/gebucht-Anbieter für denselben Adresseintragstyp installiert hat, sollte der Benutzer diese Anbieter in der umgekehrten Reihenfolge deinstallieren (also immer den aktuellen Anbieter deinstallieren).</span><span class="sxs-lookup"><span data-stu-id="12b9a-138">However, if a user has installed more than one free/busy provider for the same address entry type, the user should uninstall these providers in the reverse order as installation (that is, always uninstall the latest provider).</span></span> <span data-ttu-id="12b9a-139">Andernfalls kann die Registrierung auf einen Anbieter verweisen, der bereits deinstalliert wurde.</span><span class="sxs-lookup"><span data-stu-id="12b9a-139">Otherwise, the registry may point to a provider that has already been uninstalled.</span></span> 
  
## <a name="api-components"></a><span data-ttu-id="12b9a-140">API-Komponenten</span><span class="sxs-lookup"><span data-stu-id="12b9a-140">API components</span></span>

<span data-ttu-id="12b9a-141">Die Frei/Gebucht-API umfasst die folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="12b9a-141">The Free/Busy API includes the following components:</span></span>
  
### <a name="definitions"></a><span data-ttu-id="12b9a-142">Definitionen</span><span class="sxs-lookup"><span data-stu-id="12b9a-142">Definitions</span></span>

- [<span data-ttu-id="12b9a-143">Konstanten (frei/gebucht-API)</span><span class="sxs-lookup"><span data-stu-id="12b9a-143">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
    
### <a name="data-types"></a><span data-ttu-id="12b9a-144">Datentypen</span><span class="sxs-lookup"><span data-stu-id="12b9a-144">Data types</span></span>

- [<span data-ttu-id="12b9a-145">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="12b9a-145">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="12b9a-146">FBStatus</span><span class="sxs-lookup"><span data-stu-id="12b9a-146">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="12b9a-147">FBUser</span><span class="sxs-lookup"><span data-stu-id="12b9a-147">FBUser</span></span>](fbuser.md)
    
### <a name="interfaces"></a><span data-ttu-id="12b9a-148">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="12b9a-148">Interfaces</span></span>

- [<span data-ttu-id="12b9a-149">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="12b9a-149">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="12b9a-150">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="12b9a-150">IFreeBusyData</span></span>](ifreebusydata.md)
- [<span data-ttu-id="12b9a-151">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="12b9a-151">IFreeBusySupport</span></span>](ifreebusysupport.md)
    

