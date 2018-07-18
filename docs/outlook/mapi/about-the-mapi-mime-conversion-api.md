---
title: Informationen über die MAPI-MIME-Konvertierungs-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 43ce3ecea6b80bace2bcc2bd333b5c1839514f7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791231"
---
# <a name="about-the-mapi-mime-conversion-api"></a><span data-ttu-id="4fa15-103">Informationen über die MAPI-MIME-Konvertierungs-API</span><span class="sxs-lookup"><span data-stu-id="4fa15-103">About the MAPI-MIME Conversion API</span></span>

  
  
<span data-ttu-id="4fa15-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4fa15-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4fa15-105">Die MAPI-MIME-Konvertierung-API ermöglicht es e-Mail-Anbieter für die Konvertierung zwischen MIME-Objekte und MAPI-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="4fa15-105">The MAPI-MIME Conversion API allows mail providers to convert between MIME objects and MAPI messages.</span></span> <span data-ttu-id="4fa15-106">Softwareentwicklern Konstantendefinitionen Klassenbezeichner und Schnittstellenbezeichner Siehe [MAPI-Konstanten](mapi-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4fa15-106">It provides constant definitions, class identifiers, and interface identifiers as shown in [MAPI Constants](mapi-constants.md).</span></span> <span data-ttu-id="4fa15-107">E-Mail-Anbieter müssen eine Instanz des **[IConverterSession](iconvertersessioniunknown.md)** durch Aufrufen der Funktion **CoCreateInstance** cocreate.</span><span class="sxs-lookup"><span data-stu-id="4fa15-107">Mail providers must cocreate an instance of **[IConverterSession](iconvertersessioniunknown.md)** by calling the **CoCreateInstance** function.</span></span> 
  

