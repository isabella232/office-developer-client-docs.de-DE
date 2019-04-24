---
title: Field. sourceable-Eigenschaft (DAO)
TOCTitle: SourceTable Property
ms:assetid: 9564ea1c-eafd-0b72-fd68-d88fcc3ea189
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197694(v=office.15)
ms:contentKeyID: 48546429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052900
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a557a4941f5b4aa511489c5d057871df5fa72c08
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292986"
---
# <a name="fieldsourcetable-property-dao"></a><span data-ttu-id="4d13c-102">Field. sourceable-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="4d13c-102">Field.SourceTable property (DAO)</span></span>


<span data-ttu-id="4d13c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4d13c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4d13c-p101">Gibt einen Wert zurück, der den Namen einer Tabelle enthält, bei der es sich um die ursprüngliche Datenquelle für ein **Field**-Objekt handelt. Schreibgeschützter **String**-Wert.</span><span class="sxs-lookup"><span data-stu-id="4d13c-p101">Returns a value that indicates the name of the table that is the original source of the data for a **Field** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d13c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d13c-106">Syntax</span></span>

<span data-ttu-id="4d13c-107">*Ausdruck* . SourceTable</span><span class="sxs-lookup"><span data-stu-id="4d13c-107">*expression* .SourceTable</span></span>

<span data-ttu-id="4d13c-108">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="4d13c-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d13c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d13c-109">Remarks</span></span>

<span data-ttu-id="4d13c-110">Bei einem **Field**-Objekt hängt die Verwendung der Eigenschaften **SourceField** und **SourceTable** vom Objekt ab, das die **Fields**-Auflistung enthält, der das **Field**-Objekt angefügt wird (siehe folgende Tabelle).</span><span class="sxs-lookup"><span data-stu-id="4d13c-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4d13c-111">Zugehörigkeit zu Objekt</span><span class="sxs-lookup"><span data-stu-id="4d13c-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="4d13c-112">Verwendung</span><span class="sxs-lookup"><span data-stu-id="4d13c-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d13c-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="4d13c-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="4d13c-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4d13c-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d13c-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="4d13c-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="4d13c-116">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d13c-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d13c-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="4d13c-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="4d13c-118">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d13c-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d13c-119"><strong>Beziehung</strong></span><span class="sxs-lookup"><span data-stu-id="4d13c-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="4d13c-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4d13c-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d13c-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="4d13c-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="4d13c-122">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d13c-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4d13c-p102">Diese Eigenschaften geben das ursprüngliche Feld und die Tabellennamen an, die einem **Field**-Objekt zugeordnet sind. Sie können mit diesen Eigenschaften z. B. die ursprüngliche Quelle der Daten in einem Abfragefeld ermitteln, dessen Name keinen Bezug zum Namen in der zugrunde liegenden Tabelle hat.</span><span class="sxs-lookup"><span data-stu-id="4d13c-p102">These properties indicate the original field and table names associated with a **Field** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <span data-ttu-id="4d13c-125">The **SourceTable** property will not return a meaningful table name if used on a **Field** object in the **Fields** collection of a table-type **Recordset** object.</span><span class="sxs-lookup"><span data-stu-id="4d13c-125">The **SourceTable** property will not return a meaningful table name if used on a **Field** object in the **Fields** collection of a table-type **Recordset** object.</span></span>


