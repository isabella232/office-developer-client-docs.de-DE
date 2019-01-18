---
title: ObjectTypeEnum (Access PC-Datenbank-Referenz)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6e3b470c8c0d0c3f04b59bd382b66117bd79c188
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711833"
---
# <a name="objecttypeenum"></a><span data-ttu-id="00c1b-102">ObjectTypeEnum</span><span class="sxs-lookup"><span data-stu-id="00c1b-102">ObjectTypeEnum</span></span>

<span data-ttu-id="00c1b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="00c1b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="00c1b-104">Gibt den Typ des Datenbankobjekts an, für das Berechtigungen oder Besitzrechte festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="00c1b-104">Specifies the type of database object for which to set permissions or ownership.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="00c1b-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="00c1b-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="00c1b-106">Wert</span><span class="sxs-lookup"><span data-stu-id="00c1b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="00c1b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00c1b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00c1b-108"><strong>adPermObjColumn</strong></span><span class="sxs-lookup"><span data-stu-id="00c1b-108"><strong>adPermObjColumn</strong></span></span></p></td>
<td><p><span data-ttu-id="00c1b-109">2</span><span class="sxs-lookup"><span data-stu-id="00c1b-109">2</span></span></p></td>
<td><p><span data-ttu-id="00c1b-110">Bei dem Objekt handelt es sich um eine Spalte.</span><span class="sxs-lookup"><span data-stu-id="00c1b-110">The object is a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00c1b-111"><strong>adPermObjDatabase</strong></span><span class="sxs-lookup"><span data-stu-id="00c1b-111"><strong>adPermObjDatabase</strong></span></span></p></td>
<td><p><span data-ttu-id="00c1b-112">3</span><span class="sxs-lookup"><span data-stu-id="00c1b-112">3</span></span></p></td>
<td><p><span data-ttu-id="00c1b-113">Bei dem Objekt handelt es sich um eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="00c1b-113">The object is a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00c1b-114"><strong>adPermObjProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="00c1b-114"><strong>adPermObjProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="00c1b-115">4</span><span class="sxs-lookup"><span data-stu-id="00c1b-115">4</span></span></p></td>
<td><p><span data-ttu-id="00c1b-116">Bei dem Objekt handelt es sich um eine Prozedur.</span><span class="sxs-lookup"><span data-stu-id="00c1b-116">The object is a procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00c1b-117"><strong>adPermObjProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="00c1b-117"><strong>adPermObjProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="00c1b-118">-1</span><span class="sxs-lookup"><span data-stu-id="00c1b-118">-1</span></span></p></td>
<td><p><span data-ttu-id="00c1b-p101">Bei dem Objekt handelt es sich um einen vom Anbieter definierten Typ. Es tritt ein Fehler auf, wenn der <em>ObjectType</em>-Parameter gleich <strong>adPermObjProviderSpecific</strong> ist und <em>ObjectTypeId</em> nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="00c1b-p101">The object is a type defined by the provider. An error will occur if the <em>ObjectType</em> parameter is <strong>adPermObjProviderSpecific</strong> and an <em>ObjectTypeId</em> is not supplied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00c1b-121"><strong>adPermObjTable</strong></span><span class="sxs-lookup"><span data-stu-id="00c1b-121"><strong>adPermObjTable</strong></span></span></p></td>
<td><p><span data-ttu-id="00c1b-122">1</span><span class="sxs-lookup"><span data-stu-id="00c1b-122">1</span></span></p></td>
<td><p><span data-ttu-id="00c1b-123">Bei dem Objekt handelt es sich um eine Tabelle.</span><span class="sxs-lookup"><span data-stu-id="00c1b-123">The object is a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00c1b-124"><strong>adPermObjView</strong></span><span class="sxs-lookup"><span data-stu-id="00c1b-124"><strong>adPermObjView</strong></span></span></p></td>
<td><p><span data-ttu-id="00c1b-125">5</span><span class="sxs-lookup"><span data-stu-id="00c1b-125">5</span></span></p></td>
<td><p><span data-ttu-id="00c1b-126">Bei dem Objekt handelt es sich um eine Sicht.</span><span class="sxs-lookup"><span data-stu-id="00c1b-126">The object is a view.</span></span></p></td>
</tr>
</tbody>
</table>

