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
ms.openlocfilehash: d58fc0eae5401773d28f5bbe510913ff381ade8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427136"
---
# <a name="attattachrenddata"></a><span data-ttu-id="162bd-103">attAttachRenddata</span><span class="sxs-lookup"><span data-stu-id="162bd-103">attAttachRenddata</span></span>

  
  
<span data-ttu-id="162bd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="162bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="162bd-105">Das **attAttachRenddata-Attribut** wird als **RENDDATA-Struktur** codiert, die beschreibt, wie und wo die Anlage im Nachrichtentext gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="162bd-105">The **attAttachRenddata** attribute is encoded as a **RENDDATA** structure that describes how and where the attachment is rendered in the message text.</span></span> <span data-ttu-id="162bd-106">Die **RENDDATA-Struktur** wird einfach im TNEF-Stream als **sizeof(RENDDATA)-Bytes** codiert, beginnend mit dem ersten Element der **RENDDATA-Struktur.**</span><span class="sxs-lookup"><span data-stu-id="162bd-106">The **RENDDATA** structure is simply encoded in the TNEF stream as **sizeof(RENDDATA)** bytes beginning with the first member of the **RENDDATA** structure.</span></span> <span data-ttu-id="162bd-107">Wenn der Wert des **dwFlags-Mitglieds** der **RENDDATA-Struktur** auf **MAC_BINARY** festgelegt ist, werden die Daten für die folgende Anlage im MacBinary-Format gespeichert. Andernfalls werden die Anlagendaten wie gewohnt codiert.</span><span class="sxs-lookup"><span data-stu-id="162bd-107">If the value of the **RENDDATA** structure's **dwFlags** member is set to **MAC_BINARY**, then the data for the following attachment is stored in MacBinary format; otherwise, the attachment data is encoded as usual.</span></span>
  

