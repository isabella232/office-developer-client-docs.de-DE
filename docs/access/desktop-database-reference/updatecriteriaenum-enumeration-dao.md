---
title: UpdateCriteriaEnum Enumeration (DAO)
TOCTitle: UpdateCriteriaEnum Enumeration
ms:assetid: 1f83a0c6-bdc8-9c3e-380b-524f611f6476
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845853(v=office.15)
ms:contentKeyID: 48543644
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8035d90da62f83c930a208cac73f1fe45d61340
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880495"
---
# <a name="updatecriteriaenum-enumeration-dao"></a><span data-ttu-id="b7600-102">UpdateCriteriaEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="b7600-102">UpdateCriteriaEnum Enumeration (DAO)</span></span>


<span data-ttu-id="b7600-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7600-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b7600-104">Hiermit geben Sie zusammen mit der **UpdateOptions**-Methode an, wie eine Batchaktualisierung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b7600-104">Used with the **UpdateOptions** method to specify how a batch update is constructed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b7600-105">Name</span><span class="sxs-lookup"><span data-stu-id="b7600-105">Name</span></span></p></th>
<th><p><span data-ttu-id="b7600-106">Wert</span><span class="sxs-lookup"><span data-stu-id="b7600-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b7600-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7600-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7600-108">dbCriteriaAllCols</span><span class="sxs-lookup"><span data-stu-id="b7600-108">dbCriteriaAllCols</span></span></p></td>
<td><p><span data-ttu-id="b7600-109">4</span><span class="sxs-lookup"><span data-stu-id="b7600-109">4</span></span></p></td>
<td><p><span data-ttu-id="b7600-110">Verwendet die Schlüsselspalte(n) und alle Spalten in der WHERE-Klausel.</span><span class="sxs-lookup"><span data-stu-id="b7600-110">Uses the key column(s) and all the columns in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7600-111">dbCriteriaDeleteInsert</span><span class="sxs-lookup"><span data-stu-id="b7600-111">dbCriteriaDeleteInsert</span></span></p></td>
<td><p><span data-ttu-id="b7600-112">16</span><span class="sxs-lookup"><span data-stu-id="b7600-112">16</span></span></p></td>
<td><p><span data-ttu-id="b7600-113">Verwendet für jede geänderte Zeile ein DELETE/INSERT-Anweisungspaar.</span><span class="sxs-lookup"><span data-stu-id="b7600-113">Uses a pair of DELETE and INSERT statements for each modified row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7600-114">dbCriteriaKey</span><span class="sxs-lookup"><span data-stu-id="b7600-114">dbCriteriaKey</span></span></p></td>
<td><p><span data-ttu-id="b7600-115">1</span><span class="sxs-lookup"><span data-stu-id="b7600-115">1</span></span></p></td>
<td><p><span data-ttu-id="b7600-116">Verwendet nur die Schlüsselspalte(n) in der WHERE-Klausel.</span><span class="sxs-lookup"><span data-stu-id="b7600-116">Uses just the key column(s) in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7600-117">dbCriteriaModValues</span><span class="sxs-lookup"><span data-stu-id="b7600-117">dbCriteriaModValues</span></span></p></td>
<td><p><span data-ttu-id="b7600-118">2</span><span class="sxs-lookup"><span data-stu-id="b7600-118">2</span></span></p></td>
<td><p><span data-ttu-id="b7600-119">Verwendet die Schlüsselspalte(n) und alle aktualisierten Spalten in der WHERE-Klausel.</span><span class="sxs-lookup"><span data-stu-id="b7600-119">Uses the key column(s) and all updated columns in the where clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7600-120">dbCriteriaTimestamp</span><span class="sxs-lookup"><span data-stu-id="b7600-120">dbCriteriaTimestamp</span></span></p></td>
<td><p><span data-ttu-id="b7600-121">8</span><span class="sxs-lookup"><span data-stu-id="b7600-121">8</span></span></p></td>
<td><p><span data-ttu-id="b7600-122">Verwendet nur die Zeitstempelspalte, soweit vorhanden (ein Laufzeitfehler wird generiert, falls im Resultset keine Zeitstempelspalte vorhanden ist).</span><span class="sxs-lookup"><span data-stu-id="b7600-122">Uses just the timestamp column if available (will generate a run-time error if no timestamp column is in the result set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7600-123">dbCriteriaUpdate</span><span class="sxs-lookup"><span data-stu-id="b7600-123">dbCriteriaUpdate</span></span></p></td>
<td><p><span data-ttu-id="b7600-124">32</span><span class="sxs-lookup"><span data-stu-id="b7600-124">32</span></span></p></td>
<td><p><span data-ttu-id="b7600-125">Verwendet für jede geänderte Zeile eine UPDATE-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="b7600-125">Uses an UPDATE statement for each modified row.</span></span></p></td>
</tr>
</tbody>
</table>

