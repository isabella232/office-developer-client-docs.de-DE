---
title: Ungültigen eines Objekts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bf7ef15ccfd9cd015771785bda9d6ad79415736b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407676"
---
# <a name="invalidating-an-object"></a><span data-ttu-id="e7040-103">Ungültigen eines Objekts</span><span class="sxs-lookup"><span data-stu-id="e7040-103">Invalidating an Object</span></span>

  
  
<span data-ttu-id="e7040-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7040-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7040-105">Im Rahmen des Herunterfahrens Ihres Anbieters möchten Sie möglicherweise ein Objekt ungültig erklären.</span><span class="sxs-lookup"><span data-stu-id="e7040-105">As part of your provider's shutdown process, you might want to invalidate an object.</span></span> <span data-ttu-id="e7040-106">Das Ungültigen eines Objekts umfasst das Ersetzen der vtable durch eine vtable, die Implementierungen für die drei **IUnknown-Methoden** **enthält: AddRef**, **Release** und **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="e7040-106">Invalidating an object involves replacing its vtable with a vtable that contains implementations for the three **IUnknown** methods: **AddRef**, **Release**, and **QueryInterface**.</span></span> <span data-ttu-id="e7040-107">Ungültig machen Sie ein Objekt, indem [Sie IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)aufrufen, eine Methode, die im Supportobjekt der drei gängigen Anbietertypen enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e7040-107">Invalidate an object by calling [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), a method that is included in the support object of each of the three common provider types.</span></span> <span data-ttu-id="e7040-108">Anbieter rufen diesen Aufruf in der Regel in der Implementierung der **Logoff-Methode** des Anmeldeobjekts ab.</span><span class="sxs-lookup"><span data-stu-id="e7040-108">Providers typically make this call in the implementation of their logon object's **Logoff** method.</span></span> 
  
<span data-ttu-id="e7040-109">Durch die Ungültigkeit eines Objekts ist MAPI letztendlich für die Speicherfreispeicherung verantwortlich, die einem Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e7040-109">Invalidating an object gives MAPI the ultimate responsibility for freeing the memory associated with an object.</span></span> <span data-ttu-id="e7040-110">Sie können alle ressourcen frei, die mit einem Objekt verbunden sind, und **makeInvalid** aufrufen, um alle Methoden in den geerbten Schnittstellen ungültig zu machen.</span><span class="sxs-lookup"><span data-stu-id="e7040-110">You can free all of the resources connected with an object and then call **MakeInvalid** to invalidate all of the methods in its inherited interfaces.</span></span> <span data-ttu-id="e7040-111">Aufrufe einer dieser Methoden geben MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="e7040-111">Calls to any of these methods will return MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="e7040-112">Die **Verwendung von MakeInvalid** ist eine Option, die viele Dienstanbieter ignorieren.</span><span class="sxs-lookup"><span data-stu-id="e7040-112">Using **MakeInvalid** is an option that many service providers choose to ignore.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e7040-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7040-113">See also</span></span>



[<span data-ttu-id="e7040-114">Herunterfahren eines Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="e7040-114">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

