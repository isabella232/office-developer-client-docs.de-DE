---
title: Invalidieren eines Objekts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bf7ef15ccfd9cd015771785bda9d6ad79415736b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317199"
---
# <a name="invalidating-an-object"></a><span data-ttu-id="fab8e-103">Invalidieren eines Objekts</span><span class="sxs-lookup"><span data-stu-id="fab8e-103">Invalidating an Object</span></span>

  
  
<span data-ttu-id="fab8e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fab8e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fab8e-105">Im Rahmen des Herunterfahrens des Anbieters möchten Sie möglicherweise ein Objekt ungültig machen.</span><span class="sxs-lookup"><span data-stu-id="fab8e-105">As part of your provider's shutdown process, you might want to invalidate an object.</span></span> <span data-ttu-id="fab8e-106">Für die Invalidierung eines Objekts wird die Vtable durch eine Vtable ersetzt, die Implementierungen für die drei **IUnknown** -Methoden enthält: **AddRef**, **Release**und **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="fab8e-106">Invalidating an object involves replacing its vtable with a vtable that contains implementations for the three **IUnknown** methods: **AddRef**, **Release**, and **QueryInterface**.</span></span> <span data-ttu-id="fab8e-107">Ein Objekt wird ungültig, indem [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md), eine Methode aufgerufen wird, die im Support Objekt der drei gängigen Anbietertypen enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="fab8e-107">Invalidate an object by calling [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), a method that is included in the support object of each of the three common provider types.</span></span> <span data-ttu-id="fab8e-108">Anbieter führen diesen Aufruf in der Regel in der Implementierung der **Logout** -Methode Ihres LOGON-Objekts aus.</span><span class="sxs-lookup"><span data-stu-id="fab8e-108">Providers typically make this call in the implementation of their logon object's **Logoff** method.</span></span> 
  
<span data-ttu-id="fab8e-109">Durch die Invalidierung eines Objekts wird MAPI die ultimative Verantwortung für die Freigabe des Arbeitsspeichers zugewiesen, der einem Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fab8e-109">Invalidating an object gives MAPI the ultimate responsibility for freeing the memory associated with an object.</span></span> <span data-ttu-id="fab8e-110">Sie können alle mit einem Objekt verbundenen Ressourcen freigeben und dann **MakeInvalid** aufrufen, um alle Methoden in den geerbten Schnittstellen zu invalidieren.</span><span class="sxs-lookup"><span data-stu-id="fab8e-110">You can free all of the resources connected with an object and then call **MakeInvalid** to invalidate all of the methods in its inherited interfaces.</span></span> <span data-ttu-id="fab8e-111">Aufrufe einer dieser Methoden geben MAPI_E_INVALID_OBJECT zurück.</span><span class="sxs-lookup"><span data-stu-id="fab8e-111">Calls to any of these methods will return MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="fab8e-112">Die Verwendung von **MakeInvalid** ist eine Option, die von vielen Dienstanbietern ignoriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fab8e-112">Using **MakeInvalid** is an option that many service providers choose to ignore.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fab8e-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fab8e-113">See also</span></span>



[<span data-ttu-id="fab8e-114">Herunterfahren eines Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="fab8e-114">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

