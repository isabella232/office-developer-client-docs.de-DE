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
ms.openlocfilehash: 87310916f4a54b308f0599ec5c1a4a3bfe83c376
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388416"
---
# <a name="initializing-ole-for-mapi"></a><span data-ttu-id="f0fd1-103">Initialisieren von OLE für MAPI</span><span class="sxs-lookup"><span data-stu-id="f0fd1-103">Initializing OLE for MAPI</span></span>

  
  
<span data-ttu-id="f0fd1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0fd1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0fd1-105">Wenn Sie auch OLE verwenden, rufen Sie die OLE-Funktion [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) die OLE-Bibliotheken nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f0fd1-105">If you also use OLE, call the OLE function [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) to initialize the OLE libraries.</span></span> <span data-ttu-id="f0fd1-106">**OleInitialize** globale Daten für die Sitzung initialisiert und bereitet die OLE-Bibliotheken Anrufe annehmen.</span><span class="sxs-lookup"><span data-stu-id="f0fd1-106">**OleInitialize** initializes global data for the session and prepares the OLE libraries to accept calls.</span></span> <span data-ttu-id="f0fd1-107">Informationen zu den aufrufenden **OleInitialize**finden Sie im Windows-SDK.</span><span class="sxs-lookup"><span data-stu-id="f0fd1-107">For information about calling **OleInitialize**, see the Windows SDK.</span></span>
  

