---
title: Schreiben einer Hierarchieanzeige
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5f6ebd20afc3b8d029fa7c632c55982862664055
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421130"
---
# <a name="writing-a-hierarchy-viewer"></a><span data-ttu-id="9324b-103">Schreiben einer Hierarchieanzeige</span><span class="sxs-lookup"><span data-stu-id="9324b-103">Writing a Hierarchy Viewer</span></span>

  
  
<span data-ttu-id="9324b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9324b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9324b-105">Ein Hierarchieanzeiger ist eine Benutzeroberflächenkomponente, die zum Anzeigen von Ordner- und Adressbuchcontainerhierarchietabellen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9324b-105">A hierarchy viewer is a user interface component that is used for displaying folder and address book container hierarchy tables.</span></span> <span data-ttu-id="9324b-106">Hierarchieanzeiger können Elemente der Hierarchie auf unterschiedlichen Ebenen anzeigen und jede Ebene bei Bedarf erweitern und verdingen.</span><span class="sxs-lookup"><span data-stu-id="9324b-106">Hierarchy viewers can display members of the hierarchy at different levels, expanding and contracting each level on demand.</span></span>
  
<span data-ttu-id="9324b-107">Die Containereigenschaft **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) steuert die Ebene, auf der ein Hierarchiemitglied angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9324b-107">The container property, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controls the level at which a hierarchy member is displayed.</span></span> <span data-ttu-id="9324b-108">Einträge, die Adressbuchcontainer oder Ordner der obersten Ebene darstellen, **PR_DEPTH** auf Null festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9324b-108">Entries that represent top-level address book containers or folders have their **PR_DEPTH** property set to zero.</span></span> <span data-ttu-id="9324b-109">Der Wert dieser Eigenschaft wird sequenziell für Einträge in sequenziellen Ebenen erhöht.</span><span class="sxs-lookup"><span data-stu-id="9324b-109">The value of this property is incremented sequentially for entries in sequential levels.</span></span> <span data-ttu-id="9324b-110">Wenn ein Benutzer also einen zu erweiternden Container auf **oberster** Ebene auswählt, werden alle Container mit PR_DEPTH 1 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9324b-110">That is, when a user selects a top-level container to expand, display all containers with **PR_DEPTH** set to 1.</span></span> <span data-ttu-id="9324b-111">Wenn ein Benutzer einen dieser Untercontainer erweitert,  zeigen Sie die Container mit PR_DEPTH 2 an, und so weiter.</span><span class="sxs-lookup"><span data-stu-id="9324b-111">When a user expands one of these subcontainers, display the containers with **PR_DEPTH** set to 2, and so on.</span></span> 
  
<span data-ttu-id="9324b-112">Hierarchieanzeigen unterstützen einen anderen Tiefenbereich.</span><span class="sxs-lookup"><span data-stu-id="9324b-112">Hierarchy viewers support a different range of depths.</span></span> <span data-ttu-id="9324b-113">Sie können den Viewer auf nur eine oder zwei Ebenen beschränken oder mehrere Ebenen unterstützen, wenn das Anzeigen einer umfangreichen Hierarchie eine Priorität hat.</span><span class="sxs-lookup"><span data-stu-id="9324b-113">You can limit your viewer to only one or two levels or you can support multiple levels, if displaying an expansive hierarchy is a priority.</span></span> 
  
<span data-ttu-id="9324b-114">Das Adressbuch bietet eine Hierarchieanzeige für die Container auf oberster Ebene im Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="9324b-114">The address book provides a hierarchy viewer for the top-level containers in the address book.</span></span> 
  
 <span data-ttu-id="9324b-115">**So greifen Sie auf die Adressbuchhierarchietabelle zu**</span><span class="sxs-lookup"><span data-stu-id="9324b-115">**To access the address book hierarchy table**</span></span>
  
1. <span data-ttu-id="9324b-116">Rufen [Sie IAddrBook::OpenEntry](iaddrbook-openentry.md)auf, und übergeben Sie einen Nulleintragsbezeichner, um den Stammcontainer des Adressbuchs zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9324b-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing a null entry identifier, to open the address book's root container.</span></span>
    
2. <span data-ttu-id="9324b-117">Rufen Sie die [IMAPIContainer::GetHierarchyTable-Methode](imapicontainer-gethierarchytable.md) des Stammcontainers auf, um auf die Hierarchietabelle des MAPI-Adressbuchs zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="9324b-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access the hierarchy table of the MAPI address book.</span></span> 
    
 <span data-ttu-id="9324b-118">**So greifen Sie auf die Hierarchietabelle des Standardnachrichtenspeichers zu**</span><span class="sxs-lookup"><span data-stu-id="9324b-118">**To access the default message store's hierarchy table**</span></span>
  
1. <span data-ttu-id="9324b-119">Rufen [Sie IMAPISession::GetMsgStoresTable auf,](imapisession-getmsgstorestable.md) um auf die Nachrichtenspeichertabelle zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="9324b-119">Call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to access the message store table.</span></span> 
    
2. <span data-ttu-id="9324b-120">Erstellen Sie eine Einschränkung mithilfe der [SPropertyRestriction-Struktur,](spropertyrestriction.md) um die Tabelle auf die Zeilen zu beschränken, für die **eine PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) -Eigenschaft auf TRUE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9324b-120">Build a restriction using the [SPropertyRestriction](spropertyrestriction.md) structure to limit the table to only those rows that have a **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property set to TRUE.</span></span> 
    
3. <span data-ttu-id="9324b-121">Rufen [Sie IMAPITable::FindRow](imapitable-findrow.md)auf, und übergeben Sie ihn an **die SPropertyRestriction,** um die Zeile zu finden, die den Standardnachrichtenspeicher darstellt.</span><span class="sxs-lookup"><span data-stu-id="9324b-121">Call [IMAPITable::FindRow](imapitable-findrow.md), passing it the **SPropertyRestriction**, to locate the row representing the default message store.</span></span> 
    
4. <span data-ttu-id="9324b-122">Rufen [Sie IMAPISession::OpenEntry](imapisession-openentry.md)auf, und übergeben Sie die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft aus der Zeile des Standardnachrichtenspeichers in der Nachrichtenspeichertabelle.</span><span class="sxs-lookup"><span data-stu-id="9324b-122">Call [IMAPISession::OpenEntry](imapisession-openentry.md), passing in the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property from the default message store's row in the message store table.</span></span>
    
5. <span data-ttu-id="9324b-123">Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des **Nachrichtenspeichers** auf, um die PR_IPM_SUBTREE_ENTRYID ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) -Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9324b-123">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
6. <span data-ttu-id="9324b-124">Rufen Sie die [IMsgStore::OpenEntry-Methode](imsgstore-openentry.md) des Nachrichtenspeichers auf, und übergeben Sie die **PR_IPM_SUBTREE_ENTRYID-Eigenschaft,** um den Stammordner der IPM-Unterstruktur des Nachrichtenspeichers zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9324b-124">Call the message store's [IMsgStore::OpenEntry](imsgstore-openentry.md) method, passing the **PR_IPM_SUBTREE_ENTRYID** property, to open the root folder of the message store's IPM subtree.</span></span> 
    
7. <span data-ttu-id="9324b-125">Rufen Sie die [IMAPIContainer::GetHierarchyTable-Methode](imapicontainer-gethierarchytable.md) des IPM-Stammordners auf, um auf die Hierarchietabelle zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="9324b-125">Call the IPM root folder's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access its hierarchy table.</span></span> 
    

