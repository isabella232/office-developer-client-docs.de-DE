---
title: Öffnen ein Adressbuchcontainer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Zuletzt geändert: 08 November 2011'
ms.openlocfilehash: 28f60154524065bd2c818e2e4b7db37ca33276b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793313"
---
# <a name="opening-an-address-book-container"></a><span data-ttu-id="0c416-103">Öffnen ein Adressbuchcontainer</span><span class="sxs-lookup"><span data-stu-id="0c416-103">Opening an address book container</span></span>

<span data-ttu-id="0c416-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0c416-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0c416-105">Nach dem Öffnen der MAPI-Adressbuch integriert, öffnen Sie eine oder mehrere Address Book Containern Zugriff auf die darin enthaltenen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="0c416-105">After opening the MAPI integrated address book, open one or more address book containers to access the recipients within them.</span></span>
  
<span data-ttu-id="0c416-106">Rufen Sie zum Öffnen den Container der obersten Ebene des Adressbuchs [IAddrBook::OpenEntry](iaddrbook-openentry.md) mit einem NULL-Eintrags-ID ein.</span><span class="sxs-lookup"><span data-stu-id="0c416-106">To open the top-level container of the address book, call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier.</span></span> 
  
<span data-ttu-id="0c416-107">Address Book Containern können implementiert werden, mit der nur-Lese- oder Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0c416-107">Address book containers can be implemented with read-only or read/write access.</span></span> <span data-ttu-id="0c416-108">Nur-Lese-Containern dienen nur zum Durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="0c416-108">Read-only containers are used only for browsing.</span></span> <span data-ttu-id="0c416-109">Lese-Schreib-Container können geändert werden, dass Clients, die zum Erstellen neuer Einträge und löschen und Ändern der vorhandenen Einträge.</span><span class="sxs-lookup"><span data-stu-id="0c416-109">Read/write containers can be modified, allowing clients to create new entries and delete and modify existing entries.</span></span> <span data-ttu-id="0c416-110">Alle Persönliches Adressbuch (PAB) Container werden als Container für Lese-/Schreibzugriff implementiert.</span><span class="sxs-lookup"><span data-stu-id="0c416-110">All personal address book (PAB) containers are implemented as read/write containers.</span></span> 
  
<span data-ttu-id="0c416-111">Zum Öffnen ein unteren Ebene Containers rufen Sie **OpenEntry auf** , und geben Sie die Eintrags-ID des Containers geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c416-111">To open any lower level container, call **OpenEntry** and specify the entry identifier of the container to be opened.</span></span> 
  
## <a name="open-the-container-designated-as-the-pab"></a><span data-ttu-id="0c416-112">Öffnen Sie den Container der PAB als</span><span class="sxs-lookup"><span data-stu-id="0c416-112">Open the container designated as the PAB</span></span>
  
1. <span data-ttu-id="0c416-113">Rufen Sie [IAddrBook::GetPAB](iaddrbook-getpab.md) , um die PAB-Eintrags-ID abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0c416-113">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the PAB's entry identifier.</span></span> 
    
