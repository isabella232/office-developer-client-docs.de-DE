---
title: Unterstützung benannter Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 27625e913f06e858295351ed62de840ae7789915
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349630"
---
# <a name="supporting-named-properties"></a><span data-ttu-id="6cf15-103">Unterstützung benannter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6cf15-103">Supporting Named Properties</span></span>

  
  
<span data-ttu-id="6cf15-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6cf15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6cf15-105">Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties.</span><span class="sxs-lookup"><span data-stu-id="6cf15-105">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties.</span></span> <span data-ttu-id="6cf15-106">Die Unterstützung für benannte Eigenschaften ist erforderlich für:</span><span class="sxs-lookup"><span data-stu-id="6cf15-106">Support for named properties is required for:</span></span> 
  
- <span data-ttu-id="6cf15-107">Adressbuchanbieter, mit denen Einträge anderer Anbieter in Ihre Container kopiert werden können.</span><span class="sxs-lookup"><span data-stu-id="6cf15-107">Address book providers that allow entries from other providers to be copied into their containers.</span></span>
    
- <span data-ttu-id="6cf15-108">Nachrichtenspeicher Anbieter, die zum Erstellen beliebiger Nachrichtentypen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="6cf15-108">Message store providers that can be used to create arbitrary message types.</span></span>
    
<span data-ttu-id="6cf15-109">Die Unterstützung benannter Eigenschaften ist für alle anderen Dienstanbieter optional.</span><span class="sxs-lookup"><span data-stu-id="6cf15-109">Named property support is optional for all other service providers.</span></span> <span data-ttu-id="6cf15-110">Dienstanbieter, die benannte Eigenschaften unterstützen, müssen die Zuordnung von Namen zu Bezeichnern in den Methoden [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) und [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) implementieren.</span><span class="sxs-lookup"><span data-stu-id="6cf15-110">Service providers that do support named properties must implement name-to-identifier mapping in the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span> <span data-ttu-id="6cf15-111">Clients rufen **GetNamesFromIDs** auf, um die entsprechenden Namen für einen oder mehrere Eigenschaftsbezeichner im over 0X8000-Range abzurufen, und **GetIDsFromNames** , um die Bezeichner für einen oder mehrere Namen zu erstellen oder abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6cf15-111">Clients call **GetNamesFromIDs** to retrieve the corresponding names for one or more property identifiers in the over 0x8000 range and **GetIDsFromNames** to either create or retrieve the identifiers for one or more names.</span></span> 
  
<span data-ttu-id="6cf15-112">Dienstanbieter, die benannte Eigenschaften nicht unterstützen, müssen:</span><span class="sxs-lookup"><span data-stu-id="6cf15-112">Service providers that do not support named properties must:</span></span>
  
- <span data-ttu-id="6cf15-113">Fehler beim Aufrufen von [IMAPIProp::](imapiprop-setprops.md) SetProps zum Festlegen von Eigenschaften mit Bezeichnern von 0X8000 oder höher, indem MAPI_E_UNEXPECTED_ID im [SPropProblem](spropproblem.md) -Array zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6cf15-113">Fail calls to [IMAPIProp::SetProps](imapiprop-setprops.md) to set properties with identifiers of 0x8000 or greater by returning MAPI_E_UNEXPECTED_ID in the [SPropProblem](spropproblem.md) array.</span></span> 
    
- <span data-ttu-id="6cf15-114">Geben Sie MAPI_E_NO_SUPPORT aus den Methoden [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) und [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="6cf15-114">Return MAPI_E_NO_SUPPORT from the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods .</span></span> 
    

