---
title: FieldEnum (Access Desktop Database Reference)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e42dcfe63194364986e5b235c59b011231307a7c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292594"
---
# <a name="fieldenum"></a><span data-ttu-id="bea7f-102">FieldEnum</span><span class="sxs-lookup"><span data-stu-id="bea7f-102">FieldEnum</span></span>

<span data-ttu-id="bea7f-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bea7f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bea7f-104">Gibt die speziellen Felder an, auf die in der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="bea7f-104">Specifies the special fields referenced in a [Record](record-object-ado.md) object's [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="bea7f-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bea7f-105">Remarks</span></span>

<span data-ttu-id="bea7f-p101">These constants provide a "shortcut" to accessing special fields associated with a **Record**. Retrieve the [Field](field-object-ado.md) object from the **Fields** collection, and then obtain its contents with the **Field** object's [Value](value-property-ado.md) property.</span><span class="sxs-lookup"><span data-stu-id="bea7f-p101">These constants provide a "shortcut" to accessing special fields associated with a **Record**. Retrieve the [Field](field-object-ado.md) object from the **Fields** collection, and then obtain its contents with the **Field** object's [Value](value-property-ado.md) property.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bea7f-108">Konstante</span><span class="sxs-lookup"><span data-stu-id="bea7f-108">Constant</span></span></p></th>
<th><p><span data-ttu-id="bea7f-109">Wert</span><span class="sxs-lookup"><span data-stu-id="bea7f-109">Value</span></span></p></th>
<th><p><span data-ttu-id="bea7f-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bea7f-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bea7f-111"><strong>adDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="bea7f-111"><strong>adDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="bea7f-112">-1</span><span class="sxs-lookup"><span data-stu-id="bea7f-112">-1</span></span></p></td>
<td><p><span data-ttu-id="bea7f-113">Verweist auf das Feld mit dem <a href="stream-object-ado.md">Stream</a> -Standardobjekt, das einem <strong>Datensatz</strong>zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bea7f-113">References the field containing the default <a href="stream-object-ado.md">Stream</a> object associated with a <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bea7f-114"><strong>adRecordURL</strong></span><span class="sxs-lookup"><span data-stu-id="bea7f-114"><strong>adRecordURL</strong></span></span></p></td>
<td><p><span data-ttu-id="bea7f-115">-2</span><span class="sxs-lookup"><span data-stu-id="bea7f-115">-2</span></span></p></td>
<td><p><span data-ttu-id="bea7f-116">Verweist auf das Feld, das die absolute URL-Zeichenfolge für den aktuellen Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="bea7f-116">References the field containing the absolute URL string for the current <strong>Record</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

