---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d8c6699ac1bc5687b1c885d156535e5b54b93140
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791330"
---
# <a name="attattachrenddata"></a><span data-ttu-id="0398a-103">attAttachRenddata</span><span class="sxs-lookup"><span data-stu-id="0398a-103">attAttachRenddata</span></span>

  
  
<span data-ttu-id="0398a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0398a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0398a-105">Das Attribut **AttAttachRenddata** wird als eine **RENDDATA** Struktur codiert, die beschreibt, wie und, in dem die Anlage im Nachrichtentext gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="0398a-105">The **attAttachRenddata** attribute is encoded as a **RENDDATA** structure that describes how and where the attachment is rendered in the message text.</span></span> <span data-ttu-id="0398a-106">Die Struktur **RENDDATA** ist einfach in der TNEF-Stream als beginnend mit dem ersten Element in der Struktur **RENDDATA** **sizeof(RENDDATA)** -Bytes codiert.</span><span class="sxs-lookup"><span data-stu-id="0398a-106">The **RENDDATA** structure is simply encoded in the TNEF stream as **sizeof(RENDDATA)** bytes beginning with the first member of the **RENDDATA** structure.</span></span> <span data-ttu-id="0398a-107">Wenn der Wert der **RENDDATA** -Struktur **DwFlags** Members auf **MAC_BINARY**festgelegt ist, werden die Daten für die folgenden Anlage im MacBinary-Format gespeichert. Andernfalls werden die Anlagendaten wie gewohnt codiert.</span><span class="sxs-lookup"><span data-stu-id="0398a-107">If the value of the **RENDDATA** structure's **dwFlags** member is set to **MAC_BINARY**, then the data for the following attachment is stored in MacBinary format; otherwise, the attachment data is encoded as usual.</span></span>
  

