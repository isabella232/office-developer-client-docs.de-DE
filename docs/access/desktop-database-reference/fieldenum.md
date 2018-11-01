---
title: FieldEnum (Access PC-Datenbank-Referenz)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 6975017ed8867d794dce189de74f617636b9f223
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886662"
---
# <a name="fieldenum"></a><span data-ttu-id="7ea7d-102">FieldEnum</span><span class="sxs-lookup"><span data-stu-id="7ea7d-102">FieldEnum</span></span>

<span data-ttu-id="7ea7d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ea7d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7ea7d-104">Gibt die speziellen Felder an, auf die in der [Fields](record-object-ado.md)-Auflistung eines [Record](fields-collection-ado.md)-Objekts verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7ea7d-104">Specifies the special fields referenced in a [Record](record-object-ado.md) object's [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ea7d-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7ea7d-105">Remarks</span></span>

<span data-ttu-id="7ea7d-106">Diese Konstanten bieten eine "Verknüpfung" für den Zugriff auf spezielle Felder, die einem **Datensatz**zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="7ea7d-106">These constants provide a "shortcut" to accessing special fields associated with a **Record**.</span></span> <span data-ttu-id="7ea7d-107">Das [Field](field-object-ado.md) -Objekt aus der **Fields** -Auflistung abrufen, und klicken Sie dann seinen Inhalt mit der [Value](value-property-ado.md) -Eigenschaft für das **Field** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7ea7d-107">Retrieve the [Field](field-object-ado.md) object from the **Fields** collection, and then obtain its contents with the **Field** object's [Value](value-property-ado.md) property.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7ea7d-108">Konstante</span><span class="sxs-lookup"><span data-stu-id="7ea7d-108">Constant</span></span></p></th>
<th><p><span data-ttu-id="7ea7d-109">Wert</span><span class="sxs-lookup"><span data-stu-id="7ea7d-109">Value</span></span></p></th>
<th><p><span data-ttu-id="7ea7d-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ea7d-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ea7d-111"><strong>adDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="7ea7d-111"><strong>adDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="7ea7d-112">-1</span><span class="sxs-lookup"><span data-stu-id="7ea7d-112">-1</span></span></p></td>
<td><p><span data-ttu-id="7ea7d-113">Verweist auf das Feld, das einem <strong>Datensatz</strong>zugeordnete <a href="stream-object-ado.md">Stream</a> -Standardobjekt enthält.</span><span class="sxs-lookup"><span data-stu-id="7ea7d-113">References the field containing the default <a href="stream-object-ado.md">Stream</a> object associated with a <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ea7d-114"><strong>adRecordURL</strong></span><span class="sxs-lookup"><span data-stu-id="7ea7d-114"><strong>adRecordURL</strong></span></span></p></td>
<td><p><span data-ttu-id="7ea7d-115">-2</span><span class="sxs-lookup"><span data-stu-id="7ea7d-115">-2</span></span></p></td>
<td><p><span data-ttu-id="7ea7d-116">Verweist auf das Feld, enthält die absolute URL-Zeichenfolge für den aktuellen <strong>Datensatz</strong>.</span><span class="sxs-lookup"><span data-stu-id="7ea7d-116">References the field containing the absolute URL string for the current <strong>Record</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

