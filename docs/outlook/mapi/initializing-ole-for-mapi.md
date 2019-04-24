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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317227"
---
# <a name="initializing-ole-for-mapi"></a><span data-ttu-id="c1d43-103">Initialisieren von OLE für MAPI</span><span class="sxs-lookup"><span data-stu-id="c1d43-103">Initializing OLE for MAPI</span></span>

  
  
<span data-ttu-id="c1d43-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1d43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1d43-105">Wenn Sie auch OLE verwenden, rufen Sie die OLE-Funktion [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) auf, um die OLE-Bibliotheken zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="c1d43-105">If you also use OLE, call the OLE function [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) to initialize the OLE libraries.</span></span> <span data-ttu-id="c1d43-106">**OleInitialize** initialisiert globale Daten für die Sitzung und bereitet die OLE-Bibliotheken so vor, dass Sie Anrufe annehmen.</span><span class="sxs-lookup"><span data-stu-id="c1d43-106">**OleInitialize** initializes global data for the session and prepares the OLE libraries to accept calls.</span></span> <span data-ttu-id="c1d43-107">Informationen zum Aufrufen von **OleInitialize**finden Sie im Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="c1d43-107">For information about calling **OleInitialize**, see the Windows SDK.</span></span>
  

