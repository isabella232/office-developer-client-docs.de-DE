---
title: OLE-Anlagen mit IStreamDocfile öffnen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Zuletzt geändert: 06 Juli 2012'
ms.openlocfilehash: 33e5b9e0112f562b192400498764a10682d006a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793325"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a><span data-ttu-id="b6af9-103">OLE-Anlagen mit IStreamDocfile öffnen</span><span class="sxs-lookup"><span data-stu-id="b6af9-103">Opening OLE attachments with IStreamDocfile</span></span>

<span data-ttu-id="b6af9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6af9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6af9-105">Verwenden Sie beim Öffnen einer OLE-Objekt Anlage **IStreamDocfile** Schnittstelle statt [IStream](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380034%28v=vs.85%29.aspx) oder [IStorage](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b6af9-105">When opening an OLE object attachment, use the **IStreamDocfile** interface rather than [IStream](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380034%28v=vs.85%29.aspx) or [IStorage](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span></span> 

<span data-ttu-id="b6af9-106">**IStreamDocfile** bietet direkten Zugriff auf das Objekt strukturierten Speicher verwenden, führen Sie einen Kopiervorgang und der Verwaltungsaufwand reduziert die überflüssig.</span><span class="sxs-lookup"><span data-stu-id="b6af9-106">**IStreamDocfile** provides direct access to the object using structured storage, eliminating the need to perform a copy operation and reducing overhead.</span></span> <span data-ttu-id="b6af9-107">**IStreamDocfile** ist eine bestimmte Implementierung von **IStream** mit dem Inhalt des Datenstroms wird sichergestellt, dass als strukturierten Speicher formatiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6af9-107">**IStreamDocfile** is a specific implementation of **IStream** with the content of the stream guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="b6af9-108">**IStreamDocfile** ist Zeichenfolgeneigenschaften Nachricht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b6af9-108">**IStreamDocfile** is implemented by message store providers.</span></span> 
  

