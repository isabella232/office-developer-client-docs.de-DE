---
title: Connection. CreateQueryDef-Methode (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 254fe81a-9b45-e8e7-108d-503c1c1c0fcc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191860(v=office.15)
ms:contentKeyID: 48543781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053067
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b6600d4508a33a31098d6a2e7c92f5904beb0e95
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295933"
---
# <a name="connectioncreatequerydef-method-dao"></a><span data-ttu-id="8e868-102">Connection. CreateQueryDef-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="8e868-102">Connection.CreateQueryDef method (DAO)</span></span>

<span data-ttu-id="8e868-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e868-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8e868-104">Erstellt ein neues **[QueryDef](querydef-object-dao.md)** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8e868-104">Creates a new **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e868-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e868-105">Syntax</span></span>

<span data-ttu-id="8e868-106">*Ausdruck* . CreateQueryDef (***Name***, ***sqltext***)</span><span class="sxs-lookup"><span data-stu-id="8e868-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span></span>

<span data-ttu-id="8e868-107">*Ausdruck* Eine Variable, die ein **Connection** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="8e868-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="8e868-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e868-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8e868-109">Name</span><span class="sxs-lookup"><span data-stu-id="8e868-109">Name</span></span></p></th>
<th><p><span data-ttu-id="8e868-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="8e868-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="8e868-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8e868-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="8e868-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e868-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e868-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="8e868-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="8e868-114">Optional</span><span class="sxs-lookup"><span data-stu-id="8e868-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="8e868-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8e868-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8e868-116">Eine <strong>Variant</strong> (Untertyp <strong>String</strong>), die die neue <strong>QueryDef</strong> eindeutig benennt.</span><span class="sxs-lookup"><span data-stu-id="8e868-116">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e868-117"><em>SQLText</em></span><span class="sxs-lookup"><span data-stu-id="8e868-117"><em>SQLText</em></span></span></p></td>
<td><p><span data-ttu-id="8e868-118">Optional</span><span class="sxs-lookup"><span data-stu-id="8e868-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="8e868-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8e868-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8e868-120">Eine <strong>Variant</strong> (Untertyp <strong>String</strong>), bei er es sich um eine SQL Anweisung handelt, die die <strong>QueryDef</strong> definiert.</span><span class="sxs-lookup"><span data-stu-id="8e868-120">A <strong>Variant</strong> (<strong>String</strong> subtype) that is an SQL statement defining the <strong>QueryDef</strong>.</span></span> <span data-ttu-id="8e868-121">Wenn dieses Argument ausgelassen wird, können Sie die <strong>QueryDef</strong> durch Festlegen ihrer <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> -Eigenschaft definieren, bevor oder nachdem Sie sie an eine Auflistung anfügen.</span><span class="sxs-lookup"><span data-stu-id="8e868-121">If you omit this argument, you can define the <strong>QueryDef</strong> by setting its <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> property before or after you append it to a collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="8e868-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e868-122">Return value</span></span>

<span data-ttu-id="8e868-123">QueryDef</span><span class="sxs-lookup"><span data-stu-id="8e868-123">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="8e868-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e868-124">Remarks</span></span>

<span data-ttu-id="8e868-125">Wenn Sie in einem Microsoft Access-Arbeitsbereich bei der Erstellung einer **QueryDef** einen anderen Wert als eine Zeichenfolge der Länge 0 (null) für den Namen angeben, wird das resultierende **QueryDef** -Objekt automatisch an die **[QueryDefs](querydefs-collection-dao.md)** -Auflistung angefügt.</span><span class="sxs-lookup"><span data-stu-id="8e868-125">In a Microsoft Access workspace, if you provide anything other than a zero-length string for the name when you create a **QueryDef**, the resulting **QueryDef** object is automatically appended to the **[QueryDefs](querydefs-collection-dao.md)** collection.</span></span>

<span data-ttu-id="8e868-126">Wenn das durch Name angegebene Objekt bereits ein Element der **Querydefs** -Auflistung ist, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="8e868-126">If the object specified by name is already a member of the **QueryDefs** collection, a run-time error occurs.</span></span> <span data-ttu-id="8e868-127">Sie können eine temporäre **QueryDef** mithilfe einer leeren Zeichenfolge für das Argument Name erstellen, wenn Sie die **CreateQueryDef** -Methode ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e868-127">You can create a temporary **QueryDef** by using a zero-length string for the name argument when you execute the **CreateQueryDef** method.</span></span> <span data-ttu-id="8e868-128">Ein andere Methode besteht darin, die **[Name](connection-name-property-dao.md)** -Eigenschaft einer neu erstellten **QueryDef** auf eine Zeichenfolge der Länge 0 ("") festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8e868-128">You can also accomplish this by setting the **[Name](connection-name-property-dao.md)** property of a newly created **QueryDef** to a zero-length string ("").</span></span> <span data-ttu-id="8e868-129">Temporäre **QueryDef** -Objekte sind nützlich, wenn Sie dynamische SQL-Anweisungen wiederholt verwenden möchten, ohne neue dauerhafte Objekte in der **QueryDefs** -Auflistung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8e868-129">Temporary **QueryDef** objects are useful if you want to repeatedly use dynamic SQL statements without having to create any new permanent objects in the **QueryDefs** collection.</span></span> <span data-ttu-id="8e868-130">Sie können eine temporäre **QueryDef** nicht an eine Auflistung anfügen, da eine Zeichenfolge der Länge 0 (null) kein gültiger Name für ein dauerhaftes **QueryDef** -Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="8e868-130">You can't append a temporary **QueryDef** to any collection because a zero-length string isn't a valid name for a permanent **QueryDef** object.</span></span> <span data-ttu-id="8e868-131">Sie können immer die Eigenschaften **Name** und **SQL** des neu erstellten **QueryDef** -Objekts festlegen und die **QueryDef** anschließend an die **QueryDefs** -Auflistung anfügen.</span><span class="sxs-lookup"><span data-stu-id="8e868-131">You can always set the **Name** and **SQL** properties of the newly created **QueryDef** object and subsequently append the **QueryDef** to the **QueryDefs** collection.</span></span>

<span data-ttu-id="8e868-132">Zum Ausführen der SQL-Anweisung in einem **QueryDef** -Objekt verwenden Sie die **[Execute](connection-execute-method-dao.md)** - oder die **[OpenRecordset](connection-openrecordset-method-dao.md)** -Methode.</span><span class="sxs-lookup"><span data-stu-id="8e868-132">To run the SQL statement in a **QueryDef** object, use the **[Execute](connection-execute-method-dao.md)** or **[OpenRecordset](connection-openrecordset-method-dao.md)** method.</span></span>

<span data-ttu-id="8e868-133">Die Verwendung eines **QueryDef** -Objekts ist das bevorzugte Verfahren zum Ausführen von SQL-Pass-Through-Abfragen mit ODBC-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="8e868-133">Using a **QueryDef** object is the preferred way to perform SQL pass-through queries with ODBC databases.</span></span>

<span data-ttu-id="8e868-134">Um ein **QueryDef** -Objekt aus einer **QueryDefs** -Auflistung in einer Datenbank des Microsoft Access-Datenbankmoduls zu entfernen, führen Sie die **[Delete](fields-delete-method-dao.md)** -Methode für die Auflistung aus.</span><span class="sxs-lookup"><span data-stu-id="8e868-134">To remove a **QueryDef** object from a **QueryDefs** collection in a Microsoft Access database engine database, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

