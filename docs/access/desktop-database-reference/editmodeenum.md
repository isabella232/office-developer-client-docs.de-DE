---
title: EditModeEnum (Access Desktop Database Reference)
TOCTitle: EditModeEnum
ms:assetid: 4da0e504-aca2-b769-04a2-0df687fa4422
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249248(v=office.15)
ms:contentKeyID: 48544737
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 246d9e29f084efb975783fd15c15993eba5a6e74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293581"
---
# <a name="editmodeenum"></a><span data-ttu-id="b0a93-102">EditModeEnum</span><span class="sxs-lookup"><span data-stu-id="b0a93-102">EditModeEnum</span></span>

<span data-ttu-id="b0a93-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0a93-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0a93-104">Gibt den Bearbeitungsstatus eines Datensatzes an.</span><span class="sxs-lookup"><span data-stu-id="b0a93-104">Specifies the editing status of a record.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0a93-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="b0a93-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="b0a93-106">Wert</span><span class="sxs-lookup"><span data-stu-id="b0a93-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b0a93-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0a93-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0a93-108"><strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="b0a93-108"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="b0a93-109">0</span><span class="sxs-lookup"><span data-stu-id="b0a93-109">0</span></span></p></td>
<td><p><span data-ttu-id="b0a93-110">Gibt an, dass kein Bearbeitungsvorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b0a93-110">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0a93-111"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="b0a93-111"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="b0a93-112">1</span><span class="sxs-lookup"><span data-stu-id="b0a93-112">1</span></span></p></td>
<td><p><span data-ttu-id="b0a93-113">Gibt an, dass Daten im aktuellen Datensatz geändert, aber nicht gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="b0a93-113">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0a93-114"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="b0a93-114"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="b0a93-115">2</span><span class="sxs-lookup"><span data-stu-id="b0a93-115">2</span></span></p></td>
<td><p><span data-ttu-id="b0a93-116">Gibt an, dass die <a href="addnew-method-ado.md">AddNew</a>-Methode aufgerufen wurde und der aktuelle Datensatz im Kopierpuffer ein neuer Datensatz ist, der in der Datenbank nicht gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="b0a93-116">Indicates that the <a href="addnew-method-ado.md">AddNew</a> method has been called, and the current record in the copy buffer is a new record that has not been saved in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0a93-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="b0a93-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="b0a93-118">4</span><span class="sxs-lookup"><span data-stu-id="b0a93-118">4</span></span></p></td>
<td><p><span data-ttu-id="b0a93-119">Gibt an, dass der aktuelle Datensatz gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="b0a93-119">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="b0a93-120">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="b0a93-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="b0a93-121">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="b0a93-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0a93-122">Konstante</span><span class="sxs-lookup"><span data-stu-id="b0a93-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0a93-123">AdoEnums. EditMode. NONE</span><span class="sxs-lookup"><span data-stu-id="b0a93-123">AdoEnums.EditMode.NONE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0a93-124">AdoEnums. EditMode. inPROGRESS</span><span class="sxs-lookup"><span data-stu-id="b0a93-124">AdoEnums.EditMode.INPROGRESS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0a93-125">AdoEnums. EditMode. ADD</span><span class="sxs-lookup"><span data-stu-id="b0a93-125">AdoEnums.EditMode.ADD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0a93-126">AdoEnums. EditMode. DELETE</span><span class="sxs-lookup"><span data-stu-id="b0a93-126">AdoEnums.EditMode.DELETE</span></span></p></td>
</tr>
</tbody>
</table>

