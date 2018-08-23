---
title: Informationen über die MAPI-MIME-Konvertierungs-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 23e68d18a6de93a99d2db32c1d93dac33d9a1225
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575266"
---
# <a name="about-the-mapi-mime-conversion-api"></a><span data-ttu-id="77ec4-103">Informationen über die MAPI-MIME-Konvertierungs-API</span><span class="sxs-lookup"><span data-stu-id="77ec4-103">About the MAPI-MIME Conversion API</span></span>

  
  
<span data-ttu-id="77ec4-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77ec4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77ec4-105">Die MAPI-MIME-Konvertierung-API ermöglicht es e-Mail-Anbieter für die Konvertierung zwischen MIME-Objekte und MAPI-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="77ec4-105">The MAPI-MIME Conversion API allows mail providers to convert between MIME objects and MAPI messages.</span></span> <span data-ttu-id="77ec4-106">Softwareentwicklern Konstantendefinitionen Klassenbezeichner und Schnittstellenbezeichner Siehe [MAPI-Konstanten](mapi-constants.md).</span><span class="sxs-lookup"><span data-stu-id="77ec4-106">It provides constant definitions, class identifiers, and interface identifiers as shown in [MAPI Constants](mapi-constants.md).</span></span> <span data-ttu-id="77ec4-107">E-Mail-Anbieter müssen eine Instanz des **[IConverterSession](iconvertersessioniunknown.md)** durch Aufrufen der Funktion **CoCreateInstance** cocreate.</span><span class="sxs-lookup"><span data-stu-id="77ec4-107">Mail providers must cocreate an instance of **[IConverterSession](iconvertersessioniunknown.md)** by calling the **CoCreateInstance** function.</span></span> 
  

