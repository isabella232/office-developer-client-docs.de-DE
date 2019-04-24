---
title: QueryDef. Type-Eigenschaft (DAO)
TOCTitle: Type Property
ms:assetid: 03db891d-b958-7cf9-56c1-524d9ff2b9b5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844814(v=office.15)
ms:contentKeyID: 48542993
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cb8856194d0b2ed14577bdc275adeb50ebdde212
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300945"
---
# <a name="querydeftype-property-dao"></a><span data-ttu-id="fbe43-102">QueryDef. Type-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="fbe43-102">QueryDef.Type property (DAO)</span></span>


<span data-ttu-id="fbe43-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fbe43-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fbe43-104">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fbe43-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="fbe43-105">Read-Only**Integer**.</span><span class="sxs-lookup"><span data-stu-id="fbe43-105">Read-only**Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbe43-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbe43-106">Syntax</span></span>

<span data-ttu-id="fbe43-107">*Ausdruck* . Typ</span><span class="sxs-lookup"><span data-stu-id="fbe43-107">*expression* .Type</span></span>

<span data-ttu-id="fbe43-108">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="fbe43-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbe43-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbe43-109">Remarks</span></span>

<span data-ttu-id="fbe43-110">Die möglichen Einstellungen und Rückgabewerte für ein **QueryDef**-Objekt sind in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fbe43-110">For a **QueryDef** object, the possible settings and return values are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fbe43-111">Konstante</span><span class="sxs-lookup"><span data-stu-id="fbe43-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="fbe43-112">Abfragetyp</span><span class="sxs-lookup"><span data-stu-id="fbe43-112">Query type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fbe43-113"><strong>dbQAction</strong></span><span class="sxs-lookup"><span data-stu-id="fbe43-113"><strong>dbQAction</strong></span></span></p></td>
<td><p><span data-ttu-id="fbe43-114">Aktion</span><span class="sxs-lookup"><span data-stu-id="fbe43-114">Action</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbe43-115"><strong>dbQAppend</strong></span><span class="sxs-lookup"><span data-stu-id="fbe43-115"><strong>dbQAppend</strong></span></span></p></td>
<td><p><span data-ttu-id="fbe43-116">Append</span><span class="sxs-lookup"><span data-stu-id="fbe43-116">Append</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbe43-117"><strong>dbQCompound</strong></span><span class="sxs-lookup"><span data-stu-id="fbe43-117"><strong>dbQCompound</strong></span></span></p></td>
<td><p><span data-ttu-id="fbe43-118">Zusammengesetzter</span><span class="sxs-lookup"><span data-stu-id="fbe43-118">Compound</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbe43-119"><strong>dbQCrosstab</strong></span><span class="sxs-lookup"><span data-stu-id="fbe43-119"><strong>dbQCrosstab</strong></span></span></p></td>
<td><p><span data-ttu-id="fbe43-120">Kreuztabellen</span><span class="sxs-lookup"><span data-stu-id="fbe43-120">Crosstab</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbe43-121"><strong>dbQDDL</strong></span><span class="sxs-lookup"><span data-stu-id="fbe43-121"><strong>dbQDDL</strong></span></span></p></td>
<td><p><span data-ttu-id="fbe43-122">Datendefinition</span><span class="sxs-lookup"><span data-stu-id="fbe43-122">Data-definition</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbe43-123"><strong>dbQDelete</strong></span><span class="sxs-lookup"><span data-stu-id="fbe43-123"><strong>dbQDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="fbe43-124">Löschen</span><span class="sxs-lookup"><span data-stu-id="fbe43-124">Delete</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbe43-125"><strong>dbQMakeTable</strong></span><span class="sxs-lookup"><span data-stu-id="fbe43-125"><strong>dbQMakeTable</strong></span></span></p></td>
<td><p><span data-ttu-id="fbe43-126">Make-Table</span><span class="sxs-lookup"><span data-stu-id="fbe43-126">Make-table</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbe43-127"><strong>dbQProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="fbe43-127"><strong>dbQProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="fbe43-128">Prozedur (nur ODBCDirect-Arbeitsbereiche)</span><span class="sxs-lookup"><span data-stu-id="fbe43-128">Procedure (ODBCDirect workspaces only)</span></span></p><p><span data-ttu-id="fbe43-129"><strong>Hinweis</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fbe43-129"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="fbe43-130">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fbe43-130">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbe43-131"><strong>dbQSelect</strong></span><span class="sxs-lookup"><span data-stu-id="fbe43-131"><strong>dbQSelect</strong></span></span></p></td>
<td><p><span data-ttu-id="fbe43-132">Auswählen</span><span class="sxs-lookup"><span data-stu-id="fbe43-132">Select</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbe43-133"><strong>dbQSetOperation</strong></span><span class="sxs-lookup"><span data-stu-id="fbe43-133"><strong>dbQSetOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="fbe43-134">Union</span><span class="sxs-lookup"><span data-stu-id="fbe43-134">Union</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbe43-135"><strong>dbQSPTBulk</strong></span><span class="sxs-lookup"><span data-stu-id="fbe43-135"><strong>dbQSPTBulk</strong></span></span></p></td>
<td><p><span data-ttu-id="fbe43-136">Wird mit <strong>dbQSQLPassThrough</strong> verwendet, um eine Abfrage festzulegen, die keine Datensätze zurückgibt (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="fbe43-136">Used with <strong>dbQSQLPassThrough</strong> to specify a query that doesn't return records (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbe43-137"><strong>dbQSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="fbe43-137"><strong>dbQSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="fbe43-138">Pass-Through-Abfrage (nur Microsoft Access-Arbeitsbereiche)</span><span class="sxs-lookup"><span data-stu-id="fbe43-138">Pass-through (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbe43-139"><strong>dbQUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="fbe43-139"><strong>dbQUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="fbe43-140">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="fbe43-140">Update</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fbe43-141">Wenn Sie an die Auflistung eines **[Field](field-object-dao.md)** -, **[Parameter](parameter-object-dao.md)** - oder **[Property](property-object-dao.md)** -Objekts ein neues **[Index](index-object-dao.md)** -, **QueryDef**-, **[Recordset](recordset-object-dao.md)** - oder **[TableDef](tabledef-object-dao.md)** -Objekt anhängen, tritt ein Fehler auf, falls die zugrunde liegende Datenbank den für das neue Objekt angegebenen Datentyp nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fbe43-141">When you append a new **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)**, or **[Property](property-object-dao.md)** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)**, or **[TableDef](tabledef-object-dao.md)** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

