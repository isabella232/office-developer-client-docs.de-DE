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
ms.openlocfilehash: 3f461d50e838aac0caee37d295ba8e86b9559bd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795830"
---
# <a name="using-the-mapi-utilities"></a><span data-ttu-id="69e98-103">Verwenden der MAPI-Dienstprogramme</span><span class="sxs-lookup"><span data-stu-id="69e98-103">Using the MAPI Utilities</span></span>

  
  
<span data-ttu-id="69e98-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="69e98-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="69e98-105">Die MAPI-Dienstprogramme Tabellendaten und Datenobjekte Eigenschaft sowie einer Reihe von Funktionen bestehen aus, um verschiedene Features unterstützen.</span><span class="sxs-lookup"><span data-stu-id="69e98-105">The MAPI utilities are made up of table data and property data objects and a variety of functions to support miscellaneous features.</span></span> <span data-ttu-id="69e98-106">Es ist möglich, damit ein Client benötigen nur diese Dienstprogramme und zur Anmeldung bei der MAPI-Subsystems herstellen eine Verbindung mit dem Dienstanbieter nicht haben.</span><span class="sxs-lookup"><span data-stu-id="69e98-106">It is possible for a client to need only these utilities and not have to log on to the MAPI subsystem to establish a connection with service providers.</span></span> <span data-ttu-id="69e98-107">Wenn der Client in dieser Kategorie passt, rufen Sie die API-Funktion [ScInitMapiUtil](scinitmapiutil.md) statt der Funktion ["MAPIInitialize"](mapiinitialize.md) bei der Initialisierung.</span><span class="sxs-lookup"><span data-stu-id="69e98-107">If your client fits into this category, call the API function [ScInitMapiUtil](scinitmapiutil.md) rather than the [MAPIInitialize](mapiinitialize.md) function at initialization time.</span></span> 
  
 <span data-ttu-id="69e98-108">**ScInitMapiUtil** können Clients Hilfsfunktionen verwenden Sie die MAPI-Allocators erfordern, aber, die nicht mehr für die Allocators explizit.</span><span class="sxs-lookup"><span data-stu-id="69e98-108">**ScInitMapiUtil** enables clients to use utility functions that require MAPI allocators, but that do not ask for the allocators explicitly.</span></span> <span data-ttu-id="69e98-109">Wenn heruntergefahren werden soll, rufen Sie [DeinitMapiUtil](deinitmapiutil.md) um Ressourcen freizugeben, sondern [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="69e98-109">When it is time to shut down, call [DeinitMapiUtil](deinitmapiutil.md) to free resources rather than [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="69e98-110">Clients, die nie **"MAPIInitialize anrufen"** sollte nicht **MAPIUninitialize**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="69e98-110">Clients that never call **MAPIInitialize** should not call **MAPIUninitialize**.</span></span>
  
<span data-ttu-id="69e98-111">Wenn Sie **ScInitMapiUtil** statt **"MAPIInitialize"** aufgerufen und Tabellen über die Methoden **ITableData** nicht über die **IMAPITable** -Methoden verwenden, beachten Sie, dass Tabelle Benachrichtigungen nicht funktioniert.</span><span class="sxs-lookup"><span data-stu-id="69e98-111">If you have called **ScInitMapiUtil** rather than **MAPIInitialize** and are using tables through the **ITableData** methods rather than through the **IMAPITable** methods, be aware that table notifications will not work.</span></span> <span data-ttu-id="69e98-112">Benachrichtigungen erfordern die Verwendung der MAPI-Bibliotheken und [IMAPITable: IUnknown](imapitableiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="69e98-112">Notifications require the use of the MAPI libraries and [IMAPITable : IUnknown](imapitableiunknown.md).</span></span>
  

