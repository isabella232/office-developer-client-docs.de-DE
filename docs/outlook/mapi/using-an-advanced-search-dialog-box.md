---
title: Verwenden eines Dialogfelds für die erweiterte Suche
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
# <a name="using-an-advanced-search-dialog-box"></a><span data-ttu-id="333b2-103">Verwenden eines Dialogfelds für die erweiterte Suche</span><span class="sxs-lookup"><span data-stu-id="333b2-103">Using an Advanced Search Dialog Box</span></span>

  
  
<span data-ttu-id="333b2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="333b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="333b2-105">Einige Adressbuchcontainer unterstützen eine erweiterte Suchfunktion, mit der Clients nach anderen Eigenschaften als PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) suchen können.</span><span class="sxs-lookup"><span data-stu-id="333b2-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="333b2-106">Adressbuchcontainer, die erweiterte Suchen unterstützen, verfügen über eine Containerobjekteigenschaft namens **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="333b2-106">Address book containers that support advanced searches have a container object property called **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span></span> <span data-ttu-id="333b2-107">Dieses Containerobjekt bietet Zugriff auf eine Anzeigetabelle, die das Suchdialogfeld beschreibt – ein Dialogfeld, das zum Eingeben und Bearbeiten der erweiterten Suchkriterien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="333b2-107">This container object provides access to a display table that describes the search dialog box — a dialog box used to enter and edit the advanced search criteria.</span></span>
  
 <span data-ttu-id="333b2-108">**So führen Sie eine erweiterte Suche in einem Adressbuchcontainer aus**</span><span class="sxs-lookup"><span data-stu-id="333b2-108">**To perform an advanced search on an address book container**</span></span>
  
1. <span data-ttu-id="333b2-109">Rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md)  des Containers auf, und geben PR_SEARCH für das Eigenschaftstag und IID_IMAPIContainer für die Schnittstellen-ID an.</span><span class="sxs-lookup"><span data-stu-id="333b2-109">Call the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, specifying **PR_SEARCH** for the property tag and IID_IMAPIContainer for the interface identifier.</span></span> 
    
2. <span data-ttu-id="333b2-110">Rufen Sie die **IMAPIProp::OpenProperty-Methode** des Suchobjekts auf, und geben Sie **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) für das Eigenschaftstag und IID_IMAPITable für den Schnittstellenbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="333b2-110">Call the search object 's **IMAPIProp::OpenProperty** method, specifying **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> 
    
3. <span data-ttu-id="333b2-111">Rufen Sie die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) des Suchobjekts auf, um Werte für die Eigenschaften zu erstellen, die in der erweiterten Suche verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="333b2-111">Call the search object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to establish values for the properties to be used in the advanced search.</span></span> 
    
4. <span data-ttu-id="333b2-112">Rufen Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) des Suchobjekts auf, um die erweiterten Suchkriterien zu speichern.</span><span class="sxs-lookup"><span data-stu-id="333b2-112">Call the search object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the advanced search criteria.</span></span> 
    
<span data-ttu-id="333b2-113">Diese Abfolge von Aufrufen führt dazu, dass eine Einschränkung verfügbar ist, wenn ein Client die **GetSearchCriteria-Methode des Suchobjekts** aufruft.</span><span class="sxs-lookup"><span data-stu-id="333b2-113">This sequence of calls results in a restriction being available when a client calls the search object's **GetSearchCriteria** method.</span></span> 
  

