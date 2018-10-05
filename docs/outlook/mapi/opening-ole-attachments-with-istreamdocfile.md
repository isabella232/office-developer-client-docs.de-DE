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
ms.openlocfilehash: 2de13be34e8d81f88bfba872dda6e5534eb431bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386551"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a><span data-ttu-id="7441e-103">OLE-Anlagen mit IStreamDocfile öffnen</span><span class="sxs-lookup"><span data-stu-id="7441e-103">Opening OLE attachments with IStreamDocfile</span></span>

<span data-ttu-id="7441e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7441e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7441e-105">Verwenden Sie beim Öffnen einer OLE-Objekt Anlage **IStreamDocfile** Schnittstelle statt [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) oder [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7441e-105">When opening an OLE object attachment, use the **IStreamDocfile** interface rather than [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) or [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span></span> 

<span data-ttu-id="7441e-106">**IStreamDocfile** bietet direkten Zugriff auf das Objekt strukturierten Speicher verwenden, führen Sie einen Kopiervorgang und der Verwaltungsaufwand reduziert die überflüssig.</span><span class="sxs-lookup"><span data-stu-id="7441e-106">**IStreamDocfile** provides direct access to the object using structured storage, eliminating the need to perform a copy operation and reducing overhead.</span></span> <span data-ttu-id="7441e-107">**IStreamDocfile** ist eine bestimmte Implementierung von **IStream** mit dem Inhalt des Datenstroms wird sichergestellt, dass als strukturierten Speicher formatiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7441e-107">**IStreamDocfile** is a specific implementation of **IStream** with the content of the stream guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="7441e-108">**IStreamDocfile** ist Zeichenfolgeneigenschaften Nachricht implementiert.</span><span class="sxs-lookup"><span data-stu-id="7441e-108">**IStreamDocfile** is implemented by message store providers.</span></span> 
  

