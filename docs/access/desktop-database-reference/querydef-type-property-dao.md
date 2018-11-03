---
title: QueryDef.Type-Eigenschaft (DAO)
TOCTitle: Type Property
ms:assetid: 03db891d-b958-7cf9-56c1-524d9ff2b9b5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844814(v=office.15)
ms:contentKeyID: 48542993
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 43e6e450021269a704650c686dea27a1d38d37f5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929510"
---
# <a name="querydeftype-property-dao"></a><span data-ttu-id="cad46-102">QueryDef.Type-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="cad46-102">QueryDef.Type property (DAO)</span></span>


<span data-ttu-id="cad46-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cad46-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cad46-p101">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück. Schreibgeschützter **Integer**-Wert.</span><span class="sxs-lookup"><span data-stu-id="cad46-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only**Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cad46-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cad46-106">Syntax</span></span>

<span data-ttu-id="cad46-107">*Ausdruck* . Typ</span><span class="sxs-lookup"><span data-stu-id="cad46-107">*expression* .Type</span></span>

<span data-ttu-id="cad46-108">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="cad46-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cad46-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cad46-109">Remarks</span></span>

<span data-ttu-id="cad46-110">Die möglichen Einstellungen und Rückgabewerte für ein **QueryDef**-Objekt sind in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cad46-110">For a **QueryDef** object, the possible settings and return values are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cad46-111">Konstante</span><span class="sxs-lookup"><span data-stu-id="cad46-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="cad46-112">Abfragetyp</span><span class="sxs-lookup"><span data-stu-id="cad46-112">Query type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cad46-113"><strong>dbQAction</strong></span><span class="sxs-lookup"><span data-stu-id="cad46-113"><strong>dbQAction</strong></span></span></p></td>
<td><p><span data-ttu-id="cad46-114">Aktion</span><span class="sxs-lookup"><span data-stu-id="cad46-114">Action</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cad46-115"><strong>dbQAppend</strong></span><span class="sxs-lookup"><span data-stu-id="cad46-115"><strong>dbQAppend</strong></span></span></p></td>
<td><p><span data-ttu-id="cad46-116">Anfügeabfrage</span><span class="sxs-lookup"><span data-stu-id="cad46-116">Append</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cad46-117"><strong>dbQCompound</strong></span><span class="sxs-lookup"><span data-stu-id="cad46-117"><strong>dbQCompound</strong></span></span></p></td>
<td><p><span data-ttu-id="cad46-118">Verbundabfrage</span><span class="sxs-lookup"><span data-stu-id="cad46-118">Compound</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cad46-119"><strong>dbQCrosstab</strong></span><span class="sxs-lookup"><span data-stu-id="cad46-119"><strong>dbQCrosstab</strong></span></span></p></td>
<td><p><span data-ttu-id="cad46-120">Kreuztabellenabfrage</span><span class="sxs-lookup"><span data-stu-id="cad46-120">Crosstab</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cad46-121"><strong>dbQDDL</strong></span><span class="sxs-lookup"><span data-stu-id="cad46-121"><strong>dbQDDL</strong></span></span></p></td>
<td><p><span data-ttu-id="cad46-122">Datendefinition</span><span class="sxs-lookup"><span data-stu-id="cad46-122">Data-definition</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cad46-123"><strong>dbQDelete</strong></span><span class="sxs-lookup"><span data-stu-id="cad46-123"><strong>dbQDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="cad46-124">Löschen</span><span class="sxs-lookup"><span data-stu-id="cad46-124">Delete</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cad46-125"><strong>dbQMakeTable</strong></span><span class="sxs-lookup"><span data-stu-id="cad46-125"><strong>dbQMakeTable</strong></span></span></p></td>
<td><p><span data-ttu-id="cad46-126">Tabellenerstellung</span><span class="sxs-lookup"><span data-stu-id="cad46-126">Make-table</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cad46-127"><strong>dbQProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="cad46-127"><strong>dbQProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="cad46-128">Prozedur (nur ODBCDirect-Arbeitsbereiche)</span><span class="sxs-lookup"><span data-stu-id="cad46-128">Procedure (ODBCDirect workspaces only)</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="cad46-p102">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cad46-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cad46-131"><strong>dbQSelect</strong></span><span class="sxs-lookup"><span data-stu-id="cad46-131"><strong>dbQSelect</strong></span></span></p></td>
<td><p><span data-ttu-id="cad46-132">Auswahlabfrage</span><span class="sxs-lookup"><span data-stu-id="cad46-132">Select</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cad46-133"><strong>dbQSetOperation</strong></span><span class="sxs-lookup"><span data-stu-id="cad46-133"><strong>dbQSetOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="cad46-134">Union-Abfrage</span><span class="sxs-lookup"><span data-stu-id="cad46-134">Union</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cad46-135"><strong>dbQSPTBulk</strong></span><span class="sxs-lookup"><span data-stu-id="cad46-135"><strong>dbQSPTBulk</strong></span></span></p></td>
<td><p><span data-ttu-id="cad46-136">Wird mit <strong>dbQSQLPassThrough</strong> verwendet, um eine Abfrage festzulegen, die keine Datensätze zurückgibt (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="cad46-136">Used with <strong>dbQSQLPassThrough</strong> to specify a query that doesn't return records (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cad46-137"><strong>dbQSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="cad46-137"><strong>dbQSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="cad46-138">Pass-Through-Abfrage (nur Microsoft Access-Arbeitsbereiche)</span><span class="sxs-lookup"><span data-stu-id="cad46-138">Pass-through (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cad46-139"><strong>dbQUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="cad46-139"><strong>dbQUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="cad46-140">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="cad46-140">Update</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cad46-141">Wenn Sie an die Auflistung eines **[Field](field-object-dao.md)** -, **[Parameter](parameter-object-dao.md)** - oder **[Property](property-object-dao.md)** -Objekts ein neues **[Index](index-object-dao.md)** -, **QueryDef**-, **[Recordset](recordset-object-dao.md)** - oder **[TableDef](tabledef-object-dao.md)** -Objekt anhängen, tritt ein Fehler auf, falls die zugrunde liegende Datenbank den für das neue Objekt angegebenen Datentyp nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cad46-141">When you append a new **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)**, or **[Property](property-object-dao.md)** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)**, or **[TableDef](tabledef-object-dao.md)** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

