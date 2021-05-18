---
title: Abrufen und Festlegen von Eigenschaften mit GetProps und SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7d11f69c6da8560f5879ebc38498d852486bed8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299398"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a><span data-ttu-id="f30ca-103">Abrufen und Festlegen von Eigenschaften mit GetProps und SetProps</span><span class="sxs-lookup"><span data-stu-id="f30ca-103">Getting and setting properties with GetProps and SetProps</span></span>
 
<span data-ttu-id="f30ca-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f30ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f30ca-105">Versuchen Sie nach Möglichkeit, eine Eigenschaft mit den [Methoden IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPIProp::SetProps abzurufen](imapiprop-setprops.md) oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f30ca-105">Whenever possible, try to retrieve or modify a property with the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="f30ca-106">Es sei denn, die Eigenschaft, mit der Sie arbeiten, ist sehr groß, diese Methoden sollten angemessen sein.</span><span class="sxs-lookup"><span data-stu-id="f30ca-106">Unless the property you are working with is very large, these methods should be adequate.</span></span> <span data-ttu-id="f30ca-107">Die andere Alternative besteht im Lesen oder Schreiben in einen Datenstrom mit der [IStream-Schnittstelle.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f30ca-107">The other alternative is to read from or write to a stream with the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="f30ca-108">Streams können sehr große Eigenschaften erfolgreich verarbeiten, aber sie sind eine höhere Ressourcenentleerung, da sie die COM-Bibliotheken erfordern.</span><span class="sxs-lookup"><span data-stu-id="f30ca-108">Streams can handle very large properties successfully, but they are a greater drain on resources because they require the COM libraries.</span></span> <span data-ttu-id="f30ca-109">Verwenden Sie **die IStream-Schnittstelle** nur, nachdem Der Aufruf von **IMAPIProp::GetProps** oder **IMAPIProp::SetProps fehlschlägt.**</span><span class="sxs-lookup"><span data-stu-id="f30ca-109">Use the **IStream** interface only after your call to **IMAPIProp::GetProps** or **IMAPIProp::SetProps** fails.</span></span> 
  

