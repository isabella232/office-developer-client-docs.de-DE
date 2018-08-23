---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a006c126ec5e0fb86847226195efd03f7ae5351f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569449"
---
# <a name="attattachrenddata"></a><span data-ttu-id="37d2c-103">attAttachRenddata</span><span class="sxs-lookup"><span data-stu-id="37d2c-103">attAttachRenddata</span></span>

  
  
<span data-ttu-id="37d2c-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37d2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37d2c-105">Das Attribut **AttAttachRenddata** wird als eine **RENDDATA** Struktur codiert, die beschreibt, wie und, in dem die Anlage im Nachrichtentext gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="37d2c-105">The **attAttachRenddata** attribute is encoded as a **RENDDATA** structure that describes how and where the attachment is rendered in the message text.</span></span> <span data-ttu-id="37d2c-106">Die Struktur **RENDDATA** ist einfach in der TNEF-Stream als beginnend mit dem ersten Element in der Struktur **RENDDATA** **sizeof(RENDDATA)** -Bytes codiert.</span><span class="sxs-lookup"><span data-stu-id="37d2c-106">The **RENDDATA** structure is simply encoded in the TNEF stream as **sizeof(RENDDATA)** bytes beginning with the first member of the **RENDDATA** structure.</span></span> <span data-ttu-id="37d2c-107">Wenn der Wert der **RENDDATA** -Struktur **DwFlags** Members auf **MAC_BINARY**festgelegt ist, werden die Daten für die folgenden Anlage im MacBinary-Format gespeichert. Andernfalls werden die Anlagendaten wie gewohnt codiert.</span><span class="sxs-lookup"><span data-stu-id="37d2c-107">If the value of the **RENDDATA** structure's **dwFlags** member is set to **MAC_BINARY**, then the data for the following attachment is stored in MacBinary format; otherwise, the attachment data is encoded as usual.</span></span>
  

