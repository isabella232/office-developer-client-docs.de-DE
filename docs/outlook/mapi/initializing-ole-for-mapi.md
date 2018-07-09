---
title: Initialisierung von OLE für die MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6efe41c79cd85eb844ee19b8c54e200956c9b2a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792680"
---
# <a name="initializing-ole-for-mapi"></a><span data-ttu-id="2edab-103">Initialisierung von OLE für die MAPI</span><span class="sxs-lookup"><span data-stu-id="2edab-103">Initializing OLE for MAPI</span></span>

  
  
<span data-ttu-id="2edab-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2edab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2edab-105">Wenn Sie auch OLE verwenden, rufen Sie die OLE-Funktion [OleInitialize](http://msdn.microsoft.com/de-de/library/ms690134%28v=VS.85%29.aspx) die OLE-Bibliotheken nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="2edab-105">If you also use OLE, call the OLE function [OleInitialize](http://msdn.microsoft.com/de-de/library/ms690134%28v=VS.85%29.aspx) to initialize the OLE libraries.</span></span> <span data-ttu-id="2edab-106">**OleInitialize** globale Daten für die Sitzung initialisiert und bereitet die OLE-Bibliotheken Anrufe annehmen.</span><span class="sxs-lookup"><span data-stu-id="2edab-106">**OleInitialize** initializes global data for the session and prepares the OLE libraries to accept calls.</span></span> <span data-ttu-id="2edab-107">Informationen zu den aufrufenden **OleInitialize**finden Sie im Windows-SDK.</span><span class="sxs-lookup"><span data-stu-id="2edab-107">For information about calling **OleInitialize**, see the Windows SDK.</span></span>
  

