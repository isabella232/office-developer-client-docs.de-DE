---
title: Index.Required-Eigenschaft (DAO)
TOCTitle: Required Property
ms:assetid: ec8fafc4-8155-c48e-b3c8-2d9be425175a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836310(v=office.15)
ms:contentKeyID: 48548518
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052963
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2660a4cb422d91cf46b98a8d3870d2ab2db73fc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703132"
---
# <a name="indexrequired-property-dao"></a><span data-ttu-id="47558-102">Index.Required-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="47558-102">Index.Required property (DAO)</span></span>

<span data-ttu-id="47558-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47558-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="47558-104">Gibt einen Wert zurück, der angibt, ob ein **[Field](field-object-dao.md)** -Objekt einen Nicht-Null-Wert erfordert, oder legt den betreffenden Wert fest.</span><span class="sxs-lookup"><span data-stu-id="47558-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="47558-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="47558-105">Syntax</span></span>

<span data-ttu-id="47558-106">*Ausdruck* . Erforderlich</span><span class="sxs-lookup"><span data-stu-id="47558-106">*expression* .Required</span></span>

<span data-ttu-id="47558-107">*Ausdruck* Eine Variable, die ein **Index** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="47558-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="47558-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47558-108">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="47558-p101">[!HINWEIS] Wenn Sie diese Eigenschaft sowohl für ein **Index**- als auch für ein **Field**-Objekt festlegen können, sollten Sie sie für das **Field**-Objekt festlegen. Die Gültigkeit des Werts dieser Eigenschaft wird zuerst für das **Field**-Objekt und erst danach für das **Index**-Objekt überprüft.</span><span class="sxs-lookup"><span data-stu-id="47558-p101">When you can set this property for either an **Index** object or a **Field** object, set it for the **Field** object. The validity of the property setting for a **Field** object is checked before that of an **Index** object.</span></span>

<span data-ttu-id="47558-111">Die Verfügbarkeit der **Required**-Eigenschaft hängt von dem Objekt ab, das die [Fields](fields-collection-dao.md)-Auflistung enthält, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="47558-111">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="47558-112">Zugehörigkeit der Fields-Auflistung</span><span class="sxs-lookup"><span data-stu-id="47558-112">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="47558-113">Required-Wert</span><span class="sxs-lookup"><span data-stu-id="47558-113">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47558-114"><strong>Index</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="47558-114"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="47558-115">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="47558-115">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47558-116"><strong>QueryDef</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="47558-116"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="47558-117">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="47558-117">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47558-118"><strong>Recordset</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="47558-118"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="47558-119">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="47558-119">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47558-120"><strong>Relation</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="47558-120"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="47558-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="47558-121">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47558-122"><strong>TableDef</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="47558-122"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="47558-123">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="47558-123">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

