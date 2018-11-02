---
title: Field.SourceTable-Eigenschaft (DAO)
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
ms.openlocfilehash: 6bd096b8989cefe48df882d447aab0d4f3d0a6ee
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925198"
---
# <a name="fieldsourcetable-property-dao"></a><span data-ttu-id="2cb2e-102">Field.SourceTable-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="2cb2e-102">Field.SourceTable property (DAO)</span></span>


<span data-ttu-id="2cb2e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2cb2e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2cb2e-p101">Gibt einen Wert zurück, der den Namen einer Tabelle enthält, bei der es sich um die ursprüngliche Datenquelle für ein **Field**-Objekt handelt. Schreibgeschützter **String**-Wert.</span><span class="sxs-lookup"><span data-stu-id="2cb2e-p101">Returns a value that indicates the name of the table that is the original source of the data for a **Field** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cb2e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cb2e-106">Syntax</span></span>

<span data-ttu-id="2cb2e-107">*Ausdruck* . SourceTable</span><span class="sxs-lookup"><span data-stu-id="2cb2e-107">*expression* .SourceTable</span></span>

<span data-ttu-id="2cb2e-108">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="2cb2e-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cb2e-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2cb2e-109">Remarks</span></span>

<span data-ttu-id="2cb2e-110">Bei einem **Field**-Objekt hängt die Verwendung der Eigenschaften **SourceField** und **SourceTable** vom Objekt ab, das die **Fields**-Auflistung enthält, der das **Field**-Objekt angefügt wird (siehe folgende Tabelle).</span><span class="sxs-lookup"><span data-stu-id="2cb2e-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2cb2e-111">Zugehörigkeit zu Objekt</span><span class="sxs-lookup"><span data-stu-id="2cb2e-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="2cb2e-112">Verwendung</span><span class="sxs-lookup"><span data-stu-id="2cb2e-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2cb2e-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="2cb2e-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="2cb2e-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2cb2e-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cb2e-115"><strong>QueryDef-Objekt</strong></span><span class="sxs-lookup"><span data-stu-id="2cb2e-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="2cb2e-116">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2cb2e-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cb2e-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="2cb2e-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="2cb2e-118">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2cb2e-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cb2e-119"><strong>Beziehung</strong></span><span class="sxs-lookup"><span data-stu-id="2cb2e-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="2cb2e-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2cb2e-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cb2e-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="2cb2e-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="2cb2e-122">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2cb2e-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2cb2e-p102">Diese Eigenschaften geben das ursprüngliche Feld und die Tabellennamen an, die einem **Field**-Objekt zugeordnet sind. Sie können mit diesen Eigenschaften z. B. die ursprüngliche Quelle der Daten in einem Abfragefeld ermitteln, dessen Name keinen Bezug zum Namen in der zugrunde liegenden Tabelle hat.</span><span class="sxs-lookup"><span data-stu-id="2cb2e-p102">These properties indicate the original field and table names associated with a **Field** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2cb2e-125">Die SourceTable-Eigenschaft gibt keinen sinnvollen Tabellenamen zurück, wenn sie für ein Field-Objekt in der Fields-Auflistung eines Recordset-Objekts vom Typ Tabelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2cb2e-125">The <STRONG>SourceTable</STRONG> property will not return a meaningful table name if used on a <STRONG>Field</STRONG> object in the <STRONG>Fields</STRONG> collection of a table-type <STRONG>Recordset</STRONG> object.</span></span></P>


