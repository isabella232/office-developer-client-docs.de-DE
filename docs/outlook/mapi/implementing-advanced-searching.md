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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407389"
---
# <a name="implementing-advanced-searching"></a><span data-ttu-id="5f446-103">Implementieren der erweiterten Suche</span><span class="sxs-lookup"><span data-stu-id="5f446-103">Implementing Advanced Searching</span></span>

  
  
<span data-ttu-id="5f446-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f446-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f446-105">Einige Adressbuchcontainer unterstützen eine erweiterte Suchfunktion, mit der Clients nach anderen Eigenschaften als PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) suchen können.</span><span class="sxs-lookup"><span data-stu-id="5f446-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="5f446-106">Um erweiterte Suchen zu unterstützen, muss Ihr Anbieter einen speziellen Container implementieren, auf den über die **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md))-Eigenschaft Ihrer anderen Container zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="5f446-106">To support advanced searches, your provider must implement a special container that is accessible through the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property of your other containers.</span></span> <span data-ttu-id="5f446-107">**PR_SEARCH** enthält ein Containerobjekt, das Zugriff auf eine Anzeigetabelle bietet, in der das Dialogfeld zum Eingeben und Bearbeiten der erweiterten Suchkriterien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="5f446-107">**PR_SEARCH** contains a container object that provides access to a display table that describes the dialog box used to enter and edit the advanced search criteria.</span></span> 
  
 <span data-ttu-id="5f446-108">**So unterstützen Sie die erweiterte Suche**</span><span class="sxs-lookup"><span data-stu-id="5f446-108">**To support advanced searching**</span></span>
  
1. <span data-ttu-id="5f446-109">Definieren Sie eine Eigenschaft für jedes Suchkriterium.</span><span class="sxs-lookup"><span data-stu-id="5f446-109">Define a property for each of your search criteria.</span></span>
    
2. <span data-ttu-id="5f446-110">Im Codeabschnitt in der [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) Ihres Containers, die die PR_SEARCH **behandelt:**</span><span class="sxs-lookup"><span data-stu-id="5f446-110">In the section of code in your container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method that handles the **PR_SEARCH** property:</span></span> 
    
1. <span data-ttu-id="5f446-111">Überprüfen Sie, ob der Client die **IMAPIContainer-Schnittstelle** anfordert.</span><span class="sxs-lookup"><span data-stu-id="5f446-111">Check that the client is requesting the **IMAPIContainer** interface.</span></span> <span data-ttu-id="5f446-112">Wenn eine unangemessene Schnittstelle angefordert wird, führen Sie einen Fehler aus, und geben Sie MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="5f446-112">If an inappropriate interface is being requested, fail and return MAPI_E_INTERFACE_NOT_SUPPORTED.</span></span> 
    
2. <span data-ttu-id="5f446-113">Erstellen Sie ein neues Suchobjekt, das die **IMAPIContainer-Schnittstelle** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5f446-113">Create a new search object that supports the **IMAPIContainer** interface.</span></span> 
    
3. <span data-ttu-id="5f446-114">An diesem Punkt wird die **IMAPIProp::OpenProperty-Methode** des Suchcontainers aufgerufen, um die **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) -Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5f446-114">At this point, a call will be made to your search container's **IMAPIProp::OpenProperty** method to retrieve its **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="5f446-115">Ihr Anbieter muss eine Anzeigetabelle liefern, in der Regel über einen Aufruf von [BuildDisplayTable,](builddisplaytable.md)in der das dialogfeld erweiterte Suche des Containers beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="5f446-115">Your provider must supply a display table, typically through a call to [BuildDisplayTable](builddisplaytable.md), that describes the container's advanced search dialog box.</span></span>
    
4. <span data-ttu-id="5f446-116">MAPI zeigt das Suchdialogfeld an, sodass der Benutzer die entsprechenden Kriterien eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="5f446-116">MAPI displays the search dialog box, allowing the user to enter the appropriate criteria.</span></span> <span data-ttu-id="5f446-117">Wenn der Benutzer fertig ist, ruft MAPI die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) des Containers auf, um die Suchkriterien zu speichern.</span><span class="sxs-lookup"><span data-stu-id="5f446-117">When the user has finished, MAPI calls the container's [IMAPIProp::SetProps](imapiprop-setprops.md) method to store the search criteria.</span></span> 
    
5. <span data-ttu-id="5f446-118">Es wird ein Aufruf zum Anfordern des Inhaltsverzeichnisses des Suchcontainers vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="5f446-118">A call will be made to request your search container's contents table.</span></span> <span data-ttu-id="5f446-119">Füllen Sie die Inhaltstabelle mit allen Einträgen im Container auf, die den Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5f446-119">Populate the contents table with all of the entries in the container that match the criteria.</span></span>
    

