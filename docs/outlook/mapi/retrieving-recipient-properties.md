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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279594"
---
# <a name="retrieving-recipient-properties"></a><span data-ttu-id="919e6-103">Abrufen von Empfängereigenschaften</span><span class="sxs-lookup"><span data-stu-id="919e6-103">Retrieving recipient properties</span></span>
  
<span data-ttu-id="919e6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="919e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a><span data-ttu-id="919e6-105">So greifen Sie auf eine oder mehrere Eigenschaften eines Adressbucheintrags zu</span><span class="sxs-lookup"><span data-stu-id="919e6-105">To access one or more properties of an address book entry</span></span>
  
1. <span data-ttu-id="919e6-106">Rufen Sie für jeden gewünschten Adressbucheintrag [IAddrBook:: OpenEntry](iaddrbook-openentry.md)auf, und übergeben Sie dabei den Eintragsbezeichner des Ziel-Messaging Benutzers oder der Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="919e6-106">For each address book entry of interest, call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing the entry identifier of the target messaging user or distribution list.</span></span>
    
2. <span data-ttu-id="919e6-107">Führen Sie dann einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="919e6-107">Then do one of the following:</span></span>
    
   - <span data-ttu-id="919e6-108">Rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Messaging Benutzers oder der Verteilerliste für die einzelnen Adressbucheinträge auf, die eine Liste der Eigenschaften aufweisen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="919e6-108">Call the messaging user or distribution list's [IMAPIProp::GetProps](imapiprop-getprops.md) method for each address book entry of interest, with a list of the one or more properties to retrieve.</span></span> 
    
   - <span data-ttu-id="919e6-109">Rufen Sie [IAddrBook::P reparerecips](iaddrbook-preparerecips.md), und übergeben Sie eine [ADRLIST](adrlist.md) -Struktur, die alle Eigenschaften für alle gewünschten Adressbucheinträge enthält.</span><span class="sxs-lookup"><span data-stu-id="919e6-109">Call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), passing an [ADRLIST](adrlist.md) structure that holds all of the properties for all of the desired address book entries.</span></span> <span data-ttu-id="919e6-110">Da ein Aufruf von **PrepareRecips** Informationen für mehrere Adressbucheinträge zurückgeben kann, ist dies die bevorzugte Strategie, wenn Sie an mehreren Empfängern interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="919e6-110">Because one call to **PrepareRecips** can return information for multiple address book entries, it is the preferable strategy when you are interested in more than one recipient.</span></span> 
    

