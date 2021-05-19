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
ms.openlocfilehash: 38063cebe70b153decce6713ac5fc31d6916dbf6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426674"
---
# <a name="retrieving-recipient-properties"></a><span data-ttu-id="e4ee0-103">Abrufen von Empfängereigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4ee0-103">Retrieving recipient properties</span></span>
  
<span data-ttu-id="e4ee0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4ee0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a><span data-ttu-id="e4ee0-105">So greifen Sie auf eine oder mehrere Eigenschaften eines Adressbucheintrags zu</span><span class="sxs-lookup"><span data-stu-id="e4ee0-105">To access one or more properties of an address book entry</span></span>
  
1. <span data-ttu-id="e4ee0-106">Rufen Sie für jeden adressbucheintrag von Interesse [IAddrBook::OpenEntry](iaddrbook-openentry.md)auf, und übergeben Sie die Eintrags-ID des Zielnachrichtenbenutzers oder der Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="e4ee0-106">For each address book entry of interest, call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing the entry identifier of the target messaging user or distribution list.</span></span>
    
2. <span data-ttu-id="e4ee0-107">Gehen Sie dann wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="e4ee0-107">Then do one of the following:</span></span>
    
   - <span data-ttu-id="e4ee0-108">Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Messagingbenutzers oder der Verteilerliste für jeden interessierten Adressbucheintrag mit einer Liste der abzurufenden Eigenschaften auf.</span><span class="sxs-lookup"><span data-stu-id="e4ee0-108">Call the messaging user or distribution list's [IMAPIProp::GetProps](imapiprop-getprops.md) method for each address book entry of interest, with a list of the one or more properties to retrieve.</span></span> 
    
   - <span data-ttu-id="e4ee0-109">Rufen [Sie IAddrBook::P repareRecips](iaddrbook-preparerecips.md)auf, und übergeben Sie eine [ADRLIST-Struktur,](adrlist.md) die alle Eigenschaften für alle gewünschten Adressbucheinträge enthält.</span><span class="sxs-lookup"><span data-stu-id="e4ee0-109">Call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), passing an [ADRLIST](adrlist.md) structure that holds all of the properties for all of the desired address book entries.</span></span> <span data-ttu-id="e4ee0-110">Da ein Aufruf **von PrepareRecips** Informationen für mehrere Adressbucheinträge zurückgeben kann, ist dies die bevorzugte Strategie, wenn Sie an mehreren Empfängern interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="e4ee0-110">Because one call to **PrepareRecips** can return information for multiple address book entries, it is the preferable strategy when you are interested in more than one recipient.</span></span> 
    

