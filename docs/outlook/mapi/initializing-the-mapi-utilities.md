---
title: Initialisieren der MAPI-Dienstprogramme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d0507a26b9ae5ae018111e2771e3af8b25761786
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567671"
---
# <a name="initializing-the-mapi-utilities"></a><span data-ttu-id="2acd6-103">Initialisieren der MAPI-Dienstprogramme</span><span class="sxs-lookup"><span data-stu-id="2acd6-103">Initializing the MAPI Utilities</span></span>

  
  
<span data-ttu-id="2acd6-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2acd6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2acd6-105">Wenn der einzige Teil des MAPI, die Sie verwenden müssen, sind die Dienstprogramme – die Schnittstellen und Funktionen in der MAPI-MAPIUTIL deklariert. H-Headerdatei wie **IPropData** und **ITableData** – Sie müssen nicht für die Initialisierung **"MAPIInitialize"** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2acd6-105">If the only part of MAPI that you need to use are the utilities — the interfaces and functions declared in MAPI's MAPIUTIL.H header file such as **IPropData** and **ITableData** — you do not need to call **MAPIInitialize** for initialization.</span></span> <span data-ttu-id="2acd6-106">Weitere Informationen finden Sie unter [IPropData: IMAPIProp](ipropdataimapiprop.md), [ITableData: IUnknown](itabledataiunknown.md), und ["MAPIInitialize"](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="2acd6-106">For more information, see [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md), and [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="2acd6-107">Rufen Sie stattdessen die **ScInitMapiUtil** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="2acd6-107">Instead, call the **ScInitMapiUtil** function.</span></span> <span data-ttu-id="2acd6-108">Weitere Informationen finden Sie unter [ScInitMapiUtil](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="2acd6-108">For more information, see [ScInitMapiUtil](scinitmapiutil.md).</span></span> <span data-ttu-id="2acd6-109">**ScInitMapiUtil** von Clientanwendungen Hilfsfunktionen und Methoden, die MAPI-Allocators erfordern, aber, die nicht mehr für diese explizit, verwenden.</span><span class="sxs-lookup"><span data-stu-id="2acd6-109">**ScInitMapiUtil** enables client applications to use utility functions and methods that require MAPI allocators, but that do not ask for them explicitly.</span></span> 
  
<span data-ttu-id="2acd6-110">Rufen Sie beim Herunterfahren **DeinitMapiUtil** zum Freigeben von Ressourcen, die mit der Dienstprogramme verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="2acd6-110">At shutdown time, make a call to **DeinitMapiUtil** to free resources connected to the utilities.</span></span> <span data-ttu-id="2acd6-111">**MAPIUninitialize**nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2acd6-111">Do not call **MAPIUninitialize**.</span></span> <span data-ttu-id="2acd6-112">Weitere Informationen finden Sie unter [DeinitMapiUtil](deinitmapiutil.md) und [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="2acd6-112">For more information, see [DeinitMapiUtil](deinitmapiutil.md) and [MAPIUninitialize](mapiuninitialize.md).</span></span>
  
<span data-ttu-id="2acd6-113">Beachten Sie, dass die Schnittstelle **ITableData** Tabelle Benachrichtigungen für Clients nicht unterstützt, die **ScInitMapiUtil** statt **"MAPIInitialize"** aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="2acd6-113">Be aware that the **ITableData** interface does not support table notifications for clients that have called **ScInitMapiUtil** rather than **MAPIInitialize**.</span></span> 
  

