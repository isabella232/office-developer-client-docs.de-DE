---
title: Name-Eigenschaft (ADO MD)
TOCTitle: Name Property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 63e098a8b97bb37fad2ef256affb2da142daf434
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878647"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="f8785-102">Name-Eigenschaft (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="f8785-102">Name Property (ADO MD)</span></span>


<span data-ttu-id="f8785-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8785-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f8785-104">Gibt den Namen eines Objekts an.</span><span class="sxs-lookup"><span data-stu-id="f8785-104">Indicates the name of an object.</span></span>

## <a name="return-values"></a><span data-ttu-id="f8785-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f8785-105">Return values</span></span>

<span data-ttu-id="f8785-106">Gibt einen schreibgeschützten **String** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f8785-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8785-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f8785-107">Remarks</span></span>

<span data-ttu-id="f8785-p101">Sie können die **Name** -Eigenschaft eines Objekts durch einen Ordinalverweis abrufen. Danach können Sie auf das Objekt direkt durch seinen Namen verweisen. Wenn z. B. "cdf.CubeDefs(0).Name" die Zeichenfolge "Bobs Video Store" zurückgibt, können Sie auf dieses [CubeDef](cubedef-object-ado-md.md)-Objekt durch die Zeichenfolge "cdf.CubeDefs("Bobs Video Store") verweisen.</span><span class="sxs-lookup"><span data-stu-id="f8785-p101">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name. For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>

