---
title: Name-Eigenschaft (ADO MD)
TOCTitle: Name property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4e27870a0c1dbb38b7c0be31c439a95f6aae671
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704154"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="0b77f-102">Name-Eigenschaft (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="0b77f-102">Name property (ADO MD)</span></span>


<span data-ttu-id="0b77f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b77f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0b77f-104">Gibt den Namen eines Objekts an.</span><span class="sxs-lookup"><span data-stu-id="0b77f-104">Indicates the name of an object.</span></span>

## <a name="return-values"></a><span data-ttu-id="0b77f-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="0b77f-105">Return values</span></span>

<span data-ttu-id="0b77f-106">Gibt einen schreibgeschützten **String** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0b77f-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b77f-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0b77f-107">Remarks</span></span>

<span data-ttu-id="0b77f-p101">Sie können die **Name** -Eigenschaft eines Objekts durch einen Ordinalverweis abrufen. Danach können Sie auf das Objekt direkt durch seinen Namen verweisen. Wenn z. B. "cdf.CubeDefs(0).Name" die Zeichenfolge "Bobs Video Store" zurückgibt, können Sie auf dieses [CubeDef](cubedef-object-ado-md.md)-Objekt durch die Zeichenfolge "cdf.CubeDefs("Bobs Video Store") verweisen.</span><span class="sxs-lookup"><span data-stu-id="0b77f-p101">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name. For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>

