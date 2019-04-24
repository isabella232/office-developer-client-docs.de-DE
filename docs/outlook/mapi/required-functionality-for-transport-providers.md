---
title: Erforderliche Funktionen für Transport Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7f9768d47cf740bdf50b439ee3af4b0d2a191602
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328686"
---
# <a name="required-functionality-for-transport-providers"></a><span data-ttu-id="b0e6f-103">Erforderliche Funktionen für Transport Anbieter</span><span class="sxs-lookup"><span data-stu-id="b0e6f-103">Required Functionality for Transport Providers</span></span>

  
  
<span data-ttu-id="b0e6f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0e6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0e6f-105">Jeder MAPI-Transportanbieter muss:</span><span class="sxs-lookup"><span data-stu-id="b0e6f-105">Every MAPI transport provider must:</span></span>
  
- <span data-ttu-id="b0e6f-106">BeFolgen Sie die allgemeinen Richtlinien für das Arbeiten mit MAPI und anderen Dienstanbietern.</span><span class="sxs-lookup"><span data-stu-id="b0e6f-106">Follow the general guidelines for working with MAPI and other service providers.</span></span> <span data-ttu-id="b0e6f-107">Weitere Informationen finden Sie unter [MAPI-Anwendungsentwicklung](mapi-application-development.md) und [MAPI-Dienstanbieter](mapi-service-providers.md).</span><span class="sxs-lookup"><span data-stu-id="b0e6f-107">For more information, see [MAPI Application Development](mapi-application-development.md) and [MAPI Service Providers](mapi-service-providers.md).</span></span>
    
- <span data-ttu-id="b0e6f-108">Lassen Sie die [XPProviderInit](xpproviderinit.md) -Initialisierungsfunktion ihrer Transportanbieter-dll für MAPI verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b0e6f-108">Have its transport provider DLL expose to MAPI its [XPProviderInit](xpproviderinit.md) initialization function.</span></span> 
    
- <span data-ttu-id="b0e6f-109">Machen Sie für MAPI die Implementierung der [IXPProvider: IUnknown](ixpprovideriunknown.md) -und [IXPLogon: IUnknown](ixplogoniunknown.md) -Schnittstellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b0e6f-109">Expose to MAPI its implementation of the [IXPProvider : IUnknown](ixpprovideriunknown.md) and [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces.</span></span> 
    
- <span data-ttu-id="b0e6f-110">Verfügbar machen für MAPI-und Clientanwendungen die Implementierung der [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b0e6f-110">Expose to MAPI and client applications its implementation of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="b0e6f-111">Weitere Informationen zum Implementieren von **IMAPIStatus**finden Sie unter [Status Object Implementation](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="b0e6f-111">For more information about implementing **IMAPIStatus**, see [Status Object Implementation](status-object-implementation.md).</span></span> 
    
- <span data-ttu-id="b0e6f-112">Implementieren Sie ein Eigenschaftenblatt-Dialogfeld für die Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b0e6f-112">Implement a property sheet dialog box for configuration.</span></span> <span data-ttu-id="b0e6f-113">Weitere Informationen zum Implementieren von Eigenschaftenblättern finden Sie unter [Eigenschaftenblatt Implementierung](property-sheet-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="b0e6f-113">For more information about implementing property sheets, see [Property Sheet Implementation](property-sheet-implementation.md).</span></span>
    

