---
title: Schreiben eines Hierarchie Viewers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0286696707d268867a5536ef345d0af7909918dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795864"
---
# <a name="writing-a-hierarchy-viewer"></a><span data-ttu-id="01129-103">Schreiben eines Hierarchie Viewers</span><span class="sxs-lookup"><span data-stu-id="01129-103">Writing a Hierarchy Viewer</span></span>

  
  
<span data-ttu-id="01129-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="01129-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="01129-105">Ein Hierarchie Viewer ist eine Komponente der Benutzeroberfläche, die für die Anzeige von Ordner Tabellen und Address Book Container Hierarchie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="01129-105">A hierarchy viewer is a user interface component that is used for displaying folder and address book container hierarchy tables.</span></span> <span data-ttu-id="01129-106">Hierarchie Viewer können Mitglieder der Hierarchie auf verschiedenen Ebenen, erweitern und jede Ebene bei Bedarf vergeben anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="01129-106">Hierarchy viewers can display members of the hierarchy at different levels, expanding and contracting each level on demand.</span></span>
  
<span data-ttu-id="01129-107">Die Container-Eigenschaft **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) steuert die Ebene, auf der Hierarchie Mitglied angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="01129-107">The container property, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controls the level at which a hierarchy member is displayed.</span></span> <span data-ttu-id="01129-108">Einträge, die auf oberster Ebene Address Book Container oder Ordner darstellen, haben die **PR_DEPTH** -Eigenschaft auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="01129-108">Entries that represent top-level address book containers or folders have their **PR_DEPTH** property set to zero.</span></span> <span data-ttu-id="01129-109">Der Wert dieser Eigenschaft wird für die Einträge im sequenziellen Ebenen sequenziell erhöht.</span><span class="sxs-lookup"><span data-stu-id="01129-109">The value of this property is incremented sequentially for entries in sequential levels.</span></span> <span data-ttu-id="01129-110">Legen alle Container mit **PR_DEPTH** auf 1 d. h., wenn der Benutzer einen Container der obersten Ebene wählt zu erweitern, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="01129-110">That is, when a user selects a top-level container to expand, display all containers with **PR_DEPTH** set to 1.</span></span> <span data-ttu-id="01129-111">Sobald ein Benutzer eine der folgenden Container erweitert, 2 anzeigen Sie die Container mit **PR_DEPTH** , usw.</span><span class="sxs-lookup"><span data-stu-id="01129-111">When a user expands one of these subcontainers, display the containers with **PR_DEPTH** set to 2, and so on.</span></span> 
  
<span data-ttu-id="01129-112">Hierarchie Viewer unterstützt einen anderen Bereich mit Tiefen.</span><span class="sxs-lookup"><span data-stu-id="01129-112">Hierarchy viewers support a different range of depths.</span></span> <span data-ttu-id="01129-113">Sie können Ihre Viewer, nur ein oder zwei Ebenen einschränken oder können Sie mehrere Ebenen unterstützen, wenn der expansiven Hierarchieanzeige eine Priorität ist.</span><span class="sxs-lookup"><span data-stu-id="01129-113">You can limit your viewer to only one or two levels or you can support multiple levels, if displaying an expansive hierarchy is a priority.</span></span> 
  
<span data-ttu-id="01129-114">Das Adressbuch bietet einen Hierarchie-Viewer für den Container der obersten Ebene im Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="01129-114">The address book provides a hierarchy viewer for the top-level containers in the address book.</span></span> 
  
 <span data-ttu-id="01129-115">**Zugriff auf die Address Book Hierarchie-Tabelle**</span><span class="sxs-lookup"><span data-stu-id="01129-115">**To access the address book hierarchy table**</span></span>
  
1. <span data-ttu-id="01129-116">Rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md), übergeben eine null-Eintrags-ID, um Container für das Adressbuch Root zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="01129-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing a null entry identifier, to open the address book's root container.</span></span>
    
2. <span data-ttu-id="01129-117">Rufen Sie den Container Root [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) -Methode zum Zugriff auf die Hierarchietabelle des MAPI-Adressbuchs.</span><span class="sxs-lookup"><span data-stu-id="01129-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access the hierarchy table of the MAPI address book.</span></span> 
    
 <span data-ttu-id="01129-118">**Zugriff auf den standardmäßigen Nachrichtenspeicher Hierarchie-Tabelle**</span><span class="sxs-lookup"><span data-stu-id="01129-118">**To access the default message store's hierarchy table**</span></span>
  
1. <span data-ttu-id="01129-119">Rufen Sie [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) Zugriff auf die Tabelle Store.</span><span class="sxs-lookup"><span data-stu-id="01129-119">Call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to access the message store table.</span></span> 
    
2. <span data-ttu-id="01129-120">Erstellen Sie eine Einschränkung mithilfe der [SPropertyRestriction](spropertyrestriction.md) -Struktur die Tabelle, um nur die Zeilen zu begrenzen, die eine **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))-Eigenschaft auf TRUE festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="01129-120">Build a restriction using the [SPropertyRestriction](spropertyrestriction.md) structure to limit the table to only those rows that have a **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property set to TRUE.</span></span> 
    
3. <span data-ttu-id="01129-121">Rufen Sie [IMAPITable](imapitable-findrow.md), übergeben sie die **SPropertyRestriction**, um zu suchen, die Standard-Informationsspeicher darstellt.</span><span class="sxs-lookup"><span data-stu-id="01129-121">Call [IMAPITable::FindRow](imapitable-findrow.md), passing it the **SPropertyRestriction**, to locate the row representing the default message store.</span></span> 
    
4. <span data-ttu-id="01129-122">Rufen Sie [IMAPISession::OpenEntry](imapisession-openentry.md), aus der Standard-Nachrichtenspeicher Zeile in der Nachricht Store-Tabelle in der Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) übergeben.</span><span class="sxs-lookup"><span data-stu-id="01129-122">Call [IMAPISession::OpenEntry](imapisession-openentry.md), passing in the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property from the default message store's row in the message store table.</span></span>
    
5. <span data-ttu-id="01129-123">Rufen Sie den Nachrichtenspeicher [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der Eigenschaft **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="01129-123">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
6. <span data-ttu-id="01129-124">Rufen Sie den Nachrichtenspeicher [IMsgStore::OpenEntry](imsgstore-openentry.md) -Methode übergeben die **PR_IPM_SUBTREE_ENTRYID** -Eigenschaft, um den Stammordner der Nachrichtenspeicher IPM-Unterstruktur zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="01129-124">Call the message store's [IMsgStore::OpenEntry](imsgstore-openentry.md) method, passing the **PR_IPM_SUBTREE_ENTRYID** property, to open the root folder of the message store's IPM subtree.</span></span> 
    
7. <span data-ttu-id="01129-125">Rufen Sie den Stammordner IPM [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) -Methode zum Zugriff auf die Hierarchietabelle.</span><span class="sxs-lookup"><span data-stu-id="01129-125">Call the IPM root folder's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access its hierarchy table.</span></span> 
    

