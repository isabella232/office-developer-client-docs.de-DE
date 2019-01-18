---
title: ConnectModeEnum (Access PC-Datenbank-Referenz)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 453d84e687a31f7df5082e17b80fe2a1bda756be
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708662"
---
# <a name="connectmodeenum"></a><span data-ttu-id="49784-102">ConnectModeEnum</span><span class="sxs-lookup"><span data-stu-id="49784-102">ConnectModeEnum</span></span>

<span data-ttu-id="49784-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="49784-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49784-104">Gibt die verfügbaren Berechtigungen zum Ändern von Daten in einer [Verbindung](connection-object-ado.md) an, wobei ein [Datensatz](record-object-ado.md) geöffnet wird oder Werte für die [Mode](mode-property-ado.md)-Eigenschaft der **Record** - und [Stream](stream-object-ado.md)-Objekte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="49784-104">Specifies the available permissions for modifying data in a [Connection](connection-object-ado.md), opening a [Record](record-object-ado.md), or specifying values for the [Mode](mode-property-ado.md) property of the **Record** and [Stream](stream-object-ado.md) objects.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49784-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="49784-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="49784-106">Wert</span><span class="sxs-lookup"><span data-stu-id="49784-106">Value</span></span></p></th>
<th><p><span data-ttu-id="49784-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49784-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49784-108"><strong>adModeRead</strong></span><span class="sxs-lookup"><span data-stu-id="49784-108"><strong>adModeRead</strong></span></span></p></td>
<td><p><span data-ttu-id="49784-109">1</span><span class="sxs-lookup"><span data-stu-id="49784-109">1</span></span></p></td>
<td><p><span data-ttu-id="49784-110">Gibt nur schreibgeschützte Berechtigungen an.</span><span class="sxs-lookup"><span data-stu-id="49784-110">Indicates read-only permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49784-111"><strong>adModeReadWrite</strong></span><span class="sxs-lookup"><span data-stu-id="49784-111"><strong>adModeReadWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="49784-112">3</span><span class="sxs-lookup"><span data-stu-id="49784-112">3</span></span></p></td>
<td><p><span data-ttu-id="49784-113">Gibt Lese-/Schreibberechtigungen an.</span><span class="sxs-lookup"><span data-stu-id="49784-113">Indicates read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49784-114"><strong>adModeRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="49784-114"><strong>adModeRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="49784-115">0 x 400000</span><span class="sxs-lookup"><span data-stu-id="49784-115">0x400000</span></span></p></td>
<td><p><span data-ttu-id="49784-116">In Verbindung mit anderen <em>*ShareDeny*</em> Werte (<strong>AdModeShareDenyNone</strong>, <strong>AdModeShareDenyWrite</strong>oder <strong>AdModeShareDenyRead</strong>) weitergegeben sharing Einschränkungen auf alle untergeordneten Datensätze des aktuellen <strong>Datensatzes</strong>verwendet.</span><span class="sxs-lookup"><span data-stu-id="49784-116">Used in conjunction with the other <em>*ShareDeny*</em> values (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>, or <strong>adModeShareDenyRead</strong>) to propagate sharing restrictions to all sub-records of the current <strong>Record</strong>.</span></span> <span data-ttu-id="49784-117">Es hat keine Auswirkung, wenn der <strong>Datensatz</strong> keine untergeordneten Elemente verfügt.</span><span class="sxs-lookup"><span data-stu-id="49784-117">It has no affect if the <strong>Record</strong> does not have any children.</span></span></p><p><span data-ttu-id="49784-118">Ein Laufzeitfehler wird generiert, wenn sie nur <strong>AdModeShareDenyNone</strong> verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="49784-118">A run-time error is generated if it is used with <strong>adModeShareDenyNone</strong> only.</span></span> <span data-ttu-id="49784-119">Sie können jedoch mit <strong>AdModeShareDenyNone</strong> in Kombination mit anderen Werte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49784-119">However, it can be used with <strong>adModeShareDenyNone</strong> when combined with other values.</span></span> <span data-ttu-id="49784-120">Sie können beispielsweise verwenden &quot; <strong>AdModeRead</strong> oder <strong>AdModeShareDenyNone</strong> oder <strong>AdModeRecursive</strong>&quot;.</span><span class="sxs-lookup"><span data-stu-id="49784-120">For example, you can use &quot;<strong>adModeRead</strong> or <strong>adModeShareDenyNone</strong> or <strong>adModeRecursive</strong>&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49784-121"><strong>adModeShareDenyNone</strong></span><span class="sxs-lookup"><span data-stu-id="49784-121"><strong>adModeShareDenyNone</strong></span></span></p></td>
<td><p><span data-ttu-id="49784-122">16</span><span class="sxs-lookup"><span data-stu-id="49784-122">16</span></span></p></td>
<td><p><span data-ttu-id="49784-p103">Ermöglicht anderen Personen, eine Verbindung mit allen Berechtigungen zu öffnen. Weder der Lese- noch der Schreibzugriff kann anderen Personen verweigert werden.</span><span class="sxs-lookup"><span data-stu-id="49784-p103">Allows others to open a connection with any permissions. Neither read nor write access can be denied to others.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49784-125"><strong>adModeShareDenyRead</strong></span><span class="sxs-lookup"><span data-stu-id="49784-125"><strong>adModeShareDenyRead</strong></span></span></p></td>
<td><p><span data-ttu-id="49784-126">4</span><span class="sxs-lookup"><span data-stu-id="49784-126">4</span></span></p></td>
<td><p><span data-ttu-id="49784-127">Verhindert, dass andere Personen eine Verbindung mit Leseberechtigungen öffnen.</span><span class="sxs-lookup"><span data-stu-id="49784-127">Prevents others from opening a connection with read permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49784-128"><strong>adModeShareDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="49784-128"><strong>adModeShareDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="49784-129">8</span><span class="sxs-lookup"><span data-stu-id="49784-129">8</span></span></p></td>
<td><p><span data-ttu-id="49784-130">Verhindert, dass andere Personen eine Verbindung mit Schreibberechtigungen öffnen.</span><span class="sxs-lookup"><span data-stu-id="49784-130">Prevents others from opening a connection with write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49784-131"><strong>adModeShareExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="49784-131"><strong>adModeShareExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="49784-132">12</span><span class="sxs-lookup"><span data-stu-id="49784-132">12</span></span></p></td>
<td><p><span data-ttu-id="49784-133">Verhindert, dass andere Personen eine Verbindung öffnen.</span><span class="sxs-lookup"><span data-stu-id="49784-133">Prevents others from opening a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49784-134"><strong>adModeUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="49784-134"><strong>adModeUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="49784-135">0</span><span class="sxs-lookup"><span data-stu-id="49784-135">0</span></span></p></td>
<td><p><span data-ttu-id="49784-p104">Standardwert. Gibt an, dass die Berechtigungen noch nicht festgelegt wurden oder nicht ermittelt werden können.</span><span class="sxs-lookup"><span data-stu-id="49784-p104">Default. Indicates that the permissions have not yet been set or cannot be determined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49784-138"><strong>adModeWrite</strong></span><span class="sxs-lookup"><span data-stu-id="49784-138"><strong>adModeWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="49784-139">2</span><span class="sxs-lookup"><span data-stu-id="49784-139">2</span></span></p></td>
<td><p><span data-ttu-id="49784-140">Gibt lesegeschützte Berechtigungen an.</span><span class="sxs-lookup"><span data-stu-id="49784-140">Indicates write-only permissions.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="49784-141">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="49784-141">ADO/WFC equivalent</span></span>

