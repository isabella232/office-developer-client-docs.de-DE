---
title: Informationen über die MAPI-MIME-Konvertierungs-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7123b2deaa9ae0f26002b486df229ad589009f53
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321819"
---
# <a name="about-the-mapi-mime-conversion-api"></a><span data-ttu-id="7d0d3-103">Informationen über die MAPI-MIME-Konvertierungs-API</span><span class="sxs-lookup"><span data-stu-id="7d0d3-103">About the MAPI-MIME Conversion API</span></span>

  
  
<span data-ttu-id="7d0d3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d0d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d0d3-105">Die MAPI-MIME-Konvertierungs-API ermöglicht es e-Mail-Anbietern, zwischen MIME-Objekten und MAPI-Nachrichten zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="7d0d3-105">The MAPI-MIME Conversion API allows mail providers to convert between MIME objects and MAPI messages.</span></span> <span data-ttu-id="7d0d3-106">Es stellt Konstante Definitionen, Klassenbezeichner und Schnittstellenbezeichner bereit, wie in [MAPI-Konstanten](mapi-constants.md)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7d0d3-106">It provides constant definitions, class identifiers, and interface identifiers as shown in [MAPI Constants](mapi-constants.md).</span></span> <span data-ttu-id="7d0d3-107">E-Mail-Anbieter müssen eine Instanz von **[IConverterSession](iconvertersessioniunknown.md)** erstellen, indem Sie die **CoCreateInstance** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7d0d3-107">Mail providers must cocreate an instance of **[IConverterSession](iconvertersessioniunknown.md)** by calling the **CoCreateInstance** function.</span></span> 
  

