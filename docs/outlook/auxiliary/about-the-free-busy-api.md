---
title: Informationen zur Frei/Gebucht-API
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: Die Frei/Gebucht-API ermöglicht es e-Mail-Anbieter für Frei-/Gebucht-Status Informationen für den angegebenen Benutzerkonten innerhalb eines angegebenen Zeitraums.
ms.openlocfilehash: 8b1559173297fbde9930b6f8f7fbc74f176273da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790923"
---
# <a name="about-the-freebusy-api"></a><span data-ttu-id="5ee04-103">Informationen zur Frei/Gebucht-API</span><span class="sxs-lookup"><span data-stu-id="5ee04-103">About the Free/Busy API</span></span>

<span data-ttu-id="5ee04-104">Die Frei/Gebucht-API ermöglicht es e-Mail-Anbieter für Frei-/Gebucht-Status Informationen für den angegebenen Benutzerkonten innerhalb eines angegebenen Zeitraums.</span><span class="sxs-lookup"><span data-stu-id="5ee04-104">The Free/Busy API allows mail providers to provide free/busy status information for specified user accounts within a specified time range.</span></span> <span data-ttu-id="5ee04-105">Der Frei/Gebucht-Status eines Textblocks Kalender des Benutzers ist einer der folgenden: Abwesenheits, gebucht, mit Vorbehalt oder frei.</span><span class="sxs-lookup"><span data-stu-id="5ee04-105">The free/busy status of a block of time on a user's calendar is one of the following: out-of-office, busy, tentative, or free.</span></span>
  
## <a name="create-a-freebusy-provider"></a><span data-ttu-id="5ee04-106">Erstellen eines Anbieters für Frei/Gebucht-Informationen</span><span class="sxs-lookup"><span data-stu-id="5ee04-106">Create a free/busy provider</span></span>

<span data-ttu-id="5ee04-107">Um Frei/Gebucht-Informationen an e-Mail-Benutzer zu ermöglichen, ein e-Mail-Anbieter einen Anbieter für Frei/Gebucht-Informationen erstellt und registriert sie bei Outlook.</span><span class="sxs-lookup"><span data-stu-id="5ee04-107">To provide free/busy information to mail users, a mail provider creates a free/busy provider and registers it with Outlook.</span></span> <span data-ttu-id="5ee04-108">Der Frei/Gebucht-Anbieter muss die folgenden Schnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="5ee04-108">The free/busy provider must implement the following interfaces.</span></span> <span data-ttu-id="5ee04-109">Beachten Sie, dass eine Anzahl von Elementen in diese Schnittstellen nicht unterstützt werden und muss zurückgeben, dass die angegebenen Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5ee04-109">Note that a number of members in these interfaces are not supported and must return the specified return values.</span></span> <span data-ttu-id="5ee04-110">Insbesondere unterstützt die Frei/Gebucht-API nicht Schreibzugriff, um Frei/Gebucht-Informationen und Delegieren des Zugriffs auf Konten.</span><span class="sxs-lookup"><span data-stu-id="5ee04-110">In particular, the Free/Busy API does not support write access to free/busy information and delegate access to accounts.</span></span>
  
- <span data-ttu-id="5ee04-111">[IFreeBusySupport](ifreebusysupport.md) – diese Schnittstelle unterstützt die Angabe der Schnittstellen, die Frei/Gebucht-Daten für bestimmte Benutzer zugreifen.</span><span class="sxs-lookup"><span data-stu-id="5ee04-111">[IFreeBusySupport](ifreebusysupport.md) —This interface supports specification of interfaces that access free/busy data for specified users.</span></span> <span data-ttu-id="5ee04-112">[FBUser](fbuser.md) verwendet, um einen Benutzer zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5ee04-112">It uses [FBUser](fbuser.md) to identify a user.</span></span> 
    
