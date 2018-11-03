---
title: UpdateCriteriaEnum (Aufzählung) (DAO)
TOCTitle: UpdateCriteriaEnum Enumeration
ms:assetid: 1f83a0c6-bdc8-9c3e-380b-524f611f6476
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845853(v=office.15)
ms:contentKeyID: 48543644
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d6160c53dd1cab26b2b92ec023f28158635d7081
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944466"
---
# <a name="updatecriteriaenum-enumeration-dao"></a><span data-ttu-id="b130d-102">UpdateCriteriaEnum (Aufzählung) (DAO)</span><span class="sxs-lookup"><span data-stu-id="b130d-102">UpdateCriteriaEnum enumeration (DAO)</span></span>


<span data-ttu-id="b130d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b130d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b130d-104">Hiermit geben Sie zusammen mit der **UpdateOptions**-Methode an, wie eine Batchaktualisierung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b130d-104">Used with the **UpdateOptions** method to specify how a batch update is constructed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b130d-105">Name</span><span class="sxs-lookup"><span data-stu-id="b130d-105">Name</span></span></p></th>
<th><p><span data-ttu-id="b130d-106">Wert</span><span class="sxs-lookup"><span data-stu-id="b130d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b130d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b130d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b130d-108">dbCriteriaAllCols</span><span class="sxs-lookup"><span data-stu-id="b130d-108">dbCriteriaAllCols</span></span></p></td>
<td><p><span data-ttu-id="b130d-109">4</span><span class="sxs-lookup"><span data-stu-id="b130d-109">4</span></span></p></td>
<td><p><span data-ttu-id="b130d-110">Verwendet die Schlüsselspalte(n) und alle Spalten in der WHERE-Klausel.</span><span class="sxs-lookup"><span data-stu-id="b130d-110">Uses the key column(s) and all the columns in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b130d-111">dbCriteriaDeleteInsert</span><span class="sxs-lookup"><span data-stu-id="b130d-111">dbCriteriaDeleteInsert</span></span></p></td>
<td><p><span data-ttu-id="b130d-112">16</span><span class="sxs-lookup"><span data-stu-id="b130d-112">16</span></span></p></td>
<td><p><span data-ttu-id="b130d-113">Verwendet für jede geänderte Zeile ein DELETE/INSERT-Anweisungspaar.</span><span class="sxs-lookup"><span data-stu-id="b130d-113">Uses a pair of DELETE and INSERT statements for each modified row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b130d-114">dbCriteriaKey</span><span class="sxs-lookup"><span data-stu-id="b130d-114">dbCriteriaKey</span></span></p></td>
<td><p><span data-ttu-id="b130d-115">1</span><span class="sxs-lookup"><span data-stu-id="b130d-115">1</span></span></p></td>
<td><p><span data-ttu-id="b130d-116">Verwendet nur die Schlüsselspalte(n) in der WHERE-Klausel.</span><span class="sxs-lookup"><span data-stu-id="b130d-116">Uses just the key column(s) in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b130d-117">dbCriteriaModValues</span><span class="sxs-lookup"><span data-stu-id="b130d-117">dbCriteriaModValues</span></span></p></td>
<td><p><span data-ttu-id="b130d-118">2</span><span class="sxs-lookup"><span data-stu-id="b130d-118">2</span></span></p></td>
<td><p><span data-ttu-id="b130d-119">Verwendet die Schlüsselspalte(n) und alle aktualisierten Spalten in der WHERE-Klausel.</span><span class="sxs-lookup"><span data-stu-id="b130d-119">Uses the key column(s) and all updated columns in the where clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b130d-120">dbCriteriaTimestamp</span><span class="sxs-lookup"><span data-stu-id="b130d-120">dbCriteriaTimestamp</span></span></p></td>
<td><p><span data-ttu-id="b130d-121">8</span><span class="sxs-lookup"><span data-stu-id="b130d-121">8</span></span></p></td>
<td><p><span data-ttu-id="b130d-122">Verwendet nur die Zeitstempelspalte, soweit vorhanden (ein Laufzeitfehler wird generiert, falls im Resultset keine Zeitstempelspalte vorhanden ist).</span><span class="sxs-lookup"><span data-stu-id="b130d-122">Uses just the timestamp column if available (will generate a run-time error if no timestamp column is in the result set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b130d-123">dbCriteriaUpdate</span><span class="sxs-lookup"><span data-stu-id="b130d-123">dbCriteriaUpdate</span></span></p></td>
<td><p><span data-ttu-id="b130d-124">32</span><span class="sxs-lookup"><span data-stu-id="b130d-124">32</span></span></p></td>
<td><p><span data-ttu-id="b130d-125">Verwendet für jede geänderte Zeile eine UPDATE-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="b130d-125">Uses an UPDATE statement for each modified row.</span></span></p></td>
</tr>
</tbody>
</table>

