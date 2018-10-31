---
title: ConnectModeEnum (Access PC-Datenbank-Referenz)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 91d1ad892557ad944dca175a3589a74e7205ad01
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862576"
---
# <a name="connectmodeenum"></a><span data-ttu-id="921b5-102">ConnectModeEnum</span><span class="sxs-lookup"><span data-stu-id="921b5-102">ConnectModeEnum</span></span>

<span data-ttu-id="921b5-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="921b5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="921b5-104">Gibt die verfügbaren Berechtigungen zum Ändern von Daten in einer [Verbindung](connection-object-ado.md) an, wobei ein [Datensatz](record-object-ado.md) geöffnet wird oder Werte für die [Mode](mode-property-ado.md)-Eigenschaft der **Record** - und [Stream](stream-object-ado.md)-Objekte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="921b5-104">Specifies the available permissions for modifying data in a [Connection](connection-object-ado.md), opening a [Record](record-object-ado.md), or specifying values for the [Mode](mode-property-ado.md) property of the **Record** and [Stream](stream-object-ado.md) objects.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="921b5-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="921b5-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="921b5-106">Wert</span><span class="sxs-lookup"><span data-stu-id="921b5-106">Value</span></span></p></th>
<th><p><span data-ttu-id="921b5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="921b5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="921b5-108"><strong>adModeRead</strong></span><span class="sxs-lookup"><span data-stu-id="921b5-108"><strong>adModeRead</strong></span></span></p></td>
<td><p><span data-ttu-id="921b5-109">1</span><span class="sxs-lookup"><span data-stu-id="921b5-109">1</span></span></p></td>
<td><p><span data-ttu-id="921b5-110">Gibt nur schreibgeschützte Berechtigungen an.</span><span class="sxs-lookup"><span data-stu-id="921b5-110">Indicates read-only permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="921b5-111"><strong>adModeReadWrite</strong></span><span class="sxs-lookup"><span data-stu-id="921b5-111"><strong>adModeReadWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="921b5-112">3</span><span class="sxs-lookup"><span data-stu-id="921b5-112">3</span></span></p></td>
<td><p><span data-ttu-id="921b5-113">Gibt Lese-/Schreibberechtigungen an.</span><span class="sxs-lookup"><span data-stu-id="921b5-113">Indicates read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="921b5-114"><strong>adModeRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="921b5-114"><strong>adModeRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="921b5-115">0 x 400000</span><span class="sxs-lookup"><span data-stu-id="921b5-115">0x400000</span></span></p></td>
<td><p><span data-ttu-id="921b5-116">In Verbindung mit anderen <em>*ShareDeny*</em> Werte (<strong>AdModeShareDenyNone</strong>, <strong>AdModeShareDenyWrite</strong>oder <strong>AdModeShareDenyRead</strong>) weitergegeben sharing Einschränkungen auf alle untergeordneten Datensätze des aktuellen <strong>Datensatzes</strong>verwendet.</span><span class="sxs-lookup"><span data-stu-id="921b5-116">Used in conjunction with the other <em>*ShareDeny*</em> values (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>, or <strong>adModeShareDenyRead</strong>) to propagate sharing restrictions to all sub-records of the current <strong>Record</strong>.</span></span> <span data-ttu-id="921b5-117">Es hat keine Auswirkung, wenn der <strong>Datensatz</strong> keine untergeordneten Elemente verfügt.</span><span class="sxs-lookup"><span data-stu-id="921b5-117">It has no affect if the <strong>Record</strong> does not have any children.</span></span></p><p><span data-ttu-id="921b5-118">Ein Laufzeitfehler wird generiert, wenn sie nur <strong>AdModeShareDenyNone</strong> verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="921b5-118">A run-time error is generated if it is used with <strong>adModeShareDenyNone</strong> only.</span></span> <span data-ttu-id="921b5-119">Sie können jedoch mit <strong>AdModeShareDenyNone</strong> in Kombination mit anderen Werte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="921b5-119">However, it can be used with <strong>adModeShareDenyNone</strong> when combined with other values.</span></span> <span data-ttu-id="921b5-120">Sie können beispielsweise verwenden &quot; <strong>AdModeRead</strong> oder <strong>AdModeShareDenyNone</strong> oder <strong>AdModeRecursive</strong>&quot;.</span><span class="sxs-lookup"><span data-stu-id="921b5-120">For example, you can use &quot;<strong>adModeRead</strong> or <strong>adModeShareDenyNone</strong> or <strong>adModeRecursive</strong>&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="921b5-121"><strong>adModeShareDenyNone</strong></span><span class="sxs-lookup"><span data-stu-id="921b5-121"><strong>adModeShareDenyNone</strong></span></span></p></td>
<td><p><span data-ttu-id="921b5-122">16</span><span class="sxs-lookup"><span data-stu-id="921b5-122">16</span></span></p></td>
<td><p><span data-ttu-id="921b5-p103">Ermöglicht anderen Personen, eine Verbindung mit allen Berechtigungen zu öffnen. Weder der Lese- noch der Schreibzugriff kann anderen Personen verweigert werden.</span><span class="sxs-lookup"><span data-stu-id="921b5-p103">Allows others to open a connection with any permissions. Neither read nor write access can be denied to others.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="921b5-125"><strong>adModeShareDenyRead</strong></span><span class="sxs-lookup"><span data-stu-id="921b5-125"><strong>adModeShareDenyRead</strong></span></span></p></td>
<td><p><span data-ttu-id="921b5-126">4</span><span class="sxs-lookup"><span data-stu-id="921b5-126">4</span></span></p></td>
<td><p><span data-ttu-id="921b5-127">Verhindert, dass andere Personen eine Verbindung mit Leseberechtigungen öffnen.</span><span class="sxs-lookup"><span data-stu-id="921b5-127">Prevents others from opening a connection with read permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="921b5-128"><strong>adModeShareDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="921b5-128"><strong>adModeShareDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="921b5-129">8</span><span class="sxs-lookup"><span data-stu-id="921b5-129">8</span></span></p></td>
<td><p><span data-ttu-id="921b5-130">Verhindert, dass andere Personen eine Verbindung mit Schreibberechtigungen öffnen.</span><span class="sxs-lookup"><span data-stu-id="921b5-130">Prevents others from opening a connection with write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="921b5-131"><strong>adModeShareExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="921b5-131"><strong>adModeShareExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="921b5-132">12</span><span class="sxs-lookup"><span data-stu-id="921b5-132">12</span></span></p></td>
<td><p><span data-ttu-id="921b5-133">Verhindert, dass andere Personen eine Verbindung öffnen.</span><span class="sxs-lookup"><span data-stu-id="921b5-133">Prevents others from opening a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="921b5-134"><strong>adModeUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="921b5-134"><strong>adModeUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="921b5-135">0</span><span class="sxs-lookup"><span data-stu-id="921b5-135">0</span></span></p></td>
<td><p><span data-ttu-id="921b5-p104">Standardwert. Gibt an, dass die Berechtigungen noch nicht festgelegt wurden oder nicht ermittelt werden können.</span><span class="sxs-lookup"><span data-stu-id="921b5-p104">Default. Indicates that the permissions have not yet been set or cannot be determined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="921b5-138"><strong>adModeWrite</strong></span><span class="sxs-lookup"><span data-stu-id="921b5-138"><strong>adModeWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="921b5-139">2</span><span class="sxs-lookup"><span data-stu-id="921b5-139">2</span></span></p></td>
<td><p><span data-ttu-id="921b5-140">Gibt lesegeschützte Berechtigungen an.</span><span class="sxs-lookup"><span data-stu-id="921b5-140">Indicates write-only permissions.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="921b5-141">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="921b5-141">ADO/WFC equivalent</span></span>

