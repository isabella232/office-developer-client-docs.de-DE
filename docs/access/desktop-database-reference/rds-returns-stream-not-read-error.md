---
title: RDS gibt den Fehler „Stream nicht gelesen“ zurück
TOCTitle: RDS returns "Stream Not Read" error
ms:assetid: 325f7b9d-8e71-bc2c-94e3-b4b4a1a2dc58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249097(v=office.15)
ms:contentKeyID: 48544075
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca0f54d8fdc7e37d0ee01f1ffd29c84a6a8ae799
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703755"
---
# <a name="rds-returns-stream-not-read-error"></a><span data-ttu-id="dc90f-102">RDS gibt \"Stream Not Read\" Fehler</span><span class="sxs-lookup"><span data-stu-id="dc90f-102">RDS returns \"Stream Not Read\" error</span></span>


<span data-ttu-id="dc90f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc90f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dc90f-p101">"The Stream object could not be read because it is empty, or the current position is at the end of the Stream. For non-empty Streams, set the current position with the Position property. To determine if a Stream is empty, check the Size property." (Das Stream-Objekt konnte nicht gelesen werden, da es leer ist oder weil sich die aktuelle Position am Ende des Streams befindet. Legen Sie bei nicht leeren Streams die aktuelle Position mithilfe der Position-Eigenschaft fest. Überprüfen Sie die Size-Eigenschaft, um festzustellen, ob der Stream leer ist.)</span><span class="sxs-lookup"><span data-stu-id="dc90f-p101">"The Stream object could not be read because it is empty, or the current position is at the end of the Stream. For non-empty Streams, set the current position with the Position property. To determine if a Stream is empty, check the Size property."</span></span>

<span data-ttu-id="dc90f-p102">Wenn die obige Fehlermeldung angezeigt wird, wurde möglicherweise versucht, eine parametrisierte hierarchische Abfrage über HTTP zu verwenden. RDS lässt keine parametrisierten Hierarchien über Remoteverbindungen zu.</span><span class="sxs-lookup"><span data-stu-id="dc90f-p102">If you get the error above, it may be a result of trying to use a parameterized hierarchical query over http. RDS does not permit you to remote parameterized hierarchies.</span></span>

