---
title: Initialisieren von OLE für MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cd279c17574ce73b42d5e07e96ac817af71dc700
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589805"
---
# <a name="initializing-ole-for-mapi"></a><span data-ttu-id="f699a-103">Initialisieren von OLE für MAPI</span><span class="sxs-lookup"><span data-stu-id="f699a-103">Initializing OLE for MAPI</span></span>

  
  
<span data-ttu-id="f699a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f699a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f699a-105">Wenn Sie auch OLE verwenden, rufen Sie die OLE-Funktion [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) die OLE-Bibliotheken nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f699a-105">If you also use OLE, call the OLE function [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) to initialize the OLE libraries.</span></span> <span data-ttu-id="f699a-106">**OleInitialize** globale Daten für die Sitzung initialisiert und bereitet die OLE-Bibliotheken Anrufe annehmen.</span><span class="sxs-lookup"><span data-stu-id="f699a-106">**OleInitialize** initializes global data for the session and prepares the OLE libraries to accept calls.</span></span> <span data-ttu-id="f699a-107">Informationen zu den aufrufenden **OleInitialize**finden Sie im Windows-SDK.</span><span class="sxs-lookup"><span data-stu-id="f699a-107">For information about calling **OleInitialize**, see the Windows SDK.</span></span>
  

