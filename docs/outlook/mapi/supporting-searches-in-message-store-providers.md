---
title: Unterstützen von Suchvorgängen in Nachrichtenspeicher Anbietern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 545047e90346b0f8e4a88eabcb20573f663f6d02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425386"
---
# <a name="supporting-searches-in-message-store-providers"></a><span data-ttu-id="fce07-103">Unterstützen von Suchvorgängen in Nachrichtenspeicher Anbietern</span><span class="sxs-lookup"><span data-stu-id="fce07-103">Supporting Searches in Message Store Providers</span></span>

  
  
<span data-ttu-id="fce07-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fce07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fce07-105">Client Anwendungen verfügen häufig über einige Benutzeroberflächenkomponenten, die für die Suche nach Nachrichten in einem Nachrichtenspeicher vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="fce07-105">Client applications frequently have some user interface components devoted to searching for messages in a message store.</span></span> <span data-ttu-id="fce07-106">Suchkriterien werden in der [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) -Schnittstelle mithilfe der Methoden [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) und [IMAPIContainer:: GetSearchCriteria](imapicontainer-getsearchcriteria.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="fce07-106">Search criteria are specified in the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) interface by means of the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) and [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) methods.</span></span> 
  
<span data-ttu-id="fce07-107">Clients verwenden die **PR_FINDER_ENTRYID** ([pidtagfinderentryid (](pidtagfinderentryid-canonical-property.md))-Eigenschaft des Nachrichtenspeicher Objekts, um den Stammordner im Nachrichtenspeicher zu identifizieren, der Ordner für Suchergebnisse enthält.</span><span class="sxs-lookup"><span data-stu-id="fce07-107">Clients use the message store object's **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) property to identify the root folder in the message store that contains folders for search results.</span></span> <span data-ttu-id="fce07-108">Der Ordner Suchergebnisse ist häufig ein Ordner auf der obersten Ebene des Nachrichtenspeichers, der nicht Teil der IPM-Ordnerstruktur ist und daher ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="fce07-108">The search-results folder is often a folder at the top level of the message store that is not part of the IPM folder tree and is, therefore, hidden.</span></span>
  
<span data-ttu-id="fce07-109">Ob der Nachrichtenspeicher Anbieter einen permanenten Suchergebnisordner verwendet oder einen erstellt, wenn ein Client die in der **PR_FINDER_ENTRYID** -Eigenschaft gespeicherte Eintrags-ID ist ein Implementierungsdetail.</span><span class="sxs-lookup"><span data-stu-id="fce07-109">Whether your message store provider uses a permanent search-results folder or creates one when a client opens the entry identifier stored in the **PR_FINDER_ENTRYID** property is an implementation detail.</span></span> <span data-ttu-id="fce07-110">Es ist für den Nachrichtenspeicher Anbieter etwas einfacher, einen permanenten Ordner zu verwenden, der beim Erstellen des Nachrichtenspeichers erstellt wird, da dadurch die Komplikation beim Überprüfen der Eintrags-ID vermieden wird, wenn ein Ordner geöffnet wird, um zu sehen, ob ein Ordner Suchergebnisse.</span><span class="sxs-lookup"><span data-stu-id="fce07-110">It is somewhat easier for your message store provider to use a permanent folder that is created when the message store is created, because doing so avoids the complication of checking the entry identifier whenever any folder is opened to see whether to create a search-results folder.</span></span> <span data-ttu-id="fce07-111">Allerdings können nicht alle Nachrichtenspeicher Anbieter dies tun; insbesondere werden schreibgeschützte Nachrichtenspeicher oder-Speicher, die eine MAPI-Schnittstelle zu einer Legacydatenbank bereitstellen, häufig nicht zugelassen oder können keinen permanenten Suchergebnisordner im zugrunde liegenden Speichermechanismus erstellen.</span><span class="sxs-lookup"><span data-stu-id="fce07-111">However, not all message store providers can do that; notably, read-only message stores or stores that provide a MAPI interface to a legacy database often are not allowed or are unable to create a permanent search-results folder in the underlying storage mechanism.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fce07-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fce07-112">See also</span></span>



[<span data-ttu-id="fce07-113">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="fce07-113">Message Store Features</span></span>](message-store-features.md)

