---
title: Verwenden eines Dialog Felds für die erweiterte Suche
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 70b62eeaf6e737747c98b3abcd6e7053f71d4308
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437301"
---
# <a name="using-an-advanced-search-dialog-box"></a><span data-ttu-id="c688b-103">Verwenden eines Dialog Felds für die erweiterte Suche</span><span class="sxs-lookup"><span data-stu-id="c688b-103">Using an Advanced Search Dialog Box</span></span>

  
  
<span data-ttu-id="c688b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c688b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c688b-105">Einige Adressbuchcontainer unterstützen eine erweiterte Suchfunktion, die es Clients ermöglicht, andere Eigenschaften als **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c688b-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="c688b-106">Adressbuchcontainer, die erweiterte Suchvorgänge unterstützen, verfügen über eine Containerobjekt Eigenschaft namens **PR_SEARCH** ([pidtagsearch (](pidtagsearch-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c688b-106">Address book containers that support advanced searches have a container object property called **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span></span> <span data-ttu-id="c688b-107">Dieses Container-Objekt ermöglicht den Zugriff auf eine Anzeigetabelle, die das Dialogfeld Suchen beschreibt – ein Dialogfeld zum eingeben und Bearbeiten der erweiterten Suchkriterien.</span><span class="sxs-lookup"><span data-stu-id="c688b-107">This container object provides access to a display table that describes the search dialog box — a dialog box used to enter and edit the advanced search criteria.</span></span>
  
 <span data-ttu-id="c688b-108">**So führen Sie eine erweiterte Suche für einen Adressbuchcontainer aus**</span><span class="sxs-lookup"><span data-stu-id="c688b-108">**To perform an advanced search on an address book container**</span></span>
  
1. <span data-ttu-id="c688b-109">Rufen Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des Containers auf, und geben Sie **PR_SEARCH** für das Property-Tag und IID_IMAPIContainer für den Schnittstellenbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="c688b-109">Call the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, specifying **PR_SEARCH** for the property tag and IID_IMAPIContainer for the interface identifier.</span></span> 
    
2. <span data-ttu-id="c688b-110">Rufen Sie die **IMAPIProp:: OpenProperty** -Methode des Search-Objekts auf, und geben Sie **PR_DETAILS_TABLE** ([pidtagdetailstable (](pidtagdetailstable-canonical-property.md)) für das Property-Tag und IID_IMAPITable für den Schnittstellenbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="c688b-110">Call the search object 's **IMAPIProp::OpenProperty** method, specifying **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> 
    
3. <span data-ttu-id="c688b-111">Rufen Sie die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode des Search-Objekts auf, um Werte für die in der erweiterten Suche zu verwendenden Eigenschaften einzurichten.</span><span class="sxs-lookup"><span data-stu-id="c688b-111">Call the search object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to establish values for the properties to be used in the advanced search.</span></span> 
    
4. <span data-ttu-id="c688b-112">Rufen Sie die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode des Search-Objekts auf, um die erweiterten Suchkriterien zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c688b-112">Call the search object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the advanced search criteria.</span></span> 
    
<span data-ttu-id="c688b-113">Diese Sequenz von Aufrufen führt zu einer Einschränkung, die verfügbar ist, wenn ein Client die **GetSearchCriteria** -Methode des Search-Objekts aufruft.</span><span class="sxs-lookup"><span data-stu-id="c688b-113">This sequence of calls results in a restriction being available when a client calls the search object's **GetSearchCriteria** method.</span></span> 
  

