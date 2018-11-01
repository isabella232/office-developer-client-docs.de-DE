---
title: ObjectTypeEnum (Access PC-Datenbank-Referenz)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 45a812e5d67a9324d5b07c5666e9cfe2940df580
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871290"
---
# <a name="objecttypeenum"></a><span data-ttu-id="77f5a-102">ObjectTypeEnum</span><span class="sxs-lookup"><span data-stu-id="77f5a-102">ObjectTypeEnum</span></span>

<span data-ttu-id="77f5a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="77f5a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="77f5a-104">Gibt den Typ des Datenbankobjekts an, für das Berechtigungen oder Besitzrechte festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="77f5a-104">Specifies the type of database object for which to set permissions or ownership.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77f5a-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="77f5a-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="77f5a-106">Wert</span><span class="sxs-lookup"><span data-stu-id="77f5a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="77f5a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77f5a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77f5a-108"><strong>adPermObjColumn</strong></span><span class="sxs-lookup"><span data-stu-id="77f5a-108"><strong>adPermObjColumn</strong></span></span></p></td>
<td><p><span data-ttu-id="77f5a-109">2</span><span class="sxs-lookup"><span data-stu-id="77f5a-109">2</span></span></p></td>
<td><p><span data-ttu-id="77f5a-110">Bei dem Objekt handelt es sich um eine Spalte.</span><span class="sxs-lookup"><span data-stu-id="77f5a-110">The object is a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77f5a-111"><strong>adPermObjDatabase</strong></span><span class="sxs-lookup"><span data-stu-id="77f5a-111"><strong>adPermObjDatabase</strong></span></span></p></td>
<td><p><span data-ttu-id="77f5a-112">3</span><span class="sxs-lookup"><span data-stu-id="77f5a-112">3</span></span></p></td>
<td><p><span data-ttu-id="77f5a-113">Bei dem Objekt handelt es sich um eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="77f5a-113">The object is a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77f5a-114"><strong>adPermObjProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="77f5a-114"><strong>adPermObjProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="77f5a-115">4</span><span class="sxs-lookup"><span data-stu-id="77f5a-115">4</span></span></p></td>
<td><p><span data-ttu-id="77f5a-116">Bei dem Objekt handelt es sich um eine Prozedur.</span><span class="sxs-lookup"><span data-stu-id="77f5a-116">The object is a procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77f5a-117"><strong>adPermObjProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="77f5a-117"><strong>adPermObjProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="77f5a-118">-1</span><span class="sxs-lookup"><span data-stu-id="77f5a-118">-1</span></span></p></td>
<td><p><span data-ttu-id="77f5a-p101">Bei dem Objekt handelt es sich um einen vom Anbieter definierten Typ. Es tritt ein Fehler auf, wenn der <em>ObjectType</em>-Parameter gleich <strong>adPermObjProviderSpecific</strong> ist und <em>ObjectTypeId</em> nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="77f5a-p101">The object is a type defined by the provider. An error will occur if the <em>ObjectType</em> parameter is <strong>adPermObjProviderSpecific</strong> and an <em>ObjectTypeId</em> is not supplied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77f5a-121"><strong>adPermObjTable</strong></span><span class="sxs-lookup"><span data-stu-id="77f5a-121"><strong>adPermObjTable</strong></span></span></p></td>
<td><p><span data-ttu-id="77f5a-122">1</span><span class="sxs-lookup"><span data-stu-id="77f5a-122">1</span></span></p></td>
<td><p><span data-ttu-id="77f5a-123">Bei dem Objekt handelt es sich um eine Tabelle.</span><span class="sxs-lookup"><span data-stu-id="77f5a-123">The object is a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77f5a-124"><strong>adPermObjView</strong></span><span class="sxs-lookup"><span data-stu-id="77f5a-124"><strong>adPermObjView</strong></span></span></p></td>
<td><p><span data-ttu-id="77f5a-125">5</span><span class="sxs-lookup"><span data-stu-id="77f5a-125">5</span></span></p></td>
<td><p><span data-ttu-id="77f5a-126">Bei dem Objekt handelt es sich um eine Sicht.</span><span class="sxs-lookup"><span data-stu-id="77f5a-126">The object is a view.</span></span></p></td>
</tr>
</tbody>
</table>

