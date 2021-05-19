---
title: Informationen über die MAPI-MIME-Konvertierungs-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7123b2deaa9ae0f26002b486df229ad589009f53
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420437"
---
# <a name="about-the-mapi-mime-conversion-api"></a><span data-ttu-id="6387f-103">Informationen über die MAPI-MIME-Konvertierungs-API</span><span class="sxs-lookup"><span data-stu-id="6387f-103">About the MAPI-MIME Conversion API</span></span>

  
  
<span data-ttu-id="6387f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6387f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6387f-105">Die MAPI-MIME-Konvertierungs-API ermöglicht E-Mail-Anbietern das Konvertieren zwischen MIME-Objekten und MAPI-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="6387f-105">The MAPI-MIME Conversion API allows mail providers to convert between MIME objects and MAPI messages.</span></span> <span data-ttu-id="6387f-106">Sie stellt Konstantendefinitionen, Klassenbezeichner und Schnittstellenbezeichner bereit, wie in [MAPI-Konstanten dargestellt.](mapi-constants.md)</span><span class="sxs-lookup"><span data-stu-id="6387f-106">It provides constant definitions, class identifiers, and interface identifiers as shown in [MAPI Constants](mapi-constants.md).</span></span> <span data-ttu-id="6387f-107">E-Mail-Anbieter müssen eine Instanz von **[IConverterSession](iconvertersessioniunknown.md)** durch Aufrufen der **CoCreateInstance-Funktion zusammenstellen.**</span><span class="sxs-lookup"><span data-stu-id="6387f-107">Mail providers must cocreate an instance of **[IConverterSession](iconvertersessioniunknown.md)** by calling the **CoCreateInstance** function.</span></span> 
  

