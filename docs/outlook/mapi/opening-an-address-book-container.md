---
title: Öffnen eines Adressbuchcontainers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Zuletzt geändert: 20 November, 2011'
ms.openlocfilehash: 97fa9f9750174c112c431c62f6171f674856fa86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326579"
---
# <a name="opening-an-address-book-container"></a><span data-ttu-id="84ede-103">Öffnen eines Adressbuchcontainers</span><span class="sxs-lookup"><span data-stu-id="84ede-103">Opening an address book container</span></span>

<span data-ttu-id="84ede-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84ede-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84ede-105">Öffnen Sie nach dem Öffnen des integrierten MAPI-Adressbuchs einen oder mehrere Adressbuchcontainer für den Zugriff auf die Empfänger in diesen.</span><span class="sxs-lookup"><span data-stu-id="84ede-105">After opening the MAPI integrated address book, open one or more address book containers to access the recipients within them.</span></span>
  
<span data-ttu-id="84ede-106">Um den Container der obersten Ebene des Adressbuchs zu öffnen, rufen Sie [IAddrBook:: OpenEntry](iaddrbook-openentry.md) mit einer NULL-Eintrags-ID auf.</span><span class="sxs-lookup"><span data-stu-id="84ede-106">To open the top-level container of the address book, call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier.</span></span> 
  
<span data-ttu-id="84ede-107">Adressbuchcontainer können mit Schreibschutz oder Lese-/Schreibzugriff implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="84ede-107">Address book containers can be implemented with read-only or read/write access.</span></span> <span data-ttu-id="84ede-108">Schreibgeschützte Container werden nur zum Browsen verwendet.</span><span class="sxs-lookup"><span data-stu-id="84ede-108">Read-only containers are used only for browsing.</span></span> <span data-ttu-id="84ede-109">Container mit Lese-/Schreibzugriff können geändert werden, sodass Clients neue Einträge erstellen und vorhandene Einträge löschen und ändern kann.</span><span class="sxs-lookup"><span data-stu-id="84ede-109">Read/write containers can be modified, allowing clients to create new entries and delete and modify existing entries.</span></span> <span data-ttu-id="84ede-110">Alle PAB-Container (persönliches Adressbuch) werden als Lese-/Schreibzugriff-Container implementiert.</span><span class="sxs-lookup"><span data-stu-id="84ede-110">All personal address book (PAB) containers are implemented as read/write containers.</span></span> 
  
<span data-ttu-id="84ede-111">Um einen Container mit niedrigerer Ebene zu \*\*\*\* öffnen, rufen Sie OpenEntry auf, und geben Sie den Eintragsbezeichner des zu öffnenden Containers an.</span><span class="sxs-lookup"><span data-stu-id="84ede-111">To open any lower level container, call **OpenEntry** and specify the entry identifier of the container to be opened.</span></span> 
  
## <a name="open-the-container-designated-as-the-pab"></a><span data-ttu-id="84ede-112">Öffnen des als PAB festgelegten Containers</span><span class="sxs-lookup"><span data-stu-id="84ede-112">Open the container designated as the PAB</span></span>
  
1. <span data-ttu-id="84ede-113">Rufen Sie [IAddrBook:: GetPAB](iaddrbook-getpab.md) auf, um die Eintrags-ID des PAB abzurufen.</span><span class="sxs-lookup"><span data-stu-id="84ede-113">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the PAB's entry identifier.</span></span> 
    
