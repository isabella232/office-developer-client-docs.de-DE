---
title: Field.SourceField Property (DAO)
TOCTitle: SourceField Property
ms:assetid: e5750d6c-4078-7bbb-9356-f9207c4e8028
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835953(v=office.15)
ms:contentKeyID: 48548360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a769cd242064ae9f1fef91c787e614610aab48a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869372"
---
# <a name="fieldsourcefield-property-dao"></a><span data-ttu-id="41390-102">Field.SourceField Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="41390-102">Field.SourceField Property (DAO)</span></span>


<span data-ttu-id="41390-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="41390-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="41390-p101">Gibt einen Wert zurück, der den Namen des Felds angibt, das die ursprüngliche Quelle der Daten für ein **Field**-Objekt ist. Schreibgeschützter **String**-Wert.</span><span class="sxs-lookup"><span data-stu-id="41390-p101">Returns a value that indicates the name of the field that is the original source of the data for a **Field** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="41390-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="41390-106">Syntax</span></span>

<span data-ttu-id="41390-107">*Ausdruck* . SourceField</span><span class="sxs-lookup"><span data-stu-id="41390-107">*expression* .SourceField</span></span>

<span data-ttu-id="41390-108">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="41390-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="41390-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41390-109">Remarks</span></span>

<span data-ttu-id="41390-110">Bei einem **Field**-Objekt hängt die Verwendung der Eigenschaften **SourceField** und **SourceTable** vom Objekt ab, das die **Fields**-Auflistung enthält, der das **Field**-Objekt angefügt wird (siehe folgende Tabelle).</span><span class="sxs-lookup"><span data-stu-id="41390-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="41390-111">Zugehörigkeit zu Objekt</span><span class="sxs-lookup"><span data-stu-id="41390-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="41390-112">Verwendung</span><span class="sxs-lookup"><span data-stu-id="41390-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41390-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="41390-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="41390-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="41390-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41390-115"><strong>QueryDef-Objekt</strong></span><span class="sxs-lookup"><span data-stu-id="41390-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="41390-116">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="41390-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41390-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="41390-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="41390-118">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="41390-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41390-119"><strong>Beziehung</strong></span><span class="sxs-lookup"><span data-stu-id="41390-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="41390-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="41390-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41390-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="41390-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="41390-122">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="41390-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="41390-p102">Diese Eigenschaften geben die Namen des ursprünglichen Felds und der ursprünglichen Tabelle an, die einem **Field**-Objekt zugeordnet sind. Sie können mit diesen Eigenschaften beispielsweise die ursprüngliche Quelle der Daten in einem Abfragefeld ermitteln, dessen Name in keiner Beziehung zu dem Namen des Felds der zugrunde liegenden Tabelle steht.</span><span class="sxs-lookup"><span data-stu-id="41390-p102">These properties indicate the original field and table names associated with a **Field** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>

