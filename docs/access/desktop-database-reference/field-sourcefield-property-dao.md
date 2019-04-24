---
title: Field. SourceField-Eigenschaft (DAO)
TOCTitle: SourceField Property
ms:assetid: e5750d6c-4078-7bbb-9356-f9207c4e8028
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835953(v=office.15)
ms:contentKeyID: 48548360
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 249dabfa13bac6973cea4bd69e0867292c4a6967
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292993"
---
# <a name="fieldsourcefield-property-dao"></a><span data-ttu-id="c1544-102">Field. SourceField-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="c1544-102">Field.SourceField property (DAO)</span></span>


<span data-ttu-id="c1544-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c1544-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c1544-p101">Gibt einen Wert zurück, der den Namen des Felds angibt, das die ursprüngliche Quelle der Daten für ein **Field**-Objekt ist. Schreibgeschützter **String**-Wert.</span><span class="sxs-lookup"><span data-stu-id="c1544-p101">Returns a value that indicates the name of the field that is the original source of the data for a **Field** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1544-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1544-106">Syntax</span></span>

<span data-ttu-id="c1544-107">*Ausdruck* . SourceField</span><span class="sxs-lookup"><span data-stu-id="c1544-107">*expression* .SourceField</span></span>

<span data-ttu-id="c1544-108">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c1544-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1544-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1544-109">Remarks</span></span>

<span data-ttu-id="c1544-110">Bei einem **Field**-Objekt hängt die Verwendung der Eigenschaften **SourceField** und **SourceTable** vom Objekt ab, das die **Fields**-Auflistung enthält, der das **Field**-Objekt angefügt wird (siehe folgende Tabelle).</span><span class="sxs-lookup"><span data-stu-id="c1544-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c1544-111">Zugehörigkeit zu Objekt</span><span class="sxs-lookup"><span data-stu-id="c1544-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="c1544-112">Verwendung</span><span class="sxs-lookup"><span data-stu-id="c1544-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1544-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="c1544-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="c1544-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c1544-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1544-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="c1544-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="c1544-116">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c1544-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1544-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="c1544-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="c1544-118">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c1544-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1544-119"><strong>Beziehung</strong></span><span class="sxs-lookup"><span data-stu-id="c1544-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="c1544-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c1544-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1544-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="c1544-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="c1544-122">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c1544-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1544-p102">Diese Eigenschaften geben die Namen des ursprünglichen Felds und der ursprünglichen Tabelle an, die einem **Field**-Objekt zugeordnet sind. Sie können mit diesen Eigenschaften beispielsweise die ursprüngliche Quelle der Daten in einem Abfragefeld ermitteln, dessen Name in keiner Beziehung zu dem Namen des Felds der zugrunde liegenden Tabelle steht.</span><span class="sxs-lookup"><span data-stu-id="c1544-p102">These properties indicate the original field and table names associated with a **Field** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>

