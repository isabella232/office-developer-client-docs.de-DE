---
title: Bestimmen des Bearbeitungsmodus
TOCTitle: Determining Edit mode
ms:assetid: 45e21fa7-94e8-3449-e062-09cbcf15cba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249215(v=office.15)
ms:contentKeyID: 48544563
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5b62bc282a99472d0e7399ee9f3dd9d0648f0c7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698750"
---
# <a name="determining-edit-mode"></a><span data-ttu-id="add1c-102">Bestimmen des Bearbeitungsmodus</span><span class="sxs-lookup"><span data-stu-id="add1c-102">Determining Edit mode</span></span>


<span data-ttu-id="add1c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="add1c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="add1c-p101">ADO verwaltet einen Bearbeitungspuffer, der dem aktuellen Datensatz zugeordnet ist. Die **EditMode** -Eigenschaft gibt an, ob Änderungen an diesem Puffer vorgenommen wurden, oder ob ein neuer Datensatz erstellt wurde. Verwenden Sie **EditMode**, um den Bearbeitungsstatus des aktuellen Datensatzes zu bestimmen. Sie können testen, ob ausstehende Änderungen vorhanden sind, falls ein Bearbeitungsprozess unterbrochen wurde, und ermitteln, ob Sie die **Update** - oder **CancelUpdate** -Methode verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="add1c-p101">ADO maintains an editing buffer associated with the current record. The **EditMode** property indicates whether changes have been made to this buffer or whether a new record has been created. Use **EditMode** to determine the editing status of the current record. You can test for pending changes if an editing process has been interrupted and determine whether you need to use the **Update** or **CancelUpdate** method.</span></span>

<span data-ttu-id="add1c-108">**EditMode** gibt eine der **EditModeEnum** -Konstanten zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="add1c-108">**EditMode** returns one of the **EditModeEnum** constants, which are listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="add1c-109">Konstante</span><span class="sxs-lookup"><span data-stu-id="add1c-109">Constant</span></span></p></th>
<th><p><span data-ttu-id="add1c-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="add1c-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="add1c-111"><strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="add1c-111"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="add1c-112">Gibt an, dass kein Bearbeitungsvorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="add1c-112">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="add1c-113"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="add1c-113"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="add1c-114">Gibt an, dass Daten im aktuellen Datensatz geändert, aber nicht gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="add1c-114">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="add1c-115"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="add1c-115"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="add1c-116">Gibt an, dass die <strong>AddNew</strong>-Methode aufgerufen wurde, und dass der aktuelle Datensatz im Kopierpuffer ein neuer Datensatz ist, der nicht in der Datenbank gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="add1c-116">Indicates that the <strong>AddNew</strong> method has been called, and the current record in the copy buffer is a new record that has not been saved to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="add1c-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="add1c-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="add1c-118">Gibt an, dass der aktuelle Datensatz gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="add1c-118">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="add1c-p102">**EditMode** kann nur einen gültigen Wert zurückgeben, wenn ein aktueller Datensatz vorhanden ist. **EditMode** gibt einen Fehler zurück, falls **BOF** oder **EOF** gleich **True** ist, oder falls der aktuelle Datensatz gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="add1c-p102">**EditMode** can return a valid value only if there is a current record. **EditMode** will return an error if **BOF** or **EOF** is **True** or if the current record has been deleted.</span></span>

