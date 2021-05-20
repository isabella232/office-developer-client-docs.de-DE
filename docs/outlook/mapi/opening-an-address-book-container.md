---
title: Öffnen eines Adressbuchcontainers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Letzte Änderung: 08. November 2011'
ms.openlocfilehash: 97fa9f9750174c112c431c62f6171f674856fa86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436741"
---
# <a name="opening-an-address-book-container"></a><span data-ttu-id="4acd7-103">Öffnen eines Adressbuchcontainers</span><span class="sxs-lookup"><span data-stu-id="4acd7-103">Opening an address book container</span></span>

<span data-ttu-id="4acd7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4acd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4acd7-105">Öffnen Sie nach dem Öffnen des integrierten Adressbuchs MAPI einen oder mehrere Adressbuchcontainer, um auf die empfänger in ihnen zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="4acd7-105">After opening the MAPI integrated address book, open one or more address book containers to access the recipients within them.</span></span>
  
<span data-ttu-id="4acd7-106">Um den Container auf oberster Ebene des Adressbuchs zu öffnen, rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md) mit einem NULL-Eintragsbezeichner auf.</span><span class="sxs-lookup"><span data-stu-id="4acd7-106">To open the top-level container of the address book, call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier.</span></span> 
  
<span data-ttu-id="4acd7-107">Adressbuchcontainer können mit Lese-/Schreibzugriff implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="4acd7-107">Address book containers can be implemented with read-only or read/write access.</span></span> <span data-ttu-id="4acd7-108">Schreibgeschützte Container werden nur zum Browsen verwendet.</span><span class="sxs-lookup"><span data-stu-id="4acd7-108">Read-only containers are used only for browsing.</span></span> <span data-ttu-id="4acd7-109">Lese-/Schreibzugriffscontainer können geändert werden, sodass Clients neue Einträge erstellen und vorhandene Einträge löschen und ändern können.</span><span class="sxs-lookup"><span data-stu-id="4acd7-109">Read/write containers can be modified, allowing clients to create new entries and delete and modify existing entries.</span></span> <span data-ttu-id="4acd7-110">Alle Persönliche Adressbuchcontainer (PAB) werden als Lese-/Schreibcontainer implementiert.</span><span class="sxs-lookup"><span data-stu-id="4acd7-110">All personal address book (PAB) containers are implemented as read/write containers.</span></span> 
  
<span data-ttu-id="4acd7-111">Rufen Sie **openEntry** auf, und geben Sie den Eintragsbezeichner des zu öffnenden Containers an, um einen Container auf niedrigerer Ebene zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4acd7-111">To open any lower level container, call **OpenEntry** and specify the entry identifier of the container to be opened.</span></span> 
  
## <a name="open-the-container-designated-as-the-pab"></a><span data-ttu-id="4acd7-112">Öffnen des als PAB festgelegten Containers</span><span class="sxs-lookup"><span data-stu-id="4acd7-112">Open the container designated as the PAB</span></span>
  
1. <span data-ttu-id="4acd7-113">Rufen [Sie IAddrBook::GetPAB auf,](iaddrbook-getpab.md) um den Eintragsbezeichner des PAB abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4acd7-113">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the PAB's entry identifier.</span></span> 
    
