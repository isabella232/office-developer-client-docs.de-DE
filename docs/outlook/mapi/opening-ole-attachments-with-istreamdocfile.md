---
title: Öffnen von OLE-Anlagen mit IStreamDocfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Letzte Änderung: 06. Juli 2012'
ms.openlocfilehash: 2de13be34e8d81f88bfba872dda6e5534eb431bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326229"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a><span data-ttu-id="5461e-103">Öffnen von OLE-Anlagen mit IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="5461e-103">Opening OLE attachments with IStreamDocfile</span></span>

<span data-ttu-id="5461e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5461e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5461e-105">Verwenden Sie beim Öffnen einer OLE-Objektanlage die **IStreamDocfile-Schnittstelle** anstelle von [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) oder [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5461e-105">When opening an OLE object attachment, use the **IStreamDocfile** interface rather than [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) or [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span></span> 

<span data-ttu-id="5461e-106">**IStreamDocfile** bietet direkten Zugriff auf das Objekt mithilfe von strukturiertem Speicher, sodass kein Kopiervorgang mehr benötigt wird und der Aufwand reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="5461e-106">**IStreamDocfile** provides direct access to the object using structured storage, eliminating the need to perform a copy operation and reducing overhead.</span></span> <span data-ttu-id="5461e-107">**IStreamDocfile** ist eine spezifische Implementierung von **IStream,** bei der der Inhalt des Datenstroms garantiert als strukturierter Speicher formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="5461e-107">**IStreamDocfile** is a specific implementation of **IStream** with the content of the stream guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="5461e-108">**IStreamDocfile** wird von Nachrichtenspeicheranbietern implementiert.</span><span class="sxs-lookup"><span data-stu-id="5461e-108">**IStreamDocfile** is implemented by message store providers.</span></span> 
  

