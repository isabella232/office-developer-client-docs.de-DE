---
title: Verwenden eines Dialogfelds für die erweiterte Suche.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 581607e184d67413e735c4cbfb874643b3222a80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588769"
---
# <a name="using-an-advanced-search-dialog-box"></a><span data-ttu-id="38925-103">Verwenden eines Dialogfelds für die erweiterte Suche.</span><span class="sxs-lookup"><span data-stu-id="38925-103">Using an Advanced Search Dialog Box</span></span>

  
  
<span data-ttu-id="38925-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38925-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38925-105">Einige Address Book Container unterstützt eine erweiterte Suchfunktionen, mit der Clients auf andere Eigenschaften als **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) durchsuchen kann.</span><span class="sxs-lookup"><span data-stu-id="38925-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="38925-106">Address Book Container, die erweiterte Suchvorgänge unterstützen, verfügen über die Container-Objekteigenschaft **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="38925-106">Address book containers that support advanced searches have a container object property called **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span></span> <span data-ttu-id="38925-107">Diese Container-Objekt ermöglicht den Zugriff auf eine zeigt die Tabelle, die das Dialogfeld Suchen beschreibt – ein Dialogfeld zum eingeben und bearbeiten die Kriterien für die erweiterte Suche verwendet.</span><span class="sxs-lookup"><span data-stu-id="38925-107">This container object provides access to a display table that describes the search dialog box — a dialog box used to enter and edit the advanced search criteria.</span></span>
  
 <span data-ttu-id="38925-108">**Zum Ausführen einer erweiterten Suche auf eine Adressbuchcontainer**</span><span class="sxs-lookup"><span data-stu-id="38925-108">**To perform an advanced search on an address book container**</span></span>
  
1. <span data-ttu-id="38925-109">Rufen Sie den Container [IMAPIProp::OpenProperty](imapiprop-openproperty.md) Methode **PR_SEARCH** für die Eigenschaftentag und IID_IMAPIContainer für den Schnittstellenbezeichner angeben.</span><span class="sxs-lookup"><span data-stu-id="38925-109">Call the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, specifying **PR_SEARCH** for the property tag and IID_IMAPIContainer for the interface identifier.</span></span> 
    
2. <span data-ttu-id="38925-110">Rufen Sie das Search-Objekt **IMAPIProp::OpenProperty** Methode **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) für die Eigenschaftentag und IID_IMAPITable für den Schnittstellenbezeichner angeben.</span><span class="sxs-lookup"><span data-stu-id="38925-110">Call the search object 's **IMAPIProp::OpenProperty** method, specifying **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> 
    
3. <span data-ttu-id="38925-111">Rufen Sie das Search-Objekt [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode zum Festlegen der Werte für die Eigenschaften in die erweiterte Suche verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38925-111">Call the search object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to establish values for the properties to be used in the advanced search.</span></span> 
    
4. <span data-ttu-id="38925-112">Rufen Sie das Search-Objekt [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, um die Kriterien für die erweiterte Suche zu speichern.</span><span class="sxs-lookup"><span data-stu-id="38925-112">Call the search object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the advanced search criteria.</span></span> 
    
<span data-ttu-id="38925-113">Diese Folge der Aufrufe führt eine Einschränkung nicht verfügbar sein, wenn ein Client das Search-Objekt **GetSearchCriteria** -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="38925-113">This sequence of calls results in a restriction being available when a client calls the search object's **GetSearchCriteria** method.</span></span> 
  

