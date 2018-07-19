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
ms.openlocfilehash: 4430b52b470b89bd7d81922b98b121b3a455768f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792550"
---
# <a name="implementing-advanced-searching"></a><span data-ttu-id="38159-103">Implementieren der erweiterten Suche</span><span class="sxs-lookup"><span data-stu-id="38159-103">Implementing Advanced Searching</span></span>

  
  
<span data-ttu-id="38159-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="38159-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38159-105">Einige Address Book Container unterstützt eine erweiterte Suchfunktionen, mit der Clients auf andere Eigenschaften als **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) durchsuchen kann.</span><span class="sxs-lookup"><span data-stu-id="38159-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="38159-106">Zur Unterstützung der erweiterten Suche muss vom Dienstanbieter ein speziellen Containers implementieren, das über die **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md))-Eigenschaft des Ihrer andere Container zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="38159-106">To support advanced searches, your provider must implement a special container that is accessible through the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property of your other containers.</span></span> <span data-ttu-id="38159-107">**PR_SEARCH** enthält ein Container-Objekt, das Zugriff auf eine Tabelle anzeigen bietet, die beschreibt das Dialogfeld zum eingeben und bearbeiten die Kriterien für die erweiterte Suche verwendet.</span><span class="sxs-lookup"><span data-stu-id="38159-107">**PR_SEARCH** contains a container object that provides access to a display table that describes the dialog box used to enter and edit the advanced search criteria.</span></span> 
  
 <span data-ttu-id="38159-108">**Zur Unterstützung der erweiterten Suche**</span><span class="sxs-lookup"><span data-stu-id="38159-108">**To support advanced searching**</span></span>
  
1. <span data-ttu-id="38159-109">Definieren Sie eine Eigenschaft für die einzelnen von den Suchkriterien.</span><span class="sxs-lookup"><span data-stu-id="38159-109">Define a property for each of your search criteria.</span></span>
    
2. <span data-ttu-id="38159-110">Im Abschnitt des Codes in den Container [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode, die **PR_SEARCH** -Eigenschaft behandelt:</span><span class="sxs-lookup"><span data-stu-id="38159-110">In the section of code in your container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method that handles the **PR_SEARCH** property:</span></span> 
    
1. <span data-ttu-id="38159-111">Überprüfen Sie, dass der Client die Schnittstelle **IMAPIContainer** anfordert.</span><span class="sxs-lookup"><span data-stu-id="38159-111">Check that the client is requesting the **IMAPIContainer** interface.</span></span> <span data-ttu-id="38159-112">Wenn eine ungeeignete-Schnittstelle angefordert wird, wird ein Fehler auftritt, und geben Sie MAPI_E_INTERFACE_NOT_SUPPORTED zurück.</span><span class="sxs-lookup"><span data-stu-id="38159-112">If an inappropriate interface is being requested, fail and return MAPI_E_INTERFACE_NOT_SUPPORTED.</span></span> 
    
2. <span data-ttu-id="38159-113">Erstellen Sie ein neues Search-Objekt, das die **IMAPIContainer** -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="38159-113">Create a new search object that supports the **IMAPIContainer** interface.</span></span> 
    
3. <span data-ttu-id="38159-114">Zu diesem Zeitpunkt wird Ihre Suche des Containers **IMAPIProp::OpenProperty** -Methode aufgerufen werden, dessen Eigenschaft **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="38159-114">At this point, a call will be made to your search container's **IMAPIProp::OpenProperty** method to retrieve its **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="38159-115">Vom Dienstanbieter muss eine zeigt die Tabelle, in der Regel durch einen Aufruf von [BuildDisplayTable](builddisplaytable.md), angeben, die Sie im Dialogfeld Erweiterte Suche der Container beschreibt.</span><span class="sxs-lookup"><span data-stu-id="38159-115">Your provider must supply a display table, typically through a call to [BuildDisplayTable](builddisplaytable.md), that describes the container's advanced search dialog box.</span></span>
    
4. <span data-ttu-id="38159-116">MAPI zeigt das Dialogfeld Suchen an, in dem der Benutzer die entsprechenden Kriterien einzugeben.</span><span class="sxs-lookup"><span data-stu-id="38159-116">MAPI displays the search dialog box, allowing the user to enter the appropriate criteria.</span></span> <span data-ttu-id="38159-117">Wenn der Benutzer beendet wurde, ruft MAPI des Containers [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode, um die Suchkriterien zu speichern.</span><span class="sxs-lookup"><span data-stu-id="38159-117">When the user has finished, MAPI calls the container's [IMAPIProp::SetProps](imapiprop-setprops.md) method to store the search criteria.</span></span> 
    
5. <span data-ttu-id="38159-118">Ein Anruf wird versucht, Ihre Suche des Containers Inhaltstabelle anfordern.</span><span class="sxs-lookup"><span data-stu-id="38159-118">A call will be made to request your search container's contents table.</span></span> <span data-ttu-id="38159-119">Füllen Sie auf Inhaltstabelle, indem Sie alle Einträge im Container, die mit den Kriterien übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="38159-119">Populate the contents table with all of the entries in the container that match the criteria.</span></span>
    