<span data-ttu-id="49784-142">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="49784-142">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49784-143">Konstante</span><span class="sxs-lookup"><span data-stu-id="49784-143">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49784-144">AdoEnums.ConnectMode.READ</span><span class="sxs-lookup"><span data-stu-id="49784-144">AdoEnums.ConnectMode.READ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49784-145">AdoEnums.ConnectMode.READWRITE</span><span class="sxs-lookup"><span data-stu-id="49784-145">AdoEnums.ConnectMode.READWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49784-146">(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</span><span class="sxs-lookup"><span data-stu-id="49784-146">(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49784-147">AdoEnums.ConnectMode.SHAREDENYNONE</span><span class="sxs-lookup"><span data-stu-id="49784-147">AdoEnums.ConnectMode.SHAREDENYNONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49784-148">AdoEnums.ConnectMode.SHAREDENYREAD</span><span class="sxs-lookup"><span data-stu-id="49784-148">AdoEnums.ConnectMode.SHAREDENYREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49784-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span><span class="sxs-lookup"><span data-stu-id="49784-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49784-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span><span class="sxs-lookup"><span data-stu-id="49784-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49784-151">AdoEnums.ConnectMode.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="49784-151">AdoEnums.ConnectMode.UNKNOWN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49784-152">AdoEnums.ConnectMode.WRITE</span><span class="sxs-lookup"><span data-stu-id="49784-152">AdoEnums.ConnectMode.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

