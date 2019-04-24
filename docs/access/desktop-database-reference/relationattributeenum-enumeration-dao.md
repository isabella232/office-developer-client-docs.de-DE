---
title: RelationAttributeEnum-Aufzählung (DAO)
TOCTitle: RelationAttributeEnum Enumeration
ms:assetid: ce8d0696-66d7-052f-1313-64baee3442ed
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834499(v=office.15)
ms:contentKeyID: 48547787
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbb8ca2e1a63154f17bd814a26fe79ed405765cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306979"
---
# <a name="relationattributeenum-enumeration-dao"></a><span data-ttu-id="a6b8d-102">RelationAttributeEnum-Aufzählung (DAO)</span><span class="sxs-lookup"><span data-stu-id="a6b8d-102">RelationAttributeEnum enumeration (DAO)</span></span>


<span data-ttu-id="a6b8d-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a6b8d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a6b8d-104">Hiermit bestimmen Sie zusammen mit der **Attributes**-Eigenschaft die Attribute eines **Relation**-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a6b8d-104">Used with the **Attributes** property to determine attributes of a **Relation** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a6b8d-105">Name</span><span class="sxs-lookup"><span data-stu-id="a6b8d-105">Name</span></span></p></th>
<th><p><span data-ttu-id="a6b8d-106">Wert</span><span class="sxs-lookup"><span data-stu-id="a6b8d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a6b8d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6b8d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6b8d-108">dbRelationDeleteCascade</span><span class="sxs-lookup"><span data-stu-id="a6b8d-108">dbRelationDeleteCascade</span></span></p></td>
<td><p><span data-ttu-id="a6b8d-109">4096</span><span class="sxs-lookup"><span data-stu-id="a6b8d-109">4096</span></span></p></td>
<td><p><span data-ttu-id="a6b8d-110">Löschungen werden weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="a6b8d-110">Deletions cascade</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6b8d-111">dbRelationDontEnforce</span><span class="sxs-lookup"><span data-stu-id="a6b8d-111">dbRelationDontEnforce</span></span></p></td>
<td><p><span data-ttu-id="a6b8d-112">2</span><span class="sxs-lookup"><span data-stu-id="a6b8d-112">2</span></span></p></td>
<td><p><span data-ttu-id="a6b8d-113">Die Beziehung wird nicht erzwungen (keine referentielle Integrität).</span><span class="sxs-lookup"><span data-stu-id="a6b8d-113">Relationship not enforced (no referential integrity)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6b8d-114">dbRelationInherited</span><span class="sxs-lookup"><span data-stu-id="a6b8d-114">dbRelationInherited</span></span></p></td>
<td><p><span data-ttu-id="a6b8d-115">4</span><span class="sxs-lookup"><span data-stu-id="a6b8d-115">4</span></span></p></td>
<td><p><span data-ttu-id="a6b8d-116">Die Beziehung ist in der Datenbank vorhanden, die die beiden verknüpften Tabellen enthält.</span><span class="sxs-lookup"><span data-stu-id="a6b8d-116">Relationship exists in the database containing the two linked tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6b8d-117">dbRelationLeft</span><span class="sxs-lookup"><span data-stu-id="a6b8d-117">dbRelationLeft</span></span></p></td>
<td><p><span data-ttu-id="a6b8d-118">16777216</span><span class="sxs-lookup"><span data-stu-id="a6b8d-118">16777216</span></span></p></td>
<td><p><span data-ttu-id="a6b8d-p101">Nur Microsoft Access. In der Entwurfsansicht wird eine LEFT JOIN-Operation als Standardverknüpfungstyp angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6b8d-p101">Microsoft Access only. In Design view, display a LEFT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6b8d-121">dbRelationRight</span><span class="sxs-lookup"><span data-stu-id="a6b8d-121">dbRelationRight</span></span></p></td>
<td><p><span data-ttu-id="a6b8d-122">33554432</span><span class="sxs-lookup"><span data-stu-id="a6b8d-122">33554432</span></span></p></td>
<td><p><span data-ttu-id="a6b8d-p102">Nur Microsoft Access. In der Entwurfsansicht wird eine RIGHT JOIN-Operation als Standardverknüpfungstyp angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6b8d-p102">Microsoft Access only. In Design view, display a RIGHT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6b8d-125">dbRelationUnique</span><span class="sxs-lookup"><span data-stu-id="a6b8d-125">dbRelationUnique</span></span></p></td>
<td><p><span data-ttu-id="a6b8d-126">1</span><span class="sxs-lookup"><span data-stu-id="a6b8d-126">1</span></span></p></td>
<td><p><span data-ttu-id="a6b8d-127">1:1-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="a6b8d-127">One-to-one relationship</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6b8d-128">dbRelationUpdateCascade</span><span class="sxs-lookup"><span data-stu-id="a6b8d-128">dbRelationUpdateCascade</span></span></p></td>
<td><p><span data-ttu-id="a6b8d-129">256</span><span class="sxs-lookup"><span data-stu-id="a6b8d-129">256</span></span></p></td>
<td><p><span data-ttu-id="a6b8d-130">Aktualisierungen werden weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="a6b8d-130">Updates cascade</span></span></p></td>
</tr>
</tbody>
</table>

