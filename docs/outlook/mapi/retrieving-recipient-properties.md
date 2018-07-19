---
title: Abrufen von Empfängereigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a7bdcf133b8b2b5d8eb906cc0f5b5803838e27a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795385"
---
# <a name="retrieving-recipient-properties"></a><span data-ttu-id="ca583-103">Abrufen von Empfängereigenschaften</span><span class="sxs-lookup"><span data-stu-id="ca583-103">Retrieving recipient properties</span></span>
  
<span data-ttu-id="ca583-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ca583-104">**Applies to**: Outlook</span></span> 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a><span data-ttu-id="ca583-105">Zugriff auf eine oder mehrere Eigenschaften eines Adresseintrags Adressbuch</span><span class="sxs-lookup"><span data-stu-id="ca583-105">To access one or more properties of an address book entry</span></span>
  
1. <span data-ttu-id="ca583-106">Rufen Sie für jeden Eintrag Address Book von Interesse [IAddrBook::OpenEntry](iaddrbook-openentry.md), übergeben die Eintrags-ID des Ziels messaging-Benutzer- oder Verteilerliste aus.</span><span class="sxs-lookup"><span data-stu-id="ca583-106">For each address book entry of interest, call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing the entry identifier of the target messaging user or distribution list.</span></span>
    
2. <span data-ttu-id="ca583-107">Klicken Sie dann einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="ca583-107">Then do one of the following:</span></span>
    
   - <span data-ttu-id="ca583-108">Rufen Sie für jeden Eintrag Adressbuch Adresse von Interesse, mit der eine oder mehrere Eigenschaften zum Abrufen einer Liste der messaging-Benutzer oder die Verteilerliste [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ca583-108">Call the messaging user or distribution list's [IMAPIProp::GetProps](imapiprop-getprops.md) method for each address book entry of interest, with a list of the one or more properties to retrieve.</span></span> 
    
   - <span data-ttu-id="ca583-109">Rufen Sie [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), übergeben eine [ADRLIST](adrlist.md) -Struktur, die alle Eigenschaften für alle gewünschten Adressbucheinträge enthält.</span><span class="sxs-lookup"><span data-stu-id="ca583-109">Call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), passing an [ADRLIST](adrlist.md) structure that holds all of the properties for all of the desired address book entries.</span></span> <span data-ttu-id="ca583-110">Da durch Aufrufen von **PrepareRecips** Informationen für mehrere Adresse Adressbucheinträge zurückgeben kann, ist die Strategie vorzuziehen, wenn Sie mehrere Empfänger interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="ca583-110">Because one call to **PrepareRecips** can return information for multiple address book entries, it is the preferable strategy when you are interested in more than one recipient.</span></span> 
    

