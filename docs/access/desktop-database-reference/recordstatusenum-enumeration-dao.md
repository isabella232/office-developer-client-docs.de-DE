---
title: RecordStatusEnum (Aufzählung) (DAO)
TOCTitle: RecordStatusEnum Enumeration
ms:assetid: bf4492f2-8d8f-f10f-7a3c-d6296d2ce96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822784(v=office.15)
ms:contentKeyID: 48547483
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 662176616b267e2fe60b225a3d3def7418e7bcaf
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944354"
---
# <a name="recordstatusenum-enumeration-dao"></a><span data-ttu-id="2ef10-102">RecordStatusEnum (Aufzählung) (DAO)</span><span class="sxs-lookup"><span data-stu-id="2ef10-102">RecordStatusEnum enumeration (DAO)</span></span>


<span data-ttu-id="2ef10-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2ef10-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2ef10-104">Hiermit geben Sie zusammen mit der **RecordStatus**-Eigenschaft den Aktualisierungsstatus des aktuellen Datensatzes an, wenn dieser Teil einer Batchaktualisierung ist.</span><span class="sxs-lookup"><span data-stu-id="2ef10-104">Used with the **RecordStatus** property to indicate the update status of the current record if it is part of a batch update.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2ef10-105">Name</span><span class="sxs-lookup"><span data-stu-id="2ef10-105">Name</span></span></p></th>
<th><p><span data-ttu-id="2ef10-106">Wert</span><span class="sxs-lookup"><span data-stu-id="2ef10-106">Value</span></span></p></th>
<th><p><span data-ttu-id="2ef10-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ef10-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ef10-108">dbRecordDBDeleted</span><span class="sxs-lookup"><span data-stu-id="2ef10-108">dbRecordDBDeleted</span></span></p></td>
<td><p><span data-ttu-id="2ef10-109">4</span><span class="sxs-lookup"><span data-stu-id="2ef10-109">4</span></span></p></td>
<td><p><span data-ttu-id="2ef10-110">Der Datensatz wurde lokal und in der Datenbank gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2ef10-110">The record has been deleted locally and in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ef10-111">dbRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="2ef10-111">dbRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="2ef10-112">3</span><span class="sxs-lookup"><span data-stu-id="2ef10-112">3</span></span></p></td>
<td><p><span data-ttu-id="2ef10-113">Der Datensatz wurde gelöscht, er wurde jedoch noch nicht in der Datenbank gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2ef10-113">The record has been deleted, but not yet deleted in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ef10-114">dbRecordModified</span><span class="sxs-lookup"><span data-stu-id="2ef10-114">dbRecordModified</span></span></p></td>
<td><p><span data-ttu-id="2ef10-115">1</span><span class="sxs-lookup"><span data-stu-id="2ef10-115">1</span></span></p></td>
<td><p><span data-ttu-id="2ef10-116">Der Datensatz wurde geändert und nicht in der Datenbank aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2ef10-116">The record has been modified and not updated in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ef10-117">dbRecordNew</span><span class="sxs-lookup"><span data-stu-id="2ef10-117">dbRecordNew</span></span></p></td>
<td><p><span data-ttu-id="2ef10-118">2</span><span class="sxs-lookup"><span data-stu-id="2ef10-118">2</span></span></p></td>
<td><p><span data-ttu-id="2ef10-119">Der Datensatz wurde mit der <strong>AddNew</strong>-Methode eingefügt, aber noch nicht in die Datenbank eingefügt.</span><span class="sxs-lookup"><span data-stu-id="2ef10-119">The record has been inserted with the <strong>AddNew</strong> method, but not yet inserted into the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ef10-120">Wert dbRecordUnmodified</span><span class="sxs-lookup"><span data-stu-id="2ef10-120">dbRecordUnmodified</span></span></p></td>
<td><p><span data-ttu-id="2ef10-121">0</span><span class="sxs-lookup"><span data-stu-id="2ef10-121">0</span></span></p></td>
<td><p><span data-ttu-id="2ef10-122">(Standard) Der Datensatz wurde nicht geändert, oder er wurde erfolgreich aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2ef10-122">(Default) The record has not been modified or has been updated successfully.</span></span></p></td>
</tr>
</tbody>
</table>

