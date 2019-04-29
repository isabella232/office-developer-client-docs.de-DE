---
title: Schreiben eines Hierarchie-Viewers
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
# <a name="writing-a-hierarchy-viewer"></a><span data-ttu-id="f7534-103">Schreiben eines Hierarchie-Viewers</span><span class="sxs-lookup"><span data-stu-id="f7534-103">Writing a Hierarchy Viewer</span></span>

  
  
<span data-ttu-id="f7534-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7534-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7534-105">Eine Hierarchieanzeige ist eine Benutzeroberflächenkomponente, die zum Anzeigen von Ordner-und Adressbuchcontainer-Hierarchietabellen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f7534-105">A hierarchy viewer is a user interface component that is used for displaying folder and address book container hierarchy tables.</span></span> <span data-ttu-id="f7534-106">Hierarchie Betrachter können die Mitglieder der Hierarchie auf verschiedenen Ebenen anzeigen, wobei jede Ebene bei Bedarf erweitert und abgezogen wird.</span><span class="sxs-lookup"><span data-stu-id="f7534-106">Hierarchy viewers can display members of the hierarchy at different levels, expanding and contracting each level on demand.</span></span>
  
<span data-ttu-id="f7534-107">Die Container-Eigenschaft, **PR_DEPTH** ([pidtagdepth (](pidtagdepth-canonical-property.md)), steuert die Ebene, auf der ein Hierarchieelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f7534-107">The container property, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controls the level at which a hierarchy member is displayed.</span></span> <span data-ttu-id="f7534-108">Einträge, die Adressbuchcontainer oder-Ordner der obersten Ebene darstellen, haben Ihre **PR_DEPTH** -Eigenschaft auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f7534-108">Entries that represent top-level address book containers or folders have their **PR_DEPTH** property set to zero.</span></span> <span data-ttu-id="f7534-109">Der Wert dieser Eigenschaft wird für Einträge in sequenziellen Ebenen sequenziell erhöht.</span><span class="sxs-lookup"><span data-stu-id="f7534-109">The value of this property is incremented sequentially for entries in sequential levels.</span></span> <span data-ttu-id="f7534-110">Wenn ein Benutzer also einen Container der obersten Ebene auswählt, der erweitert werden soll, zeigen Sie alle Container mit **PR_DEPTH** auf 1 festgelegt an.</span><span class="sxs-lookup"><span data-stu-id="f7534-110">That is, when a user selects a top-level container to expand, display all containers with **PR_DEPTH** set to 1.</span></span> <span data-ttu-id="f7534-111">Wenn ein Benutzer einen dieser Untercontainer erweitert, zeigen Sie die Container mit **PR_DEPTH** auf 2 und so weiter an.</span><span class="sxs-lookup"><span data-stu-id="f7534-111">When a user expands one of these subcontainers, display the containers with **PR_DEPTH** set to 2, and so on.</span></span> 
  
<span data-ttu-id="f7534-112">Hierarchie Betrachter unterstützen einen unterschiedlichen Tiefen Umfang.</span><span class="sxs-lookup"><span data-stu-id="f7534-112">Hierarchy viewers support a different range of depths.</span></span> <span data-ttu-id="f7534-113">Sie können Ihren Viewer auf eine oder zwei Ebenen beschränken, oder Sie können mehrere Ebenen unterstützen, wenn eine expansive Hierarchie eine Priorität darstellt.</span><span class="sxs-lookup"><span data-stu-id="f7534-113">You can limit your viewer to only one or two levels or you can support multiple levels, if displaying an expansive hierarchy is a priority.</span></span> 
  
<span data-ttu-id="f7534-114">Das Adressbuch bietet einen Hierarchie Viewer für die Container der obersten Ebene im Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="f7534-114">The address book provides a hierarchy viewer for the top-level containers in the address book.</span></span> 
  
 <span data-ttu-id="f7534-115">**So greifen Sie auf die Adressbuch-Hierarchietabelle zu**</span><span class="sxs-lookup"><span data-stu-id="f7534-115">**To access the address book hierarchy table**</span></span>
  
1. <span data-ttu-id="f7534-116">Rufen Sie [IAddrBook:: OpenEntry](iaddrbook-openentry.md)auf, und übergeben Sie einen NULL-Eintragsbezeichner, um den Stammcontainer des Adressbuchs zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f7534-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing a null entry identifier, to open the address book's root container.</span></span>
    
2. <span data-ttu-id="f7534-117">Rufen Sie die [IMAPIContainer:: gethierarchyid](imapicontainer-gethierarchytable.md) -Methode des Stammcontainers auf, um auf die Hierarchietabelle des MAPI-Adressbuchs zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="f7534-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access the hierarchy table of the MAPI address book.</span></span> 
    
 <span data-ttu-id="f7534-118">**So greifen Sie auf die Hierarchietabelle des Standardnachrichten Speichers zu**</span><span class="sxs-lookup"><span data-stu-id="f7534-118">**To access the default message store's hierarchy table**</span></span>
  
1. <span data-ttu-id="f7534-119">Rufen Sie [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) auf, um auf die Nachrichtenspeichertabelle zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="f7534-119">Call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to access the message store table.</span></span> 
    
2. <span data-ttu-id="f7534-120">Erstellen Sie eine Einschränkung mithilfe der [SPropertyRestriction](spropertyrestriction.md) -Struktur, um die Tabelle auf die Zeilen einzuschränken, deren **PR_DEFAULT_STORE** ([PIDTAGDEFAULTSTORE (](pidtagdefaultstore-canonical-property.md))-Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f7534-120">Build a restriction using the [SPropertyRestriction](spropertyrestriction.md) structure to limit the table to only those rows that have a **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property set to TRUE.</span></span> 
    
3. <span data-ttu-id="f7534-121">Rufen Sie [IMAPITable:: FindRow](imapitable-findrow.md), und übergeben Sie die **SPropertyRestriction**, um die Zeile zu finden, die den Standardnachrichtenspeicher darstellt.</span><span class="sxs-lookup"><span data-stu-id="f7534-121">Call [IMAPITable::FindRow](imapitable-findrow.md), passing it the **SPropertyRestriction**, to locate the row representing the default message store.</span></span> 
    
4. <span data-ttu-id="f7534-122">Rufen Sie [IMAPISession:: OpenEntry](imapisession-openentry.md)auf, und übergeben Sie die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft aus der Zeile des Standardnachrichten Speichers in der Nachrichtenspeichertabelle.</span><span class="sxs-lookup"><span data-stu-id="f7534-122">Call [IMAPISession::OpenEntry](imapisession-openentry.md), passing in the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property from the default message store's row in the message store table.</span></span>
    
5. <span data-ttu-id="f7534-123">Rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Nachrichtenspeichers auf, um die **PR_IPM_SUBTREE_ENTRYID** ([pidtagipmsubtreeentryid (](pidtagipmsubtreeentryid-canonical-property.md))-Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f7534-123">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
6. <span data-ttu-id="f7534-124">Rufen Sie die [IMsgStore:: OpenEntry](imsgstore-openentry.md) -Methode des Nachrichtenspeichers auf, und übergeben Sie die **PR_IPM_SUBTREE_ENTRYID** -Eigenschaft, um den Stammordner der IPM-Unterstruktur des Nachrichtenspeichers zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f7534-124">Call the message store's [IMsgStore::OpenEntry](imsgstore-openentry.md) method, passing the **PR_IPM_SUBTREE_ENTRYID** property, to open the root folder of the message store's IPM subtree.</span></span> 
    
7. <span data-ttu-id="f7534-125">Rufen Sie die [IMAPIContainer:: gethierarchyid](imapicontainer-gethierarchytable.md) -Methode des IPM-Stammordners auf, um auf die Hierarchietabelle zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="f7534-125">Call the IPM root folder's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access its hierarchy table.</span></span> 
    

