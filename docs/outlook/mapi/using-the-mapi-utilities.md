---
title: Verwenden der MAPI-Dienstprogramme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d8ec18ee7b80d8603266cf827f9484ee85bdb03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409986"
---
# <a name="using-the-mapi-utilities"></a><span data-ttu-id="61081-103">Verwenden der MAPI-Dienstprogramme</span><span class="sxs-lookup"><span data-stu-id="61081-103">Using the MAPI Utilities</span></span>

  
  
<span data-ttu-id="61081-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61081-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61081-105">Die MAPI-Dienstprogramme bestehen aus Tabellendaten und Eigenschaftendaten Objekten sowie verschiedenen Funktionen zur Unterstützung verschiedener Features.</span><span class="sxs-lookup"><span data-stu-id="61081-105">The MAPI utilities are made up of table data and property data objects and a variety of functions to support miscellaneous features.</span></span> <span data-ttu-id="61081-106">Ein Client kann nur diese Dienstprogramme benötigen und sich nicht beim MAPI-Subsystem anmelden, um eine Verbindung mit Dienstanbietern herzustellen.</span><span class="sxs-lookup"><span data-stu-id="61081-106">It is possible for a client to need only these utilities and not have to log on to the MAPI subsystem to establish a connection with service providers.</span></span> <span data-ttu-id="61081-107">Wenn Ihr Client in diese Kategorie passt, rufen Sie die API-Funktion [ScInitMapiUtil](scinitmapiutil.md) anstelle der [MAPIInitialize](mapiinitialize.md) -Funktion bei der Initialisierungszeit.</span><span class="sxs-lookup"><span data-stu-id="61081-107">If your client fits into this category, call the API function [ScInitMapiUtil](scinitmapiutil.md) rather than the [MAPIInitialize](mapiinitialize.md) function at initialization time.</span></span> 
  
 <span data-ttu-id="61081-108">**ScInitMapiUtil** ermöglicht Clients das Verwenden von Hilfsfunktionen, die MAPI-Zuweisungen erfordern, die jedoch nicht explizit nach den Zuordnungen Fragen.</span><span class="sxs-lookup"><span data-stu-id="61081-108">**ScInitMapiUtil** enables clients to use utility functions that require MAPI allocators, but that do not ask for the allocators explicitly.</span></span> <span data-ttu-id="61081-109">Wenn es Zeit zum Herunterfahren ist, rufen Sie [DeinitMapiUtil](deinitmapiutil.md) auf, um Ressourcen anstelle von [MAPIUninitialize](mapiuninitialize.md)zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="61081-109">When it is time to shut down, call [DeinitMapiUtil](deinitmapiutil.md) to free resources rather than [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="61081-110">Clients, die **MAPIInitialize** nie aufrufen, sollten **MAPIUninitialize**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="61081-110">Clients that never call **MAPIInitialize** should not call **MAPIUninitialize**.</span></span>
  
<span data-ttu-id="61081-111">Wenn Sie **ScInitMapiUtil** statt **MAPIInitialize** aufgerufen haben und Tabellen über die **ITableData** -Methoden statt über die **IMAPITable** -Methoden verwenden, beachten Sie, dass Tabellen Benachrichtigungen nicht funktionieren.</span><span class="sxs-lookup"><span data-stu-id="61081-111">If you have called **ScInitMapiUtil** rather than **MAPIInitialize** and are using tables through the **ITableData** methods rather than through the **IMAPITable** methods, be aware that table notifications will not work.</span></span> <span data-ttu-id="61081-112">Benachrichtigungen erfordern die Verwendung der MAPI-Bibliotheken und [IMAPITable: IUnknown](imapitableiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="61081-112">Notifications require the use of the MAPI libraries and [IMAPITable : IUnknown](imapitableiunknown.md).</span></span>
  