- <span data-ttu-id="5ee04-113">[IFreeBusyData](ifreebusydata.md) – diese Schnittstelle ruft ab und legt einen Zeitraum für einen bestimmten Benutzer fest und gibt eine Schnittstelle zum Aufzählen Datenblöcke Frei/Gebucht-Informationen in diesem Zeitraum zurück.</span><span class="sxs-lookup"><span data-stu-id="5ee04-113">[IFreeBusyData](ifreebusydata.md) —This interface gets and sets a time range for a given user and returns an interface for enumerating free/busy blocks of data within this time range.</span></span> <span data-ttu-id="5ee04-114">Relative Zeit verwendet zum Abrufen und Festlegen der Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="5ee04-114">It uses relative time to get and set this time range.</span></span> <span data-ttu-id="5ee04-115">Weitere Informationen finden Sie unter [Verwendung relative Zeit auf Frei/Gebucht-Daten zugreifen](how-to-use-relative-time-to-access-free-busy-data.md).</span><span class="sxs-lookup"><span data-stu-id="5ee04-115">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
- <span data-ttu-id="5ee04-116">[IEnumFBBlock](ienumfbblock.md) – diese Schnittstelle unterstützt den Zugriff auf und auflisten Datenblöcke Frei/Gebucht-Informationen für einen Benutzer innerhalb eines Zeitraums.</span><span class="sxs-lookup"><span data-stu-id="5ee04-116">[IEnumFBBlock](ienumfbblock.md) —This interface supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="5ee04-117">Eine Enumeration enthält Frei/Gebucht-Blöcke, die den Frei/Gebucht-Status von Zeiträume Kalender des Benutzers, innerhalb eines Zeitraums (angegeben durch [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)) angeben.</span><span class="sxs-lookup"><span data-stu-id="5ee04-117">An enumeration contains free/busy blocks that indicate the free/busy status of periods of time on a user's calendar, within a time range (specified by [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span></span> <span data-ttu-id="5ee04-118">Elemente in einem Kalender, wie Termine und Besprechungsanfragen, bilden Blöcke in der-Aufzählung.</span><span class="sxs-lookup"><span data-stu-id="5ee04-118">Items on a calendar, such as appointments and meeting requests, form blocks in the enumeration.</span></span> <span data-ttu-id="5ee04-119">Elemente, die im Kalender nebeneinander und haben den gleichen Frei/Gebucht-Status werden auf einem einzelnen Block Formular kombiniert.</span><span class="sxs-lookup"><span data-stu-id="5ee04-119">Items that are adjacent to one another on the calendar and have the same free/busy status are combined to form one single block.</span></span> <span data-ttu-id="5ee04-120">Ein freier Zeitraum in einem Kalender bildet auch einen Block.</span><span class="sxs-lookup"><span data-stu-id="5ee04-120">A free period of time on a calendar also forms a block.</span></span> <span data-ttu-id="5ee04-121">Keine zwei aufeinander folgenden Blöcke in einer Enumeration müssen daher den gleichen Frei/Gebucht-Status.</span><span class="sxs-lookup"><span data-stu-id="5ee04-121">Therefore, no two consecutive blocks in an enumeration would have the same free/busy status.</span></span> <span data-ttu-id="5ee04-122">Diese Blöcke überlappen nicht rechtzeitig.</span><span class="sxs-lookup"><span data-stu-id="5ee04-122">These blocks do not overlap in time.</span></span> <span data-ttu-id="5ee04-123">Wenn sich überschneidenden Elemente in einem Kalender sind, verbindet Outlook diese Elemente um Frei/Gebucht-Blöcke übereinander in der angegebenen Reihenfolge der Priorität-Enumeration bilden: Abwesenheits, gebucht, mit Vorbehalt.</span><span class="sxs-lookup"><span data-stu-id="5ee04-123">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span> 
  
<span data-ttu-id="5ee04-124">Zum Registrieren des Anbieters Frei/Gebucht-Informationen mit Outlook, sollte der e-Mail-Anbieter Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="5ee04-124">To register the free/busy provider with Outlook, the mail provider should do the following:</span></span>
  
1. <span data-ttu-id="5ee04-125">Registrieren des Anbieters Frei/Gebucht-Informationen mit COM, bietet eine CLSID, die Zugriff auf den Anbieter Implementierung **IFreeBusySupport**ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="5ee04-125">Register the free/busy provider with COM, providing a CLSID that allows access to the provider's implementation of **IFreeBusySupport**.</span></span> 
    
2. <span data-ttu-id="5ee04-126">Lassen Sie Outlook wissen, dass der Anbieter Frei/Gebucht-Informationen vorhanden ist, indem Sie den folgenden Schlüssel festlegen (wobei `<xx.x>` steht für die Version von Outlook) in der Registrierung:</span><span class="sxs-lookup"><span data-stu-id="5ee04-126">Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   <span data-ttu-id="5ee04-127">Beispielsweise ist der Adressbuchhierarchie SMTP, zum Registrieren des Anbieters mit Microsoft Outlook 2010, legen Sie den folgenden Schlüssel mit den Daten in der folgenden Tabelle:</span><span class="sxs-lookup"><span data-stu-id="5ee04-127">For example, if the transport provider is SMTP, to register the provider with Microsoft Outlook 2010, set the following key to the data in the following table:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |<span data-ttu-id="5ee04-128">Name</span><span class="sxs-lookup"><span data-stu-id="5ee04-128">Name</span></span> |<span data-ttu-id="5ee04-129">Typ</span><span class="sxs-lookup"><span data-stu-id="5ee04-129">Type</span></span> |<span data-ttu-id="5ee04-130">Wert</span><span class="sxs-lookup"><span data-stu-id="5ee04-130">Value</span></span> |
   |:-----|:-----|:-----|
   |<span data-ttu-id="5ee04-131">SMTP</span><span class="sxs-lookup"><span data-stu-id="5ee04-131">SMTP</span></span>  |<span data-ttu-id="5ee04-132">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5ee04-132">REG_SZ</span></span>  |<span data-ttu-id="5ee04-133">{CLSID für die jeweilige Implementierung der IFreeBusySupport}</span><span class="sxs-lookup"><span data-stu-id="5ee04-133">{CLSID for respective implementation of IFreeBusySupport}</span></span>  |
   
   <span data-ttu-id="5ee04-134">In diesem Szenario wird Outlook gemeinsame erstellt die COM-Klasse und wird verwendet, um das Abrufen von Frei/Gebucht-Informationen für eine beliebige SMTP-Mail-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="5ee04-134">In this scenario, Outlook co-creates the COM class and uses it to retrieve free/busy information for any SMTP mail users.</span></span>
    
