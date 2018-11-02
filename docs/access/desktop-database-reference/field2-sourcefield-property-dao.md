---
title: Field2.SourceField-Eigenschaft (DAO)
TOCTitle: SourceField Property
ms:assetid: f89146c1-d4a4-1129-636a-c22cf7921a4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836948(v=office.15)
ms:contentKeyID: 48548784
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 587214a5fddc5774423d2eb5af7c2a8926ee1622
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926269"
---
# <a name="field2sourcefield-property-dao"></a><span data-ttu-id="c59ee-102">Field2.SourceField-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="c59ee-102">Field2.SourceField property (DAO)</span></span>


<span data-ttu-id="c59ee-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c59ee-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c59ee-p101">Gibt einen Wert zurück, der den Namen eines Felds enthält, bei dem es sich um die ursprüngliche Datenquelle für ein **Field2**-Objekt handelt. Schreibgeschützter **String**-Wert.</span><span class="sxs-lookup"><span data-stu-id="c59ee-p101">Returns a value that indicates the name of the field that is the original source of the data for a **Field2** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c59ee-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c59ee-106">Syntax</span></span>

<span data-ttu-id="c59ee-107">*Ausdruck* . SourceField</span><span class="sxs-lookup"><span data-stu-id="c59ee-107">*expression* .SourceField</span></span>

<span data-ttu-id="c59ee-108">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c59ee-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c59ee-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c59ee-109">Remarks</span></span>

<span data-ttu-id="c59ee-110">Bei einem **Field2**-Objekt hängt die Verwendung der Eigenschaften **SourceField** und **SourceTable** vom Objekt ab, das die **Fields**-Auflistung enthält, der das **Field2**-Objekt angefügt wird (siehe folgende Tabelle).</span><span class="sxs-lookup"><span data-stu-id="c59ee-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c59ee-111">Zugehörigkeit zu Objekt</span><span class="sxs-lookup"><span data-stu-id="c59ee-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="c59ee-112">Verwendung</span><span class="sxs-lookup"><span data-stu-id="c59ee-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c59ee-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="c59ee-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="c59ee-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c59ee-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c59ee-115"><strong>QueryDef-Objekt</strong></span><span class="sxs-lookup"><span data-stu-id="c59ee-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="c59ee-116">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c59ee-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c59ee-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="c59ee-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="c59ee-118">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c59ee-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c59ee-119"><strong>Beziehung</strong></span><span class="sxs-lookup"><span data-stu-id="c59ee-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="c59ee-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c59ee-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c59ee-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="c59ee-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="c59ee-122">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c59ee-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c59ee-p102">Diese Eigenschaften geben das ursprüngliche Feld und die Tabellennamen an, die einem **Field2**-Objekt zugeordnet sind. Sie können mit diesen Eigenschaften z. B. die ursprüngliche Quelle der Daten in einem Abfragefeld ermitteln, dessen Name keinen Bezug zum Namen in der zugrunde liegenden Tabelle hat.</span><span class="sxs-lookup"><span data-stu-id="c59ee-p102">These properties indicate the original field and table names associated with a **Field2** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>

