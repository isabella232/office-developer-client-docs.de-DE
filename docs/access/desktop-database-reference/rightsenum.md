---
title: RightsEnum (Access PC-Datenbank-Referenz)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3c7bf2f88632265cda7537215f2ea3c68507f16f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706604"
---
# <a name="rightsenum"></a><span data-ttu-id="e547a-102">RightsEnum</span><span class="sxs-lookup"><span data-stu-id="e547a-102">RightsEnum</span></span>

<span data-ttu-id="e547a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e547a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e547a-104">Gibt die Rechte oder Berechtigungen einer Gruppe oder eines Benutzers für ein Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e547a-104">Specifies the rights or permissions for a group or user on an object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e547a-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="e547a-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="e547a-106">Wert</span><span class="sxs-lookup"><span data-stu-id="e547a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e547a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e547a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e547a-108"><strong>adRightCreate</strong></span><span class="sxs-lookup"><span data-stu-id="e547a-108"><strong>adRightCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="e547a-109">16384</span><span class="sxs-lookup"><span data-stu-id="e547a-109">16384</span></span><br />
<span data-ttu-id="e547a-110">(&amp;H4000)</span><span class="sxs-lookup"><span data-stu-id="e547a-110">(&amp;H4000)</span></span></p></td>
<td><p><span data-ttu-id="e547a-111">Der Benutzer oder die Gruppe verfügt über die Berechtigung, neue Objekte dieses 'Typs zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e547a-111">The user or group has permission to create new objects of this type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e547a-112"><strong>adRightDelete</strong></span><span class="sxs-lookup"><span data-stu-id="e547a-112"><strong>adRightDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="e547a-113">65536</span><span class="sxs-lookup"><span data-stu-id="e547a-113">65536</span></span><br />
<span data-ttu-id="e547a-114">(&amp;H10000)</span><span class="sxs-lookup"><span data-stu-id="e547a-114">(&amp;H10000)</span></span></p></td>
<td><p><span data-ttu-id="e547a-p101">Der Benutzer oder die Gruppe verfügt über die Berechtigung, Daten aus einem Objekt zu löschen. Für Objekte wie <strong>Tables</strong> verfügt der Benutzer über die Berechtigung, Datenwerte aus Datensätzen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="e547a-p101">The user or group has permission to delete data from an object. For objects such as <strong>Tables</strong>, the user has permission to delete data values from records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e547a-117"><strong>adRightDrop</strong></span><span class="sxs-lookup"><span data-stu-id="e547a-117"><strong>adRightDrop</strong></span></span></p></td>
<td><p><span data-ttu-id="e547a-118">256</span><span class="sxs-lookup"><span data-stu-id="e547a-118">256</span></span><br />
<span data-ttu-id="e547a-119">(&amp;H100)</span><span class="sxs-lookup"><span data-stu-id="e547a-119">(&amp;H100)</span></span></p></td>
<td><p><span data-ttu-id="e547a-p102">Der Benutzer oder die Gruppe verfügt über die Berechtigung, Objekte aus dem Katalog zu entfernen. Beispielsweise kann <strong>Tables</strong> durch einen DROP TABLE SQL-Befehl gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="e547a-p102">The user or group has permission to remove objects from the catalog. For example, <strong>Tables</strong> can be deleted by a DROP TABLE SQL command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e547a-122"><strong>adRightExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="e547a-122"><strong>adRightExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="e547a-123">512</span><span class="sxs-lookup"><span data-stu-id="e547a-123">512</span></span><br />
<span data-ttu-id="e547a-124">(&amp;H200)</span><span class="sxs-lookup"><span data-stu-id="e547a-124">(&amp;H200)</span></span></p></td>
<td><p><span data-ttu-id="e547a-125">Der Benutzer oder die Gruppe verfügen über die Berechtigung, exklusiv auf das Objekt zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="e547a-125">The user or group has permission to access the object exclusively.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e547a-126"><strong>adRightExecute</strong></span><span class="sxs-lookup"><span data-stu-id="e547a-126"><strong>adRightExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="e547a-127">536870912</span><span class="sxs-lookup"><span data-stu-id="e547a-127">536870912</span></span><br />
<span data-ttu-id="e547a-128">(&amp;H20000000)</span><span class="sxs-lookup"><span data-stu-id="e547a-128">(&amp;H20000000)</span></span></p></td>
<td><p><span data-ttu-id="e547a-129">Der Benutzer oder die Gruppe verfügt über die Berechtigung, das Objekt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e547a-129">The user or group has permission to execute the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e547a-130"><strong>adRightFull</strong></span><span class="sxs-lookup"><span data-stu-id="e547a-130"><strong>adRightFull</strong></span></span></p></td>
<td><p><span data-ttu-id="e547a-131">268435456</span><span class="sxs-lookup"><span data-stu-id="e547a-131">268435456</span></span><br />
<span data-ttu-id="e547a-132">(&amp;H10000000)</span><span class="sxs-lookup"><span data-stu-id="e547a-132">(&amp;H10000000)</span></span></p></td>
<td><p><span data-ttu-id="e547a-133">Der Benutzer oder die Gruppe verfügt über alle Berechtigungen für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="e547a-133">The user or group has all permissions on the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e547a-134"><strong>adRightInsert</strong></span><span class="sxs-lookup"><span data-stu-id="e547a-134"><strong>adRightInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="e547a-135">32768</span><span class="sxs-lookup"><span data-stu-id="e547a-135">32768</span></span><br />
<span data-ttu-id="e547a-136">(&amp;H8000)</span><span class="sxs-lookup"><span data-stu-id="e547a-136">(&amp;H8000)</span></span></p></td>
<td><p><span data-ttu-id="e547a-p103">Der Benutzer oder die Gruppe verfügt über die Berechtigung, das Objekt einzufügen. Für Objekte wie <strong>Tables</strong> verfügt der Benutzer über die Berechtigung, Daten in die Tabelle einzufügen.</span><span class="sxs-lookup"><span data-stu-id="e547a-p103">The user or group has permission to insert the object. For objects such as <strong>Tables</strong>, the user has permission to insert data into the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e547a-139"><strong>adRightMaximumAllowed</strong></span><span class="sxs-lookup"><span data-stu-id="e547a-139"><strong>adRightMaximumAllowed</strong></span></span></p></td>
<td><p><span data-ttu-id="e547a-140">33554432 (&amp;H2000000)</span><span class="sxs-lookup"><span data-stu-id="e547a-140">33554432 (&amp;H2000000)</span></span></p></td>
<td><p><span data-ttu-id="e547a-p104">Der Benutzer oder die Gruppe verfügt über die durch den Anbieter maximal zulässige Anzahl von Berechtigungen. Spezifische Berechtigungen sind anbieterabhängig.</span><span class="sxs-lookup"><span data-stu-id="e547a-p104">The user or group has the maximum number of permissions allowed by the provider. Specific permissions are provider-dependent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e547a-143"><strong>adRightNone</strong></span><span class="sxs-lookup"><span data-stu-id="e547a-143"><strong>adRightNone</strong></span></span></p></td>
<td><p><span data-ttu-id="e547a-144">0</span><span class="sxs-lookup"><span data-stu-id="e547a-144">0</span></span></p></td>
<td><p><span data-ttu-id="e547a-145">Der Benutzer oder die Gruppe verfügt über keine Berechtigungen für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="e547a-145">The user or group has no permissions for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e547a-146"><strong>adRightRead</strong></span><span class="sxs-lookup"><span data-stu-id="e547a-146"><strong>adRightRead</strong></span></span></p></td>
<td><p><span data-ttu-id="e547a-147">-2147483648</span><span class="sxs-lookup"><span data-stu-id="e547a-147">-2147483648</span></span><br />
<span data-ttu-id="e547a-148">(&amp;H80000000)</span><span class="sxs-lookup"><span data-stu-id="e547a-148">(&amp;H80000000)</span></span></p></td>
<td><p><span data-ttu-id="e547a-p105">Der Benutzer oder die Gruppe verfügt über eine Leseberechtigung für das Objekt. Für Objekte wie <a href="table-object-adox.md">Tables</a> verfügt der Benutzer über die Berechtigung, Daten in der Tabelle zu lesen.</span><span class="sxs-lookup"><span data-stu-id="e547a-p105">The user or group has permission to read the object. For objects such as <a href="table-object-adox.md">Tables</a>, the user has permission to read the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e547a-151"><strong>adRightReadDesign</strong></span><span class="sxs-lookup"><span data-stu-id="e547a-151"><strong>adRightReadDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="e547a-152">1024</span><span class="sxs-lookup"><span data-stu-id="e547a-152">1024</span></span><br />
<span data-ttu-id="e547a-153">(&amp;H400)</span><span class="sxs-lookup"><span data-stu-id="e547a-153">(&amp;H400)</span></span></p></td>
<td><p><span data-ttu-id="e547a-154">Der Benutzer oder die Gruppe verfügt über die Berechtigung, den Entwurf für das Objekt zu lesen.</span><span class="sxs-lookup"><span data-stu-id="e547a-154">The user or group has permission to read the design for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e547a-155"><strong>adRightReadPermissions</strong></span><span class="sxs-lookup"><span data-stu-id="e547a-155"><strong>adRightReadPermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="e547a-156">131072</span><span class="sxs-lookup"><span data-stu-id="e547a-156">131072</span></span><br />
<span data-ttu-id="e547a-157">(&amp;H20000)</span><span class="sxs-lookup"><span data-stu-id="e547a-157">(&amp;H20000)</span></span></p></td>
<td><p><span data-ttu-id="e547a-158">Der Benutzer oder die Gruppe kann die spezifischen Berechtigungen für ein Objekt im Katalog anzeigen, aber nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="e547a-158">The user or group can view, but not change, the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e547a-159"><strong>adRightReference</strong></span><span class="sxs-lookup"><span data-stu-id="e547a-159"><strong>adRightReference</strong></span></span></p></td>
<td><p><span data-ttu-id="e547a-160">8192</span><span class="sxs-lookup"><span data-stu-id="e547a-160">8192</span></span><br />
<span data-ttu-id="e547a-161">(&amp;H2000)</span><span class="sxs-lookup"><span data-stu-id="e547a-161">(&amp;H2000)</span></span></p></td>
<td><p><span data-ttu-id="e547a-162">Der Benutzer oder die Gruppe verfügt über die Berechtigung, auf das Objekt zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="e547a-162">The user or group has permission to reference the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e547a-163"><strong>adRightUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="e547a-163"><strong>adRightUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="e547a-164">1073741824</span><span class="sxs-lookup"><span data-stu-id="e547a-164">1073741824</span></span><br />
<span data-ttu-id="e547a-165">(&amp;H40000000)</span><span class="sxs-lookup"><span data-stu-id="e547a-165">(&amp;H40000000)</span></span></p></td>
<td><p><span data-ttu-id="e547a-p106">Der Benutzer oder die Gruppe verfügt über die Berechtigung, das Objekt zu aktualisieren. Für Objekte wie <strong>Tables</strong> verfügt der Benutzer über die Berechtigung, die Daten in der Tabelle zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e547a-p106">The user or group has permission to update the object. For objects such as <strong>Tables</strong>, the user has permission to update the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e547a-168"><strong>adRightWithGrant</strong></span><span class="sxs-lookup"><span data-stu-id="e547a-168"><strong>adRightWithGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="e547a-169">4096</span><span class="sxs-lookup"><span data-stu-id="e547a-169">4096</span></span><br />
<span data-ttu-id="e547a-170">(&amp;H1000)</span><span class="sxs-lookup"><span data-stu-id="e547a-170">(&amp;H1000)</span></span></p></td>
<td><p><span data-ttu-id="e547a-171">Der Benutzer oder die Gruppe verfügt über die Berechtigung, Berechtigungen für das Objekt zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="e547a-171">The user or group has permission to grant permissions on the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e547a-172"><strong>adRightWriteDesign</strong></span><span class="sxs-lookup"><span data-stu-id="e547a-172"><strong>adRightWriteDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="e547a-173">2048</span><span class="sxs-lookup"><span data-stu-id="e547a-173">2048</span></span><br />
<span data-ttu-id="e547a-174">(&amp;H800)</span><span class="sxs-lookup"><span data-stu-id="e547a-174">(&amp;H800)</span></span></p></td>
<td><p><span data-ttu-id="e547a-175">Der Benutzer oder die Gruppe verfügt über die Berechtigung, den Entwurf des Objekts zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e547a-175">The user or group has permission to modify the design for the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e547a-176"><strong>adRightWriteOwner</strong></span><span class="sxs-lookup"><span data-stu-id="e547a-176"><strong>adRightWriteOwner</strong></span></span></p></td>
<td><p><span data-ttu-id="e547a-177">524288</span><span class="sxs-lookup"><span data-stu-id="e547a-177">524288</span></span><br />
<span data-ttu-id="e547a-178">(&amp;H80000)</span><span class="sxs-lookup"><span data-stu-id="e547a-178">(&amp;H80000)</span></span></p></td>
<td><p><span data-ttu-id="e547a-179">Der Benutzer oder die Gruppe verfügt über die Berechtigung, den Besitzer des Objekts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e547a-179">The user or group has permission to modify the owner of the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e547a-180"><strong>adRightWritePermissions</strong></span><span class="sxs-lookup"><span data-stu-id="e547a-180"><strong>adRightWritePermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="e547a-181">262144</span><span class="sxs-lookup"><span data-stu-id="e547a-181">262144</span></span><br />
<span data-ttu-id="e547a-182">(&amp;H40000)</span><span class="sxs-lookup"><span data-stu-id="e547a-182">(&amp;H40000)</span></span></p></td>
<td><p><span data-ttu-id="e547a-183">Der Benutzer oder die Gruppe kann die spezifischen Berechtigungen für ein Objekt im Katalog bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e547a-183">The user or group can modify the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
</tbody>
</table>

