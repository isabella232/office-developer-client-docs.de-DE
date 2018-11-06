---
title: Connection.CreateQueryDef-Methode (DAO)
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
ms.openlocfilehash: 681da274ab1f709da2eb614df038e6aa492a224a
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997252"
---
# <a name="connectioncreatequerydef-method-dao"></a><span data-ttu-id="5a952-102">Connection.CreateQueryDef-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="5a952-102">Connection.CreateQueryDef method (DAO)</span></span>

<span data-ttu-id="5a952-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a952-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5a952-104">Erstellt ein neues **[QueryDef](querydef-object-dao.md)** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="5a952-104">Creates a new **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a952-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a952-105">Syntax</span></span>

<span data-ttu-id="5a952-106">*Ausdruck* . CreateQueryDef (***Name***, ***SQLText***)</span><span class="sxs-lookup"><span data-stu-id="5a952-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span></span>

<span data-ttu-id="5a952-107">*Ausdruck* Eine Variable, die ein **Connection** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="5a952-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="5a952-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a952-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a952-109">Name</span><span class="sxs-lookup"><span data-stu-id="5a952-109">Name</span></span></p></th>
<th><p><span data-ttu-id="5a952-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="5a952-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="5a952-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5a952-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="5a952-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a952-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a952-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="5a952-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="5a952-114">Optional</span><span class="sxs-lookup"><span data-stu-id="5a952-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="5a952-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="5a952-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="5a952-116">Eine <strong>Variant</strong> (Untertyp <strong>String</strong>), die die neue <strong>QueryDef</strong> eindeutig benennt.</span><span class="sxs-lookup"><span data-stu-id="5a952-116">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a952-117"><em>SQLText</em></span><span class="sxs-lookup"><span data-stu-id="5a952-117"><em>SQLText</em></span></span></p></td>
<td><p><span data-ttu-id="5a952-118">Optional</span><span class="sxs-lookup"><span data-stu-id="5a952-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="5a952-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="5a952-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="5a952-p101">Eine <strong>Variant</strong> (Untertyp <strong>String</strong>), bei er es sich um eine SQL Anweisung handelt, die die <strong>QueryDef</strong> definiert. Wenn dieses Argument ausgelassen wird, können Sie die <strong>QueryDef</strong> durch Festlegen ihrer <strong><a href="querydef-sql-property-dao.md">SQL</a></strong>-Eigenschaft definieren, bevor oder nachdem Sie sie an eine Auflistung anfügen.</span><span class="sxs-lookup"><span data-stu-id="5a952-p101">A <strong>Variant</strong> (<strong>String</strong> subtype) that is an SQL statement defining the <strong>QueryDef</strong>. If you omit this argument, you can define the <strong>QueryDef</strong> by setting its <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> property before or after you append it to a collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="5a952-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a952-122">Return value</span></span>

<span data-ttu-id="5a952-123">QueryDef-Objekt</span><span class="sxs-lookup"><span data-stu-id="5a952-123">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="5a952-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5a952-124">Remarks</span></span>

<span data-ttu-id="5a952-125">Wenn Sie in einem Microsoft Access-Arbeitsbereich beim Erstellen eines **QueryDef**-Objekts für den Namen einen anderen Wert angeben als eine leere Zeichenfolge, wird das resultierende **QueryDef**-Objekt automatisch an die **[QueryDefs](querydefs-collection-dao.md)** -Auflistung angefügt.</span><span class="sxs-lookup"><span data-stu-id="5a952-125">In a Microsoft Access workspace, if you provide anything other than a zero-length string for the name when you create a **QueryDef**, the resulting **QueryDef** object is automatically appended to the **[QueryDefs](querydefs-collection-dao.md)** collection.</span></span>

<span data-ttu-id="5a952-126">Wenn das durch Name angegebene Objekt bereits ein Mitglied der **QueryDefs** -Auflistung ist, tritt ein Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="5a952-126">If the object specified by name is already a member of the **QueryDefs** collection, a run-time error occurs.</span></span> <span data-ttu-id="5a952-127">Sie können eine temporäre **QueryDef-Objekt** erstellen, indem Sie eine leere Zeichenfolge für das Namenargument verwenden, wenn Sie die **CreateQueryDef** -Methode ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a952-127">You can create a temporary **QueryDef** by using a zero-length string for the name argument when you execute the **CreateQueryDef** method.</span></span> <span data-ttu-id="5a952-128">Sie können aber auch die **[Name](connection-name-property-dao.md)** -Eigenschaft eines neu erstellten **QueryDef**-Objekts auf eine leere Zeichenfolge ("") festlegen.</span><span class="sxs-lookup"><span data-stu-id="5a952-128">You can also accomplish this by setting the **[Name](connection-name-property-dao.md)** property of a newly created **QueryDef** to a zero-length string ("").</span></span> <span data-ttu-id="5a952-129">Temporäre **QueryDef**-Objekte sind nützlich, wenn Sie dynamische SQL-Anweisungen mehrmals verwenden möchten, ohne dass Sie neue permanente Objekte in der **QueryDefs**-Auflistung erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="5a952-129">Temporary **QueryDef** objects are useful if you want to repeatedly use dynamic SQL statements without having to create any new permanent objects in the **QueryDefs** collection.</span></span> <span data-ttu-id="5a952-130">Sie können ein temporäres **QueryDef**-Objekt nicht an jede Auflistung anfügen, da eine leere Zeichenfolge kein gültiger Name für ein permanentes **QueryDef**-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="5a952-130">You can't append a temporary **QueryDef** to any collection because a zero-length string isn't a valid name for a permanent **QueryDef** object.</span></span> <span data-ttu-id="5a952-131">Sie haben jedoch immer die Möglichkeit, die **Name**- und **SQL**-Eigenschaften des neu erstellten **QueryDef**-Objekts festzulegen und anschließend das **QueryDef**-Objekt an die **QueryDefs**-Auflistung anzufügen.</span><span class="sxs-lookup"><span data-stu-id="5a952-131">You can always set the **Name** and **SQL** properties of the newly created **QueryDef** object and subsequently append the **QueryDef** to the **QueryDefs** collection.</span></span>

<span data-ttu-id="5a952-132">Verwenden Sie zum Ausführen der SQL-Anweisung in einem **QueryDef**-Objekt die **[Execute](connection-execute-method-dao.md)** - oder **[OpenRecordset](connection-openrecordset-method-dao.md)** -Methode.</span><span class="sxs-lookup"><span data-stu-id="5a952-132">To run the SQL statement in a **QueryDef** object, use the **[Execute](connection-execute-method-dao.md)** or **[OpenRecordset](connection-openrecordset-method-dao.md)** method.</span></span>

<span data-ttu-id="5a952-133">Das Verwenden eines **QueryDef**-Objekts ist die empfohlene Methode für SQL Pass-Through-Abfragen in ODBC-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="5a952-133">Using a **QueryDef** object is the preferred way to perform SQL pass-through queries with ODBC databases.</span></span>

<span data-ttu-id="5a952-134">Verwenden Sie die \*\*\*\*Delete\*\*\*\* -Methode für die Auflistung, um ein [QueryDef](fields-delete-method-dao.md)-Objekt aus einer **QueryDefs**-Auflistung in einer Microsoft Access-Datenbank zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="5a952-134">To remove a **QueryDef** object from a **QueryDefs** collection in a Microsoft Access database engine database, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

