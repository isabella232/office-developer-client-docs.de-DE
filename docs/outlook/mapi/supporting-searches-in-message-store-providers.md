---
title: Unterstützen von Suchdiensten in Store Anbietern
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
# <a name="supporting-searches-in-message-store-providers"></a><span data-ttu-id="d462e-103">Unterstützen von Suchdiensten in Store Anbietern</span><span class="sxs-lookup"><span data-stu-id="d462e-103">Supporting Searches in Message Store Providers</span></span>

  
  
<span data-ttu-id="d462e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d462e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d462e-105">Clientanwendungen verfügen häufig über einige Benutzeroberflächenkomponenten, die für die Suche nach Nachrichten in einem Nachrichtenspeicher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d462e-105">Client applications frequently have some user interface components devoted to searching for messages in a message store.</span></span> <span data-ttu-id="d462e-106">Suchkriterien werden in der [IMAPIContainer : IMAPIProp-Schnittstelle](imapicontainerimapiprop.md) mit den [Methoden IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) und [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="d462e-106">Search criteria are specified in the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) interface by means of the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) and [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) methods.</span></span> 
  
<span data-ttu-id="d462e-107">Clients verwenden die PR_FINDER_ENTRYID **(** [PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) -Eigenschaft des Nachrichtenspeicherobjekts, um den Stammordner im Nachrichtenspeicher zu identifizieren, der Ordner für Suchergebnisse enthält.</span><span class="sxs-lookup"><span data-stu-id="d462e-107">Clients use the message store object's **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) property to identify the root folder in the message store that contains folders for search results.</span></span> <span data-ttu-id="d462e-108">Der Suchergebnisordner ist häufig ein Ordner auf oberster Ebene des Nachrichtenspeichers, der nicht Teil der IPM-Ordnerstruktur ist und daher ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="d462e-108">The search-results folder is often a folder at the top level of the message store that is not part of the IPM folder tree and is, therefore, hidden.</span></span>
  
<span data-ttu-id="d462e-109">Ob Ihr Nachrichtenspeicheranbieter einen permanenten Suchergebnisordner verwendet oder einen erstellt, wenn ein Client die in der **PR_FINDER_ENTRYID-Eigenschaft** gespeicherte Eintrags-ID öffnet, ist ein Implementierungsdetail.</span><span class="sxs-lookup"><span data-stu-id="d462e-109">Whether your message store provider uses a permanent search-results folder or creates one when a client opens the entry identifier stored in the **PR_FINDER_ENTRYID** property is an implementation detail.</span></span> <span data-ttu-id="d462e-110">Es ist für Ihren Nachrichtenspeicheranbieter etwas einfacher, einen permanenten Ordner zu verwenden, der beim Erstellen des Nachrichtenspeichers erstellt wird, da dadurch die Komplikation vermieden wird, die Eintrags-ID zu überprüfen, wenn ein Ordner geöffnet wird, um festzustellen, ob ein Suchergebnisordner erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d462e-110">It is somewhat easier for your message store provider to use a permanent folder that is created when the message store is created, because doing so avoids the complication of checking the entry identifier whenever any folder is opened to see whether to create a search-results folder.</span></span> <span data-ttu-id="d462e-111">Dies können jedoch nicht alle Nachrichtenspeicheranbieter tun. Insbesondere schreibgeschützte Nachrichtenspeicher oder -speicher, die eine MAPI-Schnittstelle für eine Ältere Datenbank bereitstellen, sind häufig nicht zulässig oder können keinen permanenten Suchergebnisordner im zugrunde liegenden Speichermechanismus erstellen.</span><span class="sxs-lookup"><span data-stu-id="d462e-111">However, not all message store providers can do that; notably, read-only message stores or stores that provide a MAPI interface to a legacy database often are not allowed or are unable to create a permanent search-results folder in the underlying storage mechanism.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d462e-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d462e-112">See also</span></span>



[<span data-ttu-id="d462e-113">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="d462e-113">Message Store Features</span></span>](message-store-features.md)

