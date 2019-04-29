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
ms.openlocfilehash: 5c5a9355e9edec28e08986ccd055fc43eec7b974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420948"
---
# <a name="initializing-the-mapi-utilities"></a><span data-ttu-id="44ebe-103">Initialisieren der MAPI-Dienstprogramme</span><span class="sxs-lookup"><span data-stu-id="44ebe-103">Initializing the MAPI Utilities</span></span>

  
  
<span data-ttu-id="44ebe-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44ebe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44ebe-105">Wenn der einzige Teil von MAPI, den Sie verwenden müssen, die Dienstprogramme ist – die Schnittstellen und Funktionen, die in MAPIs MAPIUTIL deklariert werden. H-Headerdatei wie **IPropData** und **ITableData** – Sie müssen **MAPIInitialize** nicht für die Initialisierung aufrufen.</span><span class="sxs-lookup"><span data-stu-id="44ebe-105">If the only part of MAPI that you need to use are the utilities — the interfaces and functions declared in MAPI's MAPIUTIL.H header file such as **IPropData** and **ITableData** — you do not need to call **MAPIInitialize** for initialization.</span></span> <span data-ttu-id="44ebe-106">Weitere Informationen finden Sie unter [IPropData: IMAPIProp](ipropdataimapiprop.md), [ITableData: IUnknown](itabledataiunknown.md)und [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="44ebe-106">For more information, see [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md), and [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="44ebe-107">Rufen Sie stattdessen die **ScInitMapiUtil** -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="44ebe-107">Instead, call the **ScInitMapiUtil** function.</span></span> <span data-ttu-id="44ebe-108">Weitere Informationen finden Sie unter [ScInitMapiUtil](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="44ebe-108">For more information, see [ScInitMapiUtil](scinitmapiutil.md).</span></span> <span data-ttu-id="44ebe-109">**ScInitMapiUtil** ermöglicht Clientanwendungen das Verwenden von Hilfsfunktionen und Methoden, die MAPI-Zuweisungen erfordern, die Sie jedoch nicht explizit anfordern.</span><span class="sxs-lookup"><span data-stu-id="44ebe-109">**ScInitMapiUtil** enables client applications to use utility functions and methods that require MAPI allocators, but that do not ask for them explicitly.</span></span> 
  
<span data-ttu-id="44ebe-110">Rufen Sie zum Zeitpunkt des Herunterfahrens den **DeinitMapiUtil** auf, um Ressourcen für die Dienstprogramme freizugeben.</span><span class="sxs-lookup"><span data-stu-id="44ebe-110">At shutdown time, make a call to **DeinitMapiUtil** to free resources connected to the utilities.</span></span> <span data-ttu-id="44ebe-111">Rufen Sie **MAPIUninitialize**nicht auf.</span><span class="sxs-lookup"><span data-stu-id="44ebe-111">Do not call **MAPIUninitialize**.</span></span> <span data-ttu-id="44ebe-112">Weitere Informationen finden Sie unter [DeinitMapiUtil](deinitmapiutil.md) und [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="44ebe-112">For more information, see [DeinitMapiUtil](deinitmapiutil.md) and [MAPIUninitialize](mapiuninitialize.md).</span></span>
  
<span data-ttu-id="44ebe-113">Beachten Sie, dass die **ITableData** -Schnittstelle Tabellen Benachrichtigungen für Clients, die **ScInitMapiUtil** aufgerufen haben, nicht **MAPIInitialize**unterstützt.</span><span class="sxs-lookup"><span data-stu-id="44ebe-113">Be aware that the **ITableData** interface does not support table notifications for clients that have called **ScInitMapiUtil** rather than **MAPIInitialize**.</span></span> 
  

