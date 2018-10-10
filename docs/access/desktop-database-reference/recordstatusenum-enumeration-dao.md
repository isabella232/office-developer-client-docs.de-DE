---
title: RecordStatusEnum Enumeration (DAO)
TOCTitle: RecordStatusEnum Enumeration
ms:assetid: bf4492f2-8d8f-f10f-7a3c-d6296d2ce96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822784(v=office.15)
ms:contentKeyID: 48547483
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 78f86e8c80a6bbc09499e9512e2daee87fc67998
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473680"
---
# <a name="recordstatusenum-enumeration-dao"></a><span data-ttu-id="9f5b1-102">RecordStatusEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="9f5b1-102">RecordStatusEnum Enumeration (DAO)</span></span>


<span data-ttu-id="9f5b1-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f5b1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9f5b1-104">Hiermit geben Sie zusammen mit der **RecordStatus**-Eigenschaft den Aktualisierungsstatus des aktuellen Datensatzes an, wenn dieser Teil einer Batchaktualisierung ist.</span><span class="sxs-lookup"><span data-stu-id="9f5b1-104">Used with the **RecordStatus** property to indicate the update status of the current record if it is part of a batch update.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9f5b1-105">Name</span><span class="sxs-lookup"><span data-stu-id="9f5b1-105">Name</span></span></p></th>
<th><p><span data-ttu-id="9f5b1-106">Wert</span><span class="sxs-lookup"><span data-stu-id="9f5b1-106">Value</span></span></p></th>
<th><p><span data-ttu-id="9f5b1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f5b1-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f5b1-108">dbRecordDBDeleted</span><span class="sxs-lookup"><span data-stu-id="9f5b1-108">dbRecordDBDeleted</span></span></p></td>
<td><p><span data-ttu-id="9f5b1-109">4</span><span class="sxs-lookup"><span data-stu-id="9f5b1-109">4</span></span></p></td>
<td><p><span data-ttu-id="9f5b1-110">Der Datensatz wurde lokal und in der Datenbank gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9f5b1-110">The record has been deleted locally and in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f5b1-111">dbRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="9f5b1-111">dbRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="9f5b1-112">3</span><span class="sxs-lookup"><span data-stu-id="9f5b1-112">3</span></span></p></td>
<td><p><span data-ttu-id="9f5b1-113">Der Datensatz wurde gelöscht, er wurde jedoch noch nicht in der Datenbank gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9f5b1-113">The record has been deleted, but not yet deleted in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f5b1-114">dbRecordModified</span><span class="sxs-lookup"><span data-stu-id="9f5b1-114">dbRecordModified</span></span></p></td>
<td><p><span data-ttu-id="9f5b1-115">1</span><span class="sxs-lookup"><span data-stu-id="9f5b1-115">1</span></span></p></td>
<td><p><span data-ttu-id="9f5b1-116">Der Datensatz wurde geändert und nicht in der Datenbank aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9f5b1-116">The record has been modified and not updated in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f5b1-117">dbRecordNew</span><span class="sxs-lookup"><span data-stu-id="9f5b1-117">dbRecordNew</span></span></p></td>
<td><p><span data-ttu-id="9f5b1-118">2</span><span class="sxs-lookup"><span data-stu-id="9f5b1-118">2</span></span></p></td>
<td><p><span data-ttu-id="9f5b1-119">Der Datensatz wurde mit der <strong>AddNew</strong>-Methode eingefügt, aber noch nicht in die Datenbank eingefügt.</span><span class="sxs-lookup"><span data-stu-id="9f5b1-119">The record has been inserted with the <strong>AddNew</strong> method, but not yet inserted into the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f5b1-120">Wert dbRecordUnmodified</span><span class="sxs-lookup"><span data-stu-id="9f5b1-120">dbRecordUnmodified</span></span></p></td>
<td><p><span data-ttu-id="9f5b1-121">0</span><span class="sxs-lookup"><span data-stu-id="9f5b1-121">0</span></span></p></td>
<td><p><span data-ttu-id="9f5b1-122">(Standard) Der Datensatz wurde nicht geändert, oder er wurde erfolgreich aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9f5b1-122">(Default) The record has not been modified or has been updated successfully.</span></span></p></td>
</tr>
</tbody>
</table>

