---
title: Implementieren der erweiterten Suche
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 35d41ff903c5ed22c5210adf6448dfded0afe4b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332816"
---
# <a name="implementing-advanced-searching"></a><span data-ttu-id="d510f-103">Implementieren der erweiterten Suche</span><span class="sxs-lookup"><span data-stu-id="d510f-103">Implementing Advanced Searching</span></span>

  
  
<span data-ttu-id="d510f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d510f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d510f-105">Einige Adressbuchcontainer unterstützen eine erweiterte Suchfunktion, die es Clients ermöglicht, andere Eigenschaften als **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) zu suchen.</span><span class="sxs-lookup"><span data-stu-id="d510f-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="d510f-106">Zur Unterstützung erweiterter Suchvorgänge muss der Anbieter einen speziellen Container implementieren, auf den über die **PR_SEARCH** ([pidtagsearch (](pidtagsearch-canonical-property.md))-Eigenschaft der anderen Container zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="d510f-106">To support advanced searches, your provider must implement a special container that is accessible through the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property of your other containers.</span></span> <span data-ttu-id="d510f-107">**PR_SEARCH** enthält ein Container-Objekt, das Zugriff auf eine Anzeigetabelle bietet, in der das Dialogfeld beschrieben wird, das zum eingeben und Bearbeiten der erweiterten Suchkriterien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d510f-107">**PR_SEARCH** contains a container object that provides access to a display table that describes the dialog box used to enter and edit the advanced search criteria.</span></span> 
  
 <span data-ttu-id="d510f-108">**So unterstützen Sie die erweiterte Suche**</span><span class="sxs-lookup"><span data-stu-id="d510f-108">**To support advanced searching**</span></span>
  
1. <span data-ttu-id="d510f-109">Definieren Sie eine Eigenschaft für jedes Suchkriterium.</span><span class="sxs-lookup"><span data-stu-id="d510f-109">Define a property for each of your search criteria.</span></span>
    
2. <span data-ttu-id="d510f-110">Im Codeabschnitt in der [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode ihres Containers, die die **PR_SEARCH** -Eigenschaft behandelt:</span><span class="sxs-lookup"><span data-stu-id="d510f-110">In the section of code in your container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method that handles the **PR_SEARCH** property:</span></span> 
    
1. <span data-ttu-id="d510f-111">Überprüfen Sie, ob der Client die **IMAPIContainer** -Schnittstelle anfordert.</span><span class="sxs-lookup"><span data-stu-id="d510f-111">Check that the client is requesting the **IMAPIContainer** interface.</span></span> <span data-ttu-id="d510f-112">Wenn eine ungeeignete Schnittstelle angefordert wird, schlagen Sie fehl und geben MAPI_E_INTERFACE_NOT_SUPPORTED zurück.</span><span class="sxs-lookup"><span data-stu-id="d510f-112">If an inappropriate interface is being requested, fail and return MAPI_E_INTERFACE_NOT_SUPPORTED.</span></span> 
    
2. <span data-ttu-id="d510f-113">Erstellen Sie ein neues Search-Objekt, das die **IMAPIContainer** -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d510f-113">Create a new search object that supports the **IMAPIContainer** interface.</span></span> 
    
3. <span data-ttu-id="d510f-114">An dieser Stelle wird ein Aufruf an die **IMAPIProp:: OpenProperty** -Methode des Such Containers durchgeführt, um die **PR_DETAILS_TABLE** ([pidtagdetailstable (](pidtagdetailstable-canonical-property.md))-Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d510f-114">At this point, a call will be made to your search container's **IMAPIProp::OpenProperty** method to retrieve its **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="d510f-115">Der Anbieter muss eine Anzeigetabelle angeben, normalerweise durch einen Aufruf von [BuildDisplayTable](builddisplaytable.md), der das Dialogfeld Erweiterte Suche des Containers beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d510f-115">Your provider must supply a display table, typically through a call to [BuildDisplayTable](builddisplaytable.md), that describes the container's advanced search dialog box.</span></span>
    
4. <span data-ttu-id="d510f-116">MAPI zeigt das Dialogfeld Suchen an, in dem der Benutzer die entsprechenden Kriterien eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="d510f-116">MAPI displays the search dialog box, allowing the user to enter the appropriate criteria.</span></span> <span data-ttu-id="d510f-117">Wenn der Benutzer fertig ist, ruft MAPI die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode des Containers auf, um die Suchkriterien zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d510f-117">When the user has finished, MAPI calls the container's [IMAPIProp::SetProps](imapiprop-setprops.md) method to store the search criteria.</span></span> 
    
5. <span data-ttu-id="d510f-118">Es wird ein Anruf getätigt, um die Inhaltstabelle Ihres Such Containers anzufordern.</span><span class="sxs-lookup"><span data-stu-id="d510f-118">A call will be made to request your search container's contents table.</span></span> <span data-ttu-id="d510f-119">Füllen Sie die Tabelle Contents mit allen Einträgen im Container, die den Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d510f-119">Populate the contents table with all of the entries in the container that match the criteria.</span></span>
    