<span data-ttu-id="921b5-142">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="921b5-142">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="921b5-143">Konstante</span><span class="sxs-lookup"><span data-stu-id="921b5-143">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="921b5-144">AdoEnums.ConnectMode.READ</span><span class="sxs-lookup"><span data-stu-id="921b5-144">AdoEnums.ConnectMode.READ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="921b5-145">AdoEnums.ConnectMode.READWRITE</span><span class="sxs-lookup"><span data-stu-id="921b5-145">AdoEnums.ConnectMode.READWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="921b5-146">(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</span><span class="sxs-lookup"><span data-stu-id="921b5-146">(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="921b5-147">AdoEnums.ConnectMode.SHAREDENYNONE</span><span class="sxs-lookup"><span data-stu-id="921b5-147">AdoEnums.ConnectMode.SHAREDENYNONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="921b5-148">AdoEnums.ConnectMode.SHAREDENYREAD</span><span class="sxs-lookup"><span data-stu-id="921b5-148">AdoEnums.ConnectMode.SHAREDENYREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="921b5-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span><span class="sxs-lookup"><span data-stu-id="921b5-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="921b5-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span><span class="sxs-lookup"><span data-stu-id="921b5-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="921b5-151">AdoEnums.ConnectMode.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="921b5-151">AdoEnums.ConnectMode.UNKNOWN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="921b5-152">AdoEnums.ConnectMode.WRITE</span><span class="sxs-lookup"><span data-stu-id="921b5-152">AdoEnums.ConnectMode.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