<span data-ttu-id="5ee04-135">Ändern Sie den *Namen* entsprechend zur Unterstützung eines Adresse Adressbuch und Transport-Anbieters, die einen Eintrag Adresstyp als SMTP verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ee04-135">To support an address book and transport provider that use an address entry type other than SMTP, change the  *Name* accordingly.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5ee04-136">Frei/Gebucht-Anbieter sollte während der Installation, überprüfen Sie, ob eine Einstellung in der Registrierung für den gleichen Adresstyp Eintrag bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5ee04-136">During installation, free/busy providers should check whether a registry setting for the the same address entry type already exists.</span></span> <span data-ttu-id="5ee04-137">Wenn dies der Fall ist, sollte der Frei/Gebucht-Anbieter überschreiben den aktuellen Anbieter für diesen Eintrag Adresstyp und an diesen Anbieter wiederherstellen, wenn es deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="5ee04-137">If it does, the free/busy provider should overwrite the current provider for that address entry type, and restore to that provider when it uninstalls.</span></span> <span data-ttu-id="5ee04-138">Jedoch, wenn ein Benutzer mehr als eine Frei/Gebucht-Anbieter für den gleichen Eintrag Adresstyp installiert wurde, der Benutzer sollte deinstallieren diese Anbieter in umgekehrter Reihenfolge als Installation (d. h., immer deinstallieren den neuesten Anbieter).</span><span class="sxs-lookup"><span data-stu-id="5ee04-138">However, if a user has installed more than one free/busy provider for the same address entry type, the user should uninstall these providers in the reverse order as installation (that is, always uninstall the latest provider).</span></span> <span data-ttu-id="5ee04-139">Andernfalls kann die Registrierung für einen Anbieter verweist, die bereits deinstalliert wurde.</span><span class="sxs-lookup"><span data-stu-id="5ee04-139">Otherwise, the registry may point to a provider that has already been uninstalled.</span></span> 
  
## <a name="api-components"></a><span data-ttu-id="5ee04-140">API-Komponenten</span><span class="sxs-lookup"><span data-stu-id="5ee04-140">API components</span></span>

<span data-ttu-id="5ee04-141">Die Frei/Gebucht-API umfasst die folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="5ee04-141">The Free/Busy API includes the following components:</span></span>
  
### <a name="definitions"></a><span data-ttu-id="5ee04-142">Definitionen</span><span class="sxs-lookup"><span data-stu-id="5ee04-142">Definitions</span></span>

- [<span data-ttu-id="5ee04-143">Konstanten (Frei/Gebucht-API)</span><span class="sxs-lookup"><span data-stu-id="5ee04-143">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
    
### <a name="data-types"></a><span data-ttu-id="5ee04-144">Datentypen</span><span class="sxs-lookup"><span data-stu-id="5ee04-144">Data types</span></span>

- [<span data-ttu-id="5ee04-145">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="5ee04-145">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="5ee04-146">FBStatus</span><span class="sxs-lookup"><span data-stu-id="5ee04-146">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="5ee04-147">FBUser</span><span class="sxs-lookup"><span data-stu-id="5ee04-147">FBUser</span></span>](fbuser.md)
    
### <a name="interfaces"></a><span data-ttu-id="5ee04-148">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5ee04-148">Interfaces</span></span>

- [<span data-ttu-id="5ee04-149">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="5ee04-149">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="5ee04-150">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="5ee04-150">IFreeBusyData</span></span>](ifreebusydata.md)
- [<span data-ttu-id="5ee04-151">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="5ee04-151">IFreeBusySupport</span></span>](ifreebusysupport.md)
    

