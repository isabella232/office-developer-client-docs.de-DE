---
title: Connection.CreateQueryDef Method (DAO)
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
ms.openlocfilehash: 5ea0e06d133c95506a68e947254bfcd0ea8a2dc6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880306"
---
# <a name="connectioncreatequerydef-method-dao"></a><span data-ttu-id="ab3a4-102">Connection.CreateQueryDef Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="ab3a4-102">Connection.CreateQueryDef Method (DAO)</span></span>


<span data-ttu-id="ab3a4-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab3a4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ab3a4-104">Erstellt ein neues **[QueryDef](querydef-object-dao.md)** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="ab3a4-104">Creates a new **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab3a4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab3a4-105">Syntax</span></span>

<span data-ttu-id="ab3a4-106">*Ausdruck* . CreateQueryDef (***Name***, ***SQLText***)</span><span class="sxs-lookup"><span data-stu-id="ab3a4-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span></span>

<span data-ttu-id="ab3a4-107">*Ausdruck* Eine Variable, die ein **Connection** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="ab3a4-107">*expression* A variable that represents a **Connection** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="ab3a4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab3a4-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ab3a4-109">Name</span><span class="sxs-lookup"><span data-stu-id="ab3a4-109">Name</span></span></p></th>
<th><p><span data-ttu-id="ab3a4-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="ab3a4-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="ab3a4-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ab3a4-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="ab3a4-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab3a4-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab3a4-113">Name</span><span class="sxs-lookup"><span data-stu-id="ab3a4-113">Name</span></span></p></td>
<td><p><span data-ttu-id="ab3a4-114">Optional</span><span class="sxs-lookup"><span data-stu-id="ab3a4-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="ab3a4-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ab3a4-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ab3a4-116">Eine <strong>Variant</strong> (Untertyp <strong>String</strong>), die die neue <strong>QueryDef</strong> eindeutig benennt.</span><span class="sxs-lookup"><span data-stu-id="ab3a4-116">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab3a4-117">SQLText</span><span class="sxs-lookup"><span data-stu-id="ab3a4-117">SQLText</span></span></p></td>
<td><p><span data-ttu-id="ab3a4-118">Optional</span><span class="sxs-lookup"><span data-stu-id="ab3a4-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="ab3a4-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ab3a4-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ab3a4-p101">Eine <strong>Variant</strong> (Untertyp <strong>String</strong>), bei er es sich um eine SQL Anweisung handelt, die die <strong>QueryDef</strong> definiert. Wenn dieses Argument ausgelassen wird, können Sie die <strong>QueryDef</strong> durch Festlegen ihrer <strong><a href="querydef-sql-property-dao.md">SQL</a></strong>-Eigenschaft definieren, bevor oder nachdem Sie sie an eine Auflistung anfügen.</span><span class="sxs-lookup"><span data-stu-id="ab3a4-p101">A <strong>Variant</strong> (<strong>String</strong> subtype) that is an SQL statement defining the <strong>QueryDef</strong>. If you omit this argument, you can define the <strong>QueryDef</strong> by setting its <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> property before or after you append it to a collection.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="ab3a4-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab3a4-122">Return value</span></span>

<span data-ttu-id="ab3a4-123">QueryDef-Objekt</span><span class="sxs-lookup"><span data-stu-id="ab3a4-123">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="ab3a4-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ab3a4-124">Remarks</span></span>

<span data-ttu-id="ab3a4-125">Wenn Sie in einem Microsoft Access-Arbeitsbereich beim Erstellen eines **QueryDef**-Objekts für den Namen einen anderen Wert angeben als eine leere Zeichenfolge, wird das resultierende **QueryDef**-Objekt automatisch an die **[QueryDefs](querydefs-collection-dao.md)** -Auflistung angefügt.</span><span class="sxs-lookup"><span data-stu-id="ab3a4-125">In a Microsoft Access workspace, if you provide anything other than a zero-length string for the name when you create a **QueryDef**, the resulting **QueryDef** object is automatically appended to the **[QueryDefs](querydefs-collection-dao.md)** collection.</span></span>