2. <span data-ttu-id="0c416-114">Übergeben Sie dieses Eintrags-ID an [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="0c416-114">Pass this entry identifier to [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span>
    
## <a name="open-a-container-that-is-not-the-pab"></a><span data-ttu-id="0c416-115">Öffnen Sie einen Container, der nicht die PAB ist</span><span class="sxs-lookup"><span data-stu-id="0c416-115">Open a container that is not the PAB</span></span>
  
1. <span data-ttu-id="0c416-116">Rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md) mit einen NULL-Eintrags-ID im Adressbuch Stammcontainer öffnen.</span><span class="sxs-lookup"><span data-stu-id="0c416-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier to open the address book's root container.</span></span> 
    
2. <span data-ttu-id="0c416-117">Rufen Sie den Container Root [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) -Methode zum Abrufen der Hierarchietabelle – eine Liste aller Container der obersten Ebene im Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="0c416-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to retrieve its hierarchy table — a list of all of the top-level containers in the address book.</span></span> 
    
3. <span data-ttu-id="0c416-118">Wenn der Container zum Öffnen eines bestimmten Typs ist:</span><span class="sxs-lookup"><span data-stu-id="0c416-118">If the container to be opened is of a specific type:</span></span>
    
   - <span data-ttu-id="0c416-119">Erstellen Sie eine **SPropertyRestriction** -Struktur mit **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) für das Eigenschafts-Tag, das Container-Typ für den Eigenschaftswert und RELOP_EQ für die Beziehung.</span><span class="sxs-lookup"><span data-stu-id="0c416-119">Create an **SPropertyRestriction** structure with **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) for the property tag, the container's type for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="0c416-120">**PR_DISPLAY_TYPE** können auf viele Werte, zwischen ihnen festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="0c416-120">**PR_DISPLAY_TYPE** can be set to many values, among them:</span></span> 
    
   - <span data-ttu-id="0c416-121">DT_GLOBAL die Hierarchietabelle Containern beschränken, die in der globalen Adressliste gehören.</span><span class="sxs-lookup"><span data-stu-id="0c416-121">DT_GLOBAL to limit the hierarchy table to containers that belong in the global address list.</span></span>
    
   - <span data-ttu-id="0c416-122">DT_LOCAL die Tabelle, die zu einem lokalen Adressbuch gehören Containern beschränken.</span><span class="sxs-lookup"><span data-stu-id="0c416-122">DT_LOCAL to limit the table to containers belonging to a local address book.</span></span>
    
   - <span data-ttu-id="0c416-123">DT_MODIFIABLE die Tabelle Containern beschränken, die geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="0c416-123">DT_MODIFIABLE to limit the table to containers that can be modified.</span></span>
    
   - <span data-ttu-id="0c416-124">Erstellen einer [SPropTagArray](sproptagarray.md) -Struktur, die **PR_ENTRYID** **PR_DISPLAY_TYPE**und alle anderen Spalten von Interesse enthält.</span><span class="sxs-lookup"><span data-stu-id="0c416-124">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID**, **PR_DISPLAY_TYPE**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="0c416-125">Rufen Sie [HrQueryAllRows](hrqueryallrows.md), Ihre eigenschaftseinschränkung und Tag-Array-Eigenschaft übergeben.</span><span class="sxs-lookup"><span data-stu-id="0c416-125">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="0c416-126">NULL oder mehr Zeilen, eine Zeile für jedes Container, in den angegebenen Typ gehört, gibt **HrQueryAllRows** zurück.</span><span class="sxs-lookup"><span data-stu-id="0c416-126">**HrQueryAllRows** will return zero or more rows, one row for every container that belongs to the specified type.</span></span> <span data-ttu-id="0c416-127">Bereiten Sie die Rückgabe einer beliebigen Anzahl von Zeilen zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="0c416-127">Be prepared to handle the return of any number of rows.</span></span> 
    
   - <span data-ttu-id="0c416-128">Rufen Sie **IAddrBook::OpenEntry** , wobei die Eintrags-ID aus der **PR_ENTRYID** -Spalte der Zeile, die den Container von Interesse darstellt.</span><span class="sxs-lookup"><span data-stu-id="0c416-128">Call **IAddrBook::OpenEntry** with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> 
    
4. <span data-ttu-id="0c416-129">Zugehörigkeit der Container zum Öffnen einer bestimmten Adressbuchanbieter:</span><span class="sxs-lookup"><span data-stu-id="0c416-129">If the container to be opened belongs to a specific address book provider:</span></span>
    
   - <span data-ttu-id="0c416-130">Erstellen Sie eine [SPropertyRestriction](spropertyrestriction.md) -Struktur mit **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) für das Eigenschafts-Tag, anbieterspezifische Wert für den Eigenschaftswert und RELOP_EQ für die Beziehung.</span><span class="sxs-lookup"><span data-stu-id="0c416-130">Create an [SPropertyRestriction](spropertyrestriction.md) structure with **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) for the property tag, a provider-specific value for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="0c416-131">In der Regel ist der Wert der anbieterspezifische einen global eindeutigen Bezeichner oder eine GUID.</span><span class="sxs-lookup"><span data-stu-id="0c416-131">Typically the provider-specific value is a globally unique identifier or GUID.</span></span> <span data-ttu-id="0c416-132">Sie finden dieses Werts in eine der Headerdateien der Adressbuchanbieter veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="0c416-132">You will find this value published in one of the address book provider's header files.</span></span> 
    
   - <span data-ttu-id="0c416-133">Erstellen einer [SPropTagArray](sproptagarray.md) -Struktur, die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**und alle anderen Spalten von Interesse enthält.</span><span class="sxs-lookup"><span data-stu-id="0c416-133">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="0c416-134">Rufen Sie [HrQueryAllRows](hrqueryallrows.md), Ihre eigenschaftseinschränkung und Tag-Array-Eigenschaft übergeben.</span><span class="sxs-lookup"><span data-stu-id="0c416-134">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="0c416-135">**HrQueryAllRows** gibt 0 (null) Zeilen zurück, wenn die angegebene Adressbuchanbieter nicht im Profil vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0c416-135">**HrQueryAllRows** will return zero rows if the specified address book provider is not in the profile.</span></span> <span data-ttu-id="0c416-136">Sie können eine oder mehrere Zeilen für den Anbieter Container auf oberster Ebene, je nach der Struktur des Anbieters zurück.</span><span class="sxs-lookup"><span data-stu-id="0c416-136">It can return one or more rows for the provider's top-level containers, depending on how the provider is organized.</span></span> 
    
   - <span data-ttu-id="0c416-137">Rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md) , wobei die Eintrags-ID aus der **PR_ENTRYID** -Spalte der Zeile, die den Container von Interesse darstellt.</span><span class="sxs-lookup"><span data-stu-id="0c416-137">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> <span data-ttu-id="0c416-138">Ist der Container, dem Sie interessiert sind nicht Container der obersten Ebene, suchen Sie den Container der obersten Ebene, und Durchlaufen der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="0c416-138">If the container that you are interested in is not a top-level container, find the top-level container and traverse the hierarchy.</span></span> 
    