2. <span data-ttu-id="84ede-114">Führen Sie diesen Eintragsbezeichner an [IAddrBook:: OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="84ede-114">Pass this entry identifier to [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span>
    
## <a name="open-a-container-that-is-not-the-pab"></a><span data-ttu-id="84ede-115">Öffnen eines Containers, der nicht das PAB ist</span><span class="sxs-lookup"><span data-stu-id="84ede-115">Open a container that is not the PAB</span></span>
  
1. <span data-ttu-id="84ede-116">Rufen Sie [IAddrBook:: OpenEntry](iaddrbook-openentry.md) mit einer NULL-Eintrags-ID auf, um den Stammcontainer des Adressbuchs zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="84ede-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier to open the address book's root container.</span></span> 
    
2. <span data-ttu-id="84ede-117">Rufen Sie die [IMAPIContainer:: gethierarchyid](imapicontainer-gethierarchytable.md) -Methode des Stammcontainers auf, um die Hierarchietabelle abzurufen – eine Liste aller Container der obersten Ebene im Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="84ede-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to retrieve its hierarchy table — a list of all of the top-level containers in the address book.</span></span> 
    
3. <span data-ttu-id="84ede-118">Wenn der Container, der geöffnet werden soll, einen bestimmten Typ hat:</span><span class="sxs-lookup"><span data-stu-id="84ede-118">If the container to be opened is of a specific type:</span></span>
    
   - <span data-ttu-id="84ede-119">Erstellen Sie eine **SPropertyRestriction** -Struktur mit **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) für das Property-Tag, den Typ des Containers für den Eigenschaftswert und RELOP_EQ für die Beziehung.</span><span class="sxs-lookup"><span data-stu-id="84ede-119">Create an **SPropertyRestriction** structure with **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) for the property tag, the container's type for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="84ede-120">**PR_DISPLAY_TYPE** kann auf viele Werte festgelegt werden, darunter:</span><span class="sxs-lookup"><span data-stu-id="84ede-120">**PR_DISPLAY_TYPE** can be set to many values, among them:</span></span> 
    
   - <span data-ttu-id="84ede-121">DT_GLOBAL, um die Hierarchietabelle auf Container zu begrenzen, die in die globale Adressliste gehören.</span><span class="sxs-lookup"><span data-stu-id="84ede-121">DT_GLOBAL to limit the hierarchy table to containers that belong in the global address list.</span></span>
    
   - <span data-ttu-id="84ede-122">DT_LOCAL, um die Tabelle auf Container zu begrenzen, die zu einem lokalen Adressbuch gehören.</span><span class="sxs-lookup"><span data-stu-id="84ede-122">DT_LOCAL to limit the table to containers belonging to a local address book.</span></span>
    
   - <span data-ttu-id="84ede-123">DT_MODIFIABLE, um die Tabelle auf Container zu begrenzen, die geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="84ede-123">DT_MODIFIABLE to limit the table to containers that can be modified.</span></span>
    
   - <span data-ttu-id="84ede-124">Erstellen Sie eine [SPropTagArray](sproptagarray.md) -Struktur, die **PR_ENTRYID**, **PR_DISPLAY_TYPE**und alle anderen interessierenden Spalten enthält.</span><span class="sxs-lookup"><span data-stu-id="84ede-124">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID**, **PR_DISPLAY_TYPE**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="84ede-125">Rufen Sie [HrQueryAllRows](hrqueryallrows.md)auf, und übergeben Sie Ihre Eigenschaftseinschränkung und das Property-Tag-Array.</span><span class="sxs-lookup"><span data-stu-id="84ede-125">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="84ede-126">**HrQueryAllRows** gibt NULL oder mehr Zeilen zurück, eine Zeile für jeden Container, der zum angegebenen Typ gehört.</span><span class="sxs-lookup"><span data-stu-id="84ede-126">**HrQueryAllRows** will return zero or more rows, one row for every container that belongs to the specified type.</span></span> <span data-ttu-id="84ede-127">Bereiten Sie die Rückgabe einer beliebigen Anzahl von Zeilen vor.</span><span class="sxs-lookup"><span data-stu-id="84ede-127">Be prepared to handle the return of any number of rows.</span></span> 
    
   - <span data-ttu-id="84ede-128">Rufen Sie **IAddrBook:: OpenEntry** mit der Eintrags-ID aus der **PR_ENTRYID** -Spalte der Zeile, die den Container von Interesse darstellt.</span><span class="sxs-lookup"><span data-stu-id="84ede-128">Call **IAddrBook::OpenEntry** with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> 
    
4. <span data-ttu-id="84ede-129">Wenn der zu öffnende Container zu einem bestimmten Adressbuchanbieter gehört:</span><span class="sxs-lookup"><span data-stu-id="84ede-129">If the container to be opened belongs to a specific address book provider:</span></span>
    
   - <span data-ttu-id="84ede-130">Erstellen Sie eine [SPropertyRestriction](spropertyrestriction.md) -Struktur mit **PR_AB_PROVIDERS** ([pidtagabproviders (](pidtagabproviders-canonical-property.md)) für das Property-Tag, einen anbieterspezifischen Wert für den Eigenschaftswert und RELOP_EQ für die Beziehung.</span><span class="sxs-lookup"><span data-stu-id="84ede-130">Create an [SPropertyRestriction](spropertyrestriction.md) structure with **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) for the property tag, a provider-specific value for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="84ede-131">Der anbieterspezifische Wert ist in der Regel ein global eindeutiger Bezeichner oder eine GUID.</span><span class="sxs-lookup"><span data-stu-id="84ede-131">Typically the provider-specific value is a globally unique identifier or GUID.</span></span> <span data-ttu-id="84ede-132">Dieser Wert wird in einer der Headerdateien des Adressbuch Anbieters veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="84ede-132">You will find this value published in one of the address book provider's header files.</span></span> 
    
   - <span data-ttu-id="84ede-133">Erstellen Sie eine [SPropTagArray](sproptagarray.md) -Struktur, die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**und alle anderen interessierenden Spalten enthält.</span><span class="sxs-lookup"><span data-stu-id="84ede-133">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="84ede-134">Rufen Sie [HrQueryAllRows](hrqueryallrows.md)auf, und übergeben Sie Ihre Eigenschaftseinschränkung und das Property-Tag-Array.</span><span class="sxs-lookup"><span data-stu-id="84ede-134">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="84ede-135">**HrQueryAllRows** gibt keine Zeilen zurück, wenn sich der angegebene Adressbuchanbieter nicht im Profil befindet.</span><span class="sxs-lookup"><span data-stu-id="84ede-135">**HrQueryAllRows** will return zero rows if the specified address book provider is not in the profile.</span></span> <span data-ttu-id="84ede-136">Je nachdem, wie der Anbieter organisiert ist, kann er eine oder mehrere Zeilen für die Container der obersten Ebene des Anbieters zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="84ede-136">It can return one or more rows for the provider's top-level containers, depending on how the provider is organized.</span></span> 
    
   - <span data-ttu-id="84ede-137">Rufen Sie [IAddrBook:: OpenEntry](iaddrbook-openentry.md) mit der Eintrags-ID aus der **PR_ENTRYID** -Spalte der Zeile, die den Container von Interesse darstellt.</span><span class="sxs-lookup"><span data-stu-id="84ede-137">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> <span data-ttu-id="84ede-138">Wenn der Container, an dem Sie interessiert sind, kein Container der obersten Ebene ist, suchen Sie den Container der obersten Ebene, und überqueren Sie die Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="84ede-138">If the container that you are interested in is not a top-level container, find the top-level container and traverse the hierarchy.</span></span> 
    

