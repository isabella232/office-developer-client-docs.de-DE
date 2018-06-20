---
title: Ein Objekt ungültig
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9c0ba8f1f0bf31bb892f380df310cd9fa7a8a24f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792716"
---
# <a name="invalidating-an-object"></a><span data-ttu-id="5f658-103">Ein Objekt ungültig</span><span class="sxs-lookup"><span data-stu-id="5f658-103">Invalidating an Object</span></span>

  
  
<span data-ttu-id="5f658-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5f658-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5f658-105">Als Teil des Herunterfahrens des Anbieters sollten Sie ein Objekt ungültig.</span><span class="sxs-lookup"><span data-stu-id="5f658-105">As part of your provider's shutdown process, you might want to invalidate an object.</span></span> <span data-ttu-id="5f658-106">Ein Objekt ungültig umfasst, und Ersetzen Sie die vtable des Objekts durch eine Vtable, die Implementierungen für die drei **IUnknown** -Methoden enthält: **QueryInterface**, **AddRef**und **Release**.</span><span class="sxs-lookup"><span data-stu-id="5f658-106">Invalidating an object involves replacing its vtable with a vtable that contains implementations for the three **IUnknown** methods: **AddRef**, **Release**, and **QueryInterface**.</span></span> <span data-ttu-id="5f658-107">Ein Objekt ungültig wird durch Aufrufen von [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), eine Methode, die im jedes der drei allgemeine Providertypen Support-Objekt enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="5f658-107">Invalidate an object by calling [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), a method that is included in the support object of each of the three common provider types.</span></span> <span data-ttu-id="5f658-108">Anbieter stellen dieses Anrufs in der Regel in der Implementierung von ihrer Anmeldung-Objekt **Logoff (** Methode).</span><span class="sxs-lookup"><span data-stu-id="5f658-108">Providers typically make this call in the implementation of their logon object's **Logoff** method.</span></span> 
  
<span data-ttu-id="5f658-109">Ein Objekt ungültig bietet MAPI die ultimative Verantwortung für ein Objekt zugeordneten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="5f658-109">Invalidating an object gives MAPI the ultimate responsibility for freeing the memory associated with an object.</span></span> <span data-ttu-id="5f658-110">Sie können alle Ressourcen verbunden mit einem Objekt frei, und rufen Sie dann **MakeInvalid** , um alle Methoden in seiner geerbten Schnittstellen ungültig.</span><span class="sxs-lookup"><span data-stu-id="5f658-110">You can free all of the resources connected with an object and then call **MakeInvalid** to invalidate all of the methods in its inherited interfaces.</span></span> <span data-ttu-id="5f658-111">Anrufe an eine der folgenden Methoden gibt MAPI_E_INVALID_OBJECT zurück.</span><span class="sxs-lookup"><span data-stu-id="5f658-111">Calls to any of these methods will return MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="5f658-112">Verwenden von **MakeInvalid** ist eine Option, die viele Dienstanbieter ignoriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5f658-112">Using **MakeInvalid** is an option that many service providers choose to ignore.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5f658-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f658-113">See also</span></span>



[<span data-ttu-id="5f658-114">Herunterfahren von einem Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="5f658-114">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