<span data-ttu-id="ab3a4-126">Wenn das durch Name angegebene Objekt bereits ein Mitglied der **QueryDefs** -Auflistung ist, tritt ein Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="ab3a4-126">If the object specified by name is already a member of the **QueryDefs** collection, a run-time error occurs.</span></span> <span data-ttu-id="ab3a4-127">Sie können eine temporäre **QueryDef-Objekt** erstellen, indem Sie eine leere Zeichenfolge für das Namenargument verwenden, wenn Sie die **CreateQueryDef** -Methode ausführen.</span><span class="sxs-lookup"><span data-stu-id="ab3a4-127">You can create a temporary **QueryDef** by using a zero-length string for the name argument when you execute the **CreateQueryDef** method.</span></span> <span data-ttu-id="ab3a4-128">Sie können aber auch die **[Name](connection-name-property-dao.md)** -Eigenschaft eines neu erstellten **QueryDef**-Objekts auf eine leere Zeichenfolge ("") festlegen.</span><span class="sxs-lookup"><span data-stu-id="ab3a4-128">You can also accomplish this by setting the **[Name](connection-name-property-dao.md)** property of a newly created **QueryDef** to a zero-length string ("").</span></span> <span data-ttu-id="ab3a4-129">Temporäre **QueryDef**-Objekte sind nützlich, wenn Sie dynamische SQL-Anweisungen mehrmals verwenden möchten, ohne dass Sie neue permanente Objekte in der **QueryDefs**-Auflistung erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="ab3a4-129">Temporary **QueryDef** objects are useful if you want to repeatedly use dynamic SQL statements without having to create any new permanent objects in the **QueryDefs** collection.</span></span> <span data-ttu-id="ab3a4-130">Sie können ein temporäres **QueryDef**-Objekt nicht an jede Auflistung anfügen, da eine leere Zeichenfolge kein gültiger Name für ein permanentes **QueryDef**-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="ab3a4-130">You can't append a temporary **QueryDef** to any collection because a zero-length string isn't a valid name for a permanent **QueryDef** object.</span></span> <span data-ttu-id="ab3a4-131">Sie haben jedoch immer die Möglichkeit, die **Name**- und **SQL**-Eigenschaften des neu erstellten **QueryDef**-Objekts festzulegen und anschließend das **QueryDef**-Objekt an die **QueryDefs**-Auflistung anzufügen.</span><span class="sxs-lookup"><span data-stu-id="ab3a4-131">You can always set the **Name** and **SQL** properties of the newly created **QueryDef** object and subsequently append the **QueryDef** to the **QueryDefs** collection.</span></span>

<span data-ttu-id="ab3a4-132">Verwenden Sie zum Ausführen der SQL-Anweisung in einem **QueryDef**-Objekt die **[Execute](connection-execute-method-dao.md)** - oder **[OpenRecordset](connection-openrecordset-method-dao.md)** -Methode.</span><span class="sxs-lookup"><span data-stu-id="ab3a4-132">To run the SQL statement in a **QueryDef** object, use the **[Execute](connection-execute-method-dao.md)** or **[OpenRecordset](connection-openrecordset-method-dao.md)** method.</span></span>

<span data-ttu-id="ab3a4-133">Das Verwenden eines **QueryDef**-Objekts ist die empfohlene Methode für SQL Pass-Through-Abfragen in ODBC-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="ab3a4-133">Using a **QueryDef** object is the preferred way to perform SQL pass-through queries with ODBC databases.</span></span>

<span data-ttu-id="ab3a4-134">Verwenden Sie die \*\*\*\*Delete\*\*\*\* -Methode für die Auflistung, um ein [QueryDef](fields-delete-method-dao.md)-Objekt aus einer **QueryDefs**-Auflistung in einer Microsoft Access-Datenbank zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="ab3a4-134">To remove a **QueryDef** object from a **QueryDefs** collection in a Microsoft Access database engine database, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

