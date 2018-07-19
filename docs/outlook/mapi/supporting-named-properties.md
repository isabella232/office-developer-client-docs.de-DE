---
title: Unterstützen von benannten Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 983cbaf4d3523bf1e5370e5ad3119ab8c1490f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795671"
---
# <a name="supporting-named-properties"></a><span data-ttu-id="c6621-103">Unterstützen von benannten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c6621-103">Supporting Named Properties</span></span>

  
  
<span data-ttu-id="c6621-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c6621-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c6621-105">Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties.</span><span class="sxs-lookup"><span data-stu-id="c6621-105">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties.</span></span> <span data-ttu-id="c6621-106">Unterstützung für benannte Eigenschaften ist für erforderlich:</span><span class="sxs-lookup"><span data-stu-id="c6621-106">Support for named properties is required for:</span></span> 
  
- <span data-ttu-id="c6621-107">Von adressbuchanbietern implementierte, mit denen Sie Einträge von anderen Anbietern in ihre Container kopiert werden können.</span><span class="sxs-lookup"><span data-stu-id="c6621-107">Address book providers that allow entries from other providers to be copied into their containers.</span></span>
    
- <span data-ttu-id="c6621-108">Nachrichtenspeicher Authentifizierungsanbieter an, die zum Erstellen von beliebigen Nachrichtentypen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c6621-108">Message store providers that can be used to create arbitrary message types.</span></span>
    
<span data-ttu-id="c6621-109">Unterstützung für benannte Eigenschaft ist optional für alle anderen Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="c6621-109">Named property support is optional for all other service providers.</span></span> <span data-ttu-id="c6621-110">Dienstanbieter, die Unterstützung für benannte Eigenschaften müssen Namensbezeichner-Zuordnung in den Methoden [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) und [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) implementieren.</span><span class="sxs-lookup"><span data-stu-id="c6621-110">Service providers that do support named properties must implement name-to-identifier mapping in the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span> <span data-ttu-id="c6621-111">Clients aufrufen **GetNamesFromIDs** zum Abrufen der entsprechenden Names für einen oder mehrere Eigenschaftenbezeichner im Bereich 0 x 8000 Failover und **GetIDsFromNames** entweder erstellen oder die Bezeichner für einen oder mehrere Namen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c6621-111">Clients call **GetNamesFromIDs** to retrieve the corresponding names for one or more property identifiers in the over 0x8000 range and **GetIDsFromNames** to either create or retrieve the identifiers for one or more names.</span></span> 
  
<span data-ttu-id="c6621-112">Dienstanbieter, die keine Unterstützung für benannte Eigenschaften müssen:</span><span class="sxs-lookup"><span data-stu-id="c6621-112">Service providers that do not support named properties must:</span></span>
  
- <span data-ttu-id="c6621-113">Schlagen Sie Aufrufe von [IMAPIProp::SetProps](imapiprop-setprops.md) Eigenschaften mit Bezeichnern oder größer 0 x 8000 Festlegen des MAPI_E_UNEXPECTED_ID im [SPropProblem](spropproblem.md) -Array zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c6621-113">Fail calls to [IMAPIProp::SetProps](imapiprop-setprops.md) to set properties with identifiers of 0x8000 or greater by returning MAPI_E_UNEXPECTED_ID in the [SPropProblem](spropproblem.md) array.</span></span> 
    
- <span data-ttu-id="c6621-114">Geben Sie die Methoden [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) und [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) MAPI_E_NO_SUPPORT zurück.</span><span class="sxs-lookup"><span data-stu-id="c6621-114">Return MAPI_E_NO_SUPPORT from the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods .</span></span> 
    

