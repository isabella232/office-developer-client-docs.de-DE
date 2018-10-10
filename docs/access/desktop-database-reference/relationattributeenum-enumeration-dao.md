---
title: RelationAttributeEnum Enumeration (DAO)
TOCTitle: RelationAttributeEnum Enumeration
ms:assetid: ce8d0696-66d7-052f-1313-64baee3442ed
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834499(v=office.15)
ms:contentKeyID: 48547787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4c4d7a2b622e382461bcf1b4171a5aa85f036854
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475381"
---
# <a name="relationattributeenum-enumeration-dao"></a><span data-ttu-id="3a3c7-102">RelationAttributeEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="3a3c7-102">RelationAttributeEnum Enumeration (DAO)</span></span>


<span data-ttu-id="3a3c7-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a3c7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3a3c7-104">Hiermit bestimmen Sie zusammen mit der **Attributes**-Eigenschaft die Attribute eines **Relation**-Objekts.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-104">Used with the **Attributes** property to determine attributes of a **Relation** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3a3c7-105">Name</span><span class="sxs-lookup"><span data-stu-id="3a3c7-105">Name</span></span></p></th>
<th><p><span data-ttu-id="3a3c7-106">Wert</span><span class="sxs-lookup"><span data-stu-id="3a3c7-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3a3c7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a3c7-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a3c7-108">dbRelationDeleteCascade</span><span class="sxs-lookup"><span data-stu-id="3a3c7-108">dbRelationDeleteCascade</span></span></p></td>
<td><p><span data-ttu-id="3a3c7-109">4096</span><span class="sxs-lookup"><span data-stu-id="3a3c7-109">4096</span></span></p></td>
<td><p><span data-ttu-id="3a3c7-110">Löschungen werden weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-110">Deletions cascade</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a3c7-111">dbRelationDontEnforce</span><span class="sxs-lookup"><span data-stu-id="3a3c7-111">dbRelationDontEnforce</span></span></p></td>
<td><p><span data-ttu-id="3a3c7-112">2</span><span class="sxs-lookup"><span data-stu-id="3a3c7-112">2</span></span></p></td>
<td><p><span data-ttu-id="3a3c7-113">Die Beziehung wird nicht erzwungen (keine referentielle Integrität).</span><span class="sxs-lookup"><span data-stu-id="3a3c7-113">Relationship not enforced (no referential integrity)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a3c7-114">dbRelationInherited</span><span class="sxs-lookup"><span data-stu-id="3a3c7-114">dbRelationInherited</span></span></p></td>
<td><p><span data-ttu-id="3a3c7-115">4</span><span class="sxs-lookup"><span data-stu-id="3a3c7-115">4</span></span></p></td>
<td><p><span data-ttu-id="3a3c7-116">Die Beziehung ist in der Datenbank vorhanden, die die beiden verknüpften Tabellen enthält.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-116">Relationship exists in the database containing the two linked tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a3c7-117">dbRelationLeft</span><span class="sxs-lookup"><span data-stu-id="3a3c7-117">dbRelationLeft</span></span></p></td>
<td><p><span data-ttu-id="3a3c7-118">16777216</span><span class="sxs-lookup"><span data-stu-id="3a3c7-118">16777216</span></span></p></td>
<td><p><span data-ttu-id="3a3c7-p101">Nur Microsoft Access. In der Entwurfsansicht wird eine LEFT JOIN-Operation als Standardverknüpfungstyp angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-p101">Microsoft Access only. In Design view, display a LEFT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a3c7-121">dbRelationRight</span><span class="sxs-lookup"><span data-stu-id="3a3c7-121">dbRelationRight</span></span></p></td>
<td><p><span data-ttu-id="3a3c7-122">33554432</span><span class="sxs-lookup"><span data-stu-id="3a3c7-122">33554432</span></span></p></td>
<td><p><span data-ttu-id="3a3c7-p102">Nur Microsoft Access. In der Entwurfsansicht wird eine RIGHT JOIN-Operation als Standardverknüpfungstyp angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-p102">Microsoft Access only. In Design view, display a RIGHT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a3c7-125">dbRelationUnique</span><span class="sxs-lookup"><span data-stu-id="3a3c7-125">dbRelationUnique</span></span></p></td>
<td><p><span data-ttu-id="3a3c7-126">1</span><span class="sxs-lookup"><span data-stu-id="3a3c7-126">1</span></span></p></td>
<td><p><span data-ttu-id="3a3c7-127">1:1-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-127">One-to-one relationship</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a3c7-128">dbRelationUpdateCascade</span><span class="sxs-lookup"><span data-stu-id="3a3c7-128">dbRelationUpdateCascade</span></span></p></td>
<td><p><span data-ttu-id="3a3c7-129">256</span><span class="sxs-lookup"><span data-stu-id="3a3c7-129">256</span></span></p></td>
<td><p><span data-ttu-id="3a3c7-130">Aktualisierungen werden weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-130">Updates cascade</span></span></p></td>
</tr>
</tbody>
</table>

