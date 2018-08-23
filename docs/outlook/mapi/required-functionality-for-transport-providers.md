---
title: Erforderliche Funktionen für Transportanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: dc1189df1b8ad8f8e613d6813681ed3f4148b122
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580495"
---
# <a name="required-functionality-for-transport-providers"></a><span data-ttu-id="15f77-103">Erforderliche Funktionen für Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="15f77-103">Required Functionality for Transport Providers</span></span>

  
  
<span data-ttu-id="15f77-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15f77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15f77-105">Jedes MAPI-Transportdienst muss:</span><span class="sxs-lookup"><span data-stu-id="15f77-105">Every MAPI transport provider must:</span></span>
  
- <span data-ttu-id="15f77-106">Führen Sie die allgemeinen Richtlinien für die Arbeit mit MAPI- und anderen Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="15f77-106">Follow the general guidelines for working with MAPI and other service providers.</span></span> <span data-ttu-id="15f77-107">Weitere Informationen finden Sie unter [MAPI-Anwendungsentwicklung](mapi-application-development.md) und [MAPI-Dienstanbieter](mapi-service-providers.md).</span><span class="sxs-lookup"><span data-stu-id="15f77-107">For more information, see [MAPI Application Development](mapi-application-development.md) and [MAPI Service Providers](mapi-service-providers.md).</span></span>
    
- <span data-ttu-id="15f77-108">Der Adressbuchhierarchie DLL machen MAPI seine Initialisierungsfunktion [XPProviderInit](xpproviderinit.md) haben.</span><span class="sxs-lookup"><span data-stu-id="15f77-108">Have its transport provider DLL expose to MAPI its [XPProviderInit](xpproviderinit.md) initialization function.</span></span> 
    
- <span data-ttu-id="15f77-109">Die Implementierung von MAPI verfügbar machen die [IXPProvider: IUnknown](ixpprovideriunknown.md) und [IXPLogon: IUnknown](ixplogoniunknown.md) Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="15f77-109">Expose to MAPI its implementation of the [IXPProvider : IUnknown](ixpprovideriunknown.md) and [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces.</span></span> 
    
- <span data-ttu-id="15f77-110">Die Implementierung von für MAPI-und Clientanwendungen verfügbar machen die [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="15f77-110">Expose to MAPI and client applications its implementation of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="15f77-111">Weitere Informationen zum Implementieren von **IMAPIStatus**finden Sie unter [Implementierung der Status-Objekts](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="15f77-111">For more information about implementing **IMAPIStatus**, see [Status Object Implementation](status-object-implementation.md).</span></span> 
    
- <span data-ttu-id="15f77-112">Implementieren Sie ein Blatt Eigenschaftendialogfeld für die Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="15f77-112">Implement a property sheet dialog box for configuration.</span></span> <span data-ttu-id="15f77-113">Weitere Informationen zum Implementieren von Eigenschaftenseiten finden Sie unter [Implementierung von Eigenschaften Blatt](property-sheet-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="15f77-113">For more information about implementing property sheets, see [Property Sheet Implementation](property-sheet-implementation.md).</span></span>
    