2. <span data-ttu-id="4acd7-114">Übergeben Sie diesen Eintragsbezeichner [an IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="4acd7-114">Pass this entry identifier to [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span>
    
## <a name="open-a-container-that-is-not-the-pab"></a><span data-ttu-id="4acd7-115">Öffnen eines Containers, der nicht das PAB ist</span><span class="sxs-lookup"><span data-stu-id="4acd7-115">Open a container that is not the PAB</span></span>
  
1. <span data-ttu-id="4acd7-116">Rufen [Sie IAddrBook::OpenEntry](iaddrbook-openentry.md) mit einem NULL-Eintragsbezeichner auf, um den Stammcontainer des Adressbuchs zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4acd7-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier to open the address book's root container.</span></span> 
    
2. <span data-ttu-id="4acd7-117">Rufen Sie die [IMAPIContainer::GetHierarchyTable-Methode](imapicontainer-gethierarchytable.md) des Stammcontainers auf, um die Hierarchietabelle abzurufen – eine Liste aller Container auf oberster Ebene im Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="4acd7-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to retrieve its hierarchy table — a list of all of the top-level containers in the address book.</span></span> 
    
3. <span data-ttu-id="4acd7-118">Wenn der zu öffnende Container einen bestimmten Typ hat:</span><span class="sxs-lookup"><span data-stu-id="4acd7-118">If the container to be opened is of a specific type:</span></span>
    
   - <span data-ttu-id="4acd7-119">Erstellen Sie eine **SPropertyRestriction-Struktur** mit **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) für das Eigenschaftstag, den Containertyp für den Eigenschaftswert und RELOP_EQ für die Beziehung.</span><span class="sxs-lookup"><span data-stu-id="4acd7-119">Create an **SPropertyRestriction** structure with **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) for the property tag, the container's type for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="4acd7-120">**PR_DISPLAY_TYPE** können auf viele Werte festgelegt werden, darunter:</span><span class="sxs-lookup"><span data-stu-id="4acd7-120">**PR_DISPLAY_TYPE** can be set to many values, among them:</span></span> 
    
   - <span data-ttu-id="4acd7-121">DT_GLOBAL, um die Hierarchietabelle auf Container zu beschränken, die in die globale Adressliste gehören.</span><span class="sxs-lookup"><span data-stu-id="4acd7-121">DT_GLOBAL to limit the hierarchy table to containers that belong in the global address list.</span></span>
    
   - <span data-ttu-id="4acd7-122">DT_LOCAL, um die Tabelle auf Container zu beschränken, die zu einem lokalen Adressbuch gehören.</span><span class="sxs-lookup"><span data-stu-id="4acd7-122">DT_LOCAL to limit the table to containers belonging to a local address book.</span></span>
    
   - <span data-ttu-id="4acd7-123">DT_MODIFIABLE, um die Tabelle auf Container zu beschränken, die geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="4acd7-123">DT_MODIFIABLE to limit the table to containers that can be modified.</span></span>
    
   - <span data-ttu-id="4acd7-124">Erstellen Sie [eine SPropTagArray-Struktur,](sproptagarray.md) die **PR_ENTRYID**, **PR_DISPLAY_TYPE** und andere wichtige Spalten enthält.</span><span class="sxs-lookup"><span data-stu-id="4acd7-124">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID**, **PR_DISPLAY_TYPE**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="4acd7-125">Rufen [Sie HrQueryAllRows auf,](hrqueryallrows.md)und übergeben Sie ihr Eigenschaftseinschränkungs- und Eigenschaftentagarray.</span><span class="sxs-lookup"><span data-stu-id="4acd7-125">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="4acd7-126">**HrQueryAllRows** gibt null oder mehr Zeilen zurück, eine Zeile für jeden Container, der zum angegebenen Typ gehört.</span><span class="sxs-lookup"><span data-stu-id="4acd7-126">**HrQueryAllRows** will return zero or more rows, one row for every container that belongs to the specified type.</span></span> <span data-ttu-id="4acd7-127">Bereiten Sie sich darauf vor, die Rückgabe einer beliebigen Anzahl von Zeilen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="4acd7-127">Be prepared to handle the return of any number of rows.</span></span> 
    
   - <span data-ttu-id="4acd7-128">Rufen **Sie IAddrBook::OpenEntry** mit dem Eintragsbezeichner aus der spalte **PR_ENTRYID** der Zeile auf, die den container von Interesse darstellt.</span><span class="sxs-lookup"><span data-stu-id="4acd7-128">Call **IAddrBook::OpenEntry** with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> 
    
4. <span data-ttu-id="4acd7-129">Wenn der zu öffnende Container zu einem bestimmten Adressbuchanbieter gehört:</span><span class="sxs-lookup"><span data-stu-id="4acd7-129">If the container to be opened belongs to a specific address book provider:</span></span>
    
   - <span data-ttu-id="4acd7-130">Erstellen Sie eine [SPropertyRestriction-Struktur](spropertyrestriction.md) mit **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) für das Eigenschaftstag, einen anbieterspezifischen Wert für den Eigenschaftswert und RELOP_EQ für die Beziehung.</span><span class="sxs-lookup"><span data-stu-id="4acd7-130">Create an [SPropertyRestriction](spropertyrestriction.md) structure with **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) for the property tag, a provider-specific value for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="4acd7-131">In der Regel ist der anbieterspezifische Wert eine global eindeutige ID oder GUID.</span><span class="sxs-lookup"><span data-stu-id="4acd7-131">Typically the provider-specific value is a globally unique identifier or GUID.</span></span> <span data-ttu-id="4acd7-132">Dieser Wert wird in einer der Headerdateien des Adressbuchanbieters veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="4acd7-132">You will find this value published in one of the address book provider's header files.</span></span> 
    
   - <span data-ttu-id="4acd7-133">Erstellen Sie [eine SPropTagArray-Struktur,](sproptagarray.md) die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS** und alle anderen von Interesse eignen Spalten enthält.</span><span class="sxs-lookup"><span data-stu-id="4acd7-133">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="4acd7-134">Rufen [Sie HrQueryAllRows auf,](hrqueryallrows.md)und übergeben Sie ihr Eigenschaftseinschränkungs- und Eigenschaftentagarray.</span><span class="sxs-lookup"><span data-stu-id="4acd7-134">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="4acd7-135">**HrQueryAllRows** gibt null Zeilen zurück, wenn sich der angegebene Adressbuchanbieter nicht im Profil befindet.</span><span class="sxs-lookup"><span data-stu-id="4acd7-135">**HrQueryAllRows** will return zero rows if the specified address book provider is not in the profile.</span></span> <span data-ttu-id="4acd7-136">Je nach Organisation des Anbieters kann eine oder mehrere Zeilen für die Container auf oberster Ebene des Anbieters zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4acd7-136">It can return one or more rows for the provider's top-level containers, depending on how the provider is organized.</span></span> 
    
   - <span data-ttu-id="4acd7-137">Rufen [Sie IAddrBook::OpenEntry](iaddrbook-openentry.md) mit dem Eintragsbezeichner aus der spalte **PR_ENTRYID** der Zeile auf, die den container von Interesse darstellt.</span><span class="sxs-lookup"><span data-stu-id="4acd7-137">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> <span data-ttu-id="4acd7-138">Wenn es sich bei dem Container, an dem Sie interessiert sind, nicht um einen Container auf oberster Ebene handelt, suchen Sie den Container auf oberster Ebene, und durchlaufen Sie die Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="4acd7-138">If the container that you are interested in is not a top-level container, find the top-level container and traverse the hierarchy.</span></span> 
    

