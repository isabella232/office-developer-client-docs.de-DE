---
title: RightsEnum (Access PC-Datenbank-Referenz)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 40cd7f789461e5b354186c2d5b8f81ec18344435
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861981"
---
# <a name="rightsenum"></a><span data-ttu-id="b3fec-102">RightsEnum</span><span class="sxs-lookup"><span data-stu-id="b3fec-102">RightsEnum</span></span>

<span data-ttu-id="b3fec-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3fec-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b3fec-104">Gibt die Rechte oder Berechtigungen einer Gruppe oder eines Benutzers für ein Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b3fec-104">Specifies the rights or permissions for a group or user on an object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b3fec-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="b3fec-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="b3fec-106">Wert</span><span class="sxs-lookup"><span data-stu-id="b3fec-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b3fec-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3fec-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3fec-108"><strong>adRightCreate</strong></span><span class="sxs-lookup"><span data-stu-id="b3fec-108"><strong>adRightCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fec-109">16384</span><span class="sxs-lookup"><span data-stu-id="b3fec-109">16384</span></span><br />
<span data-ttu-id="b3fec-110">(&amp;H4000)</span><span class="sxs-lookup"><span data-stu-id="b3fec-110">(&amp;H4000)</span></span></p></td>
<td><p><span data-ttu-id="b3fec-111">Der Benutzer oder die Gruppe verfügt über die Berechtigung, neue Objekte dieses 'Typs zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b3fec-111">The user or group has permission to create new objects of this type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3fec-112"><strong>adRightDelete</strong></span><span class="sxs-lookup"><span data-stu-id="b3fec-112"><strong>adRightDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fec-113">65536</span><span class="sxs-lookup"><span data-stu-id="b3fec-113">65536</span></span><br />
<span data-ttu-id="b3fec-114">(&amp;H10000)</span><span class="sxs-lookup"><span data-stu-id="b3fec-114">(&amp;H10000)</span></span></p></td>
<td><p><span data-ttu-id="b3fec-p101">Der Benutzer oder die Gruppe verfügt über die Berechtigung, Daten aus einem Objekt zu löschen. Für Objekte wie <strong>Tables</strong> verfügt der Benutzer über die Berechtigung, Datenwerte aus Datensätzen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="b3fec-p101">The user or group has permission to delete data from an object. For objects such as <strong>Tables</strong>, the user has permission to delete data values from records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3fec-117"><strong>adRightDrop</strong></span><span class="sxs-lookup"><span data-stu-id="b3fec-117"><strong>adRightDrop</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fec-118">256</span><span class="sxs-lookup"><span data-stu-id="b3fec-118">256</span></span><br />
<span data-ttu-id="b3fec-119">(&amp;H100)</span><span class="sxs-lookup"><span data-stu-id="b3fec-119">(&amp;H100)</span></span></p></td>
<td><p><span data-ttu-id="b3fec-p102">Der Benutzer oder die Gruppe verfügt über die Berechtigung, Objekte aus dem Katalog zu entfernen. Beispielsweise kann <strong>Tables</strong> durch einen DROP TABLE SQL-Befehl gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="b3fec-p102">The user or group has permission to remove objects from the catalog. For example, <strong>Tables</strong> can be deleted by a DROP TABLE SQL command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3fec-122"><strong>adRightExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="b3fec-122"><strong>adRightExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fec-123">512</span><span class="sxs-lookup"><span data-stu-id="b3fec-123">512</span></span><br />
<span data-ttu-id="b3fec-124">(&amp;H200)</span><span class="sxs-lookup"><span data-stu-id="b3fec-124">(&amp;H200)</span></span></p></td>
<td><p><span data-ttu-id="b3fec-125">Der Benutzer oder die Gruppe verfügen über die Berechtigung, exklusiv auf das Objekt zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="b3fec-125">The user or group has permission to access the object exclusively.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3fec-126"><strong>adRightExecute</strong></span><span class="sxs-lookup"><span data-stu-id="b3fec-126"><strong>adRightExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fec-127">536870912</span><span class="sxs-lookup"><span data-stu-id="b3fec-127">536870912</span></span><br />
<span data-ttu-id="b3fec-128">(&amp;H20000000)</span><span class="sxs-lookup"><span data-stu-id="b3fec-128">(&amp;H20000000)</span></span></p></td>
<td><p><span data-ttu-id="b3fec-129">Der Benutzer oder die Gruppe verfügt über die Berechtigung, das Objekt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b3fec-129">The user or group has permission to execute the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3fec-130"><strong>adRightFull</strong></span><span class="sxs-lookup"><span data-stu-id="b3fec-130"><strong>adRightFull</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fec-131">268435456</span><span class="sxs-lookup"><span data-stu-id="b3fec-131">268435456</span></span><br />
<span data-ttu-id="b3fec-132">(&amp;H10000000)</span><span class="sxs-lookup"><span data-stu-id="b3fec-132">(&amp;H10000000)</span></span></p></td>
<td><p><span data-ttu-id="b3fec-133">Der Benutzer oder die Gruppe verfügt über alle Berechtigungen für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="b3fec-133">The user or group has all permissions on the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3fec-134"><strong>adRightInsert</strong></span><span class="sxs-lookup"><span data-stu-id="b3fec-134"><strong>adRightInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fec-135">32768</span><span class="sxs-lookup"><span data-stu-id="b3fec-135">32768</span></span><br />
<span data-ttu-id="b3fec-136">(&amp;H8000)</span><span class="sxs-lookup"><span data-stu-id="b3fec-136">(&amp;H8000)</span></span></p></td>
<td><p><span data-ttu-id="b3fec-p103">Der Benutzer oder die Gruppe verfügt über die Berechtigung, das Objekt einzufügen. Für Objekte wie <strong>Tables</strong> verfügt der Benutzer über die Berechtigung, Daten in die Tabelle einzufügen.</span><span class="sxs-lookup"><span data-stu-id="b3fec-p103">The user or group has permission to insert the object. For objects such as <strong>Tables</strong>, the user has permission to insert data into the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3fec-139"><strong>adRightMaximumAllowed</strong></span><span class="sxs-lookup"><span data-stu-id="b3fec-139"><strong>adRightMaximumAllowed</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fec-140">33554432 (&amp;H2000000)</span><span class="sxs-lookup"><span data-stu-id="b3fec-140">33554432 (&amp;H2000000)</span></span></p></td>
<td><p><span data-ttu-id="b3fec-p104">Der Benutzer oder die Gruppe verfügt über die durch den Anbieter maximal zulässige Anzahl von Berechtigungen. Spezifische Berechtigungen sind anbieterabhängig.</span><span class="sxs-lookup"><span data-stu-id="b3fec-p104">The user or group has the maximum number of permissions allowed by the provider. Specific permissions are provider-dependent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3fec-143"><strong>adRightNone</strong></span><span class="sxs-lookup"><span data-stu-id="b3fec-143"><strong>adRightNone</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fec-144">0</span><span class="sxs-lookup"><span data-stu-id="b3fec-144">0</span></span></p></td>
<td><p><span data-ttu-id="b3fec-145">Der Benutzer oder die Gruppe verfügt über keine Berechtigungen für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="b3fec-145">The user or group has no permissions for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3fec-146"><strong>adRightRead</strong></span><span class="sxs-lookup"><span data-stu-id="b3fec-146"><strong>adRightRead</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fec-147">-2147483648</span><span class="sxs-lookup"><span data-stu-id="b3fec-147">-2147483648</span></span><br />
<span data-ttu-id="b3fec-148">(&amp;H80000000)</span><span class="sxs-lookup"><span data-stu-id="b3fec-148">(&amp;H80000000)</span></span></p></td>
<td><p><span data-ttu-id="b3fec-p105">Der Benutzer oder die Gruppe verfügt über eine Leseberechtigung für das Objekt. Für Objekte wie <a href="table-object-adox.md">Tables</a> verfügt der Benutzer über die Berechtigung, Daten in der Tabelle zu lesen.</span><span class="sxs-lookup"><span data-stu-id="b3fec-p105">The user or group has permission to read the object. For objects such as <a href="table-object-adox.md">Tables</a>, the user has permission to read the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3fec-151"><strong>adRightReadDesign</strong></span><span class="sxs-lookup"><span data-stu-id="b3fec-151"><strong>adRightReadDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fec-152">1024</span><span class="sxs-lookup"><span data-stu-id="b3fec-152">1024</span></span><br />
<span data-ttu-id="b3fec-153">(&amp;H400)</span><span class="sxs-lookup"><span data-stu-id="b3fec-153">(&amp;H400)</span></span></p></td>
<td><p><span data-ttu-id="b3fec-154">Der Benutzer oder die Gruppe verfügt über die Berechtigung, den Entwurf für das Objekt zu lesen.</span><span class="sxs-lookup"><span data-stu-id="b3fec-154">The user or group has permission to read the design for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3fec-155"><strong>adRightReadPermissions</strong></span><span class="sxs-lookup"><span data-stu-id="b3fec-155"><strong>adRightReadPermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fec-156">131072</span><span class="sxs-lookup"><span data-stu-id="b3fec-156">131072</span></span><br />
<span data-ttu-id="b3fec-157">(&amp;H20000)</span><span class="sxs-lookup"><span data-stu-id="b3fec-157">(&amp;H20000)</span></span></p></td>
<td><p><span data-ttu-id="b3fec-158">Der Benutzer oder die Gruppe kann die spezifischen Berechtigungen für ein Objekt im Katalog anzeigen, aber nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="b3fec-158">The user or group can view, but not change, the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3fec-159"><strong>adRightReference</strong></span><span class="sxs-lookup"><span data-stu-id="b3fec-159"><strong>adRightReference</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fec-160">8192</span><span class="sxs-lookup"><span data-stu-id="b3fec-160">8192</span></span><br />
<span data-ttu-id="b3fec-161">(&amp;H2000)</span><span class="sxs-lookup"><span data-stu-id="b3fec-161">(&amp;H2000)</span></span></p></td>
<td><p><span data-ttu-id="b3fec-162">Der Benutzer oder die Gruppe verfügt über die Berechtigung, auf das Objekt zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="b3fec-162">The user or group has permission to reference the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3fec-163"><strong>adRightUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="b3fec-163"><strong>adRightUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fec-164">1073741824</span><span class="sxs-lookup"><span data-stu-id="b3fec-164">1073741824</span></span><br />
<span data-ttu-id="b3fec-165">(&amp;H40000000)</span><span class="sxs-lookup"><span data-stu-id="b3fec-165">(&amp;H40000000)</span></span></p></td>
<td><p><span data-ttu-id="b3fec-p106">Der Benutzer oder die Gruppe verfügt über die Berechtigung, das Objekt zu aktualisieren. Für Objekte wie <strong>Tables</strong> verfügt der Benutzer über die Berechtigung, die Daten in der Tabelle zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b3fec-p106">The user or group has permission to update the object. For objects such as <strong>Tables</strong>, the user has permission to update the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3fec-168"><strong>adRightWithGrant</strong></span><span class="sxs-lookup"><span data-stu-id="b3fec-168"><strong>adRightWithGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fec-169">4096</span><span class="sxs-lookup"><span data-stu-id="b3fec-169">4096</span></span><br />
<span data-ttu-id="b3fec-170">(&amp;H1000)</span><span class="sxs-lookup"><span data-stu-id="b3fec-170">(&amp;H1000)</span></span></p></td>
<td><p><span data-ttu-id="b3fec-171">Der Benutzer oder die Gruppe verfügt über die Berechtigung, Berechtigungen für das Objekt zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="b3fec-171">The user or group has permission to grant permissions on the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3fec-172"><strong>adRightWriteDesign</strong></span><span class="sxs-lookup"><span data-stu-id="b3fec-172"><strong>adRightWriteDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fec-173">2048</span><span class="sxs-lookup"><span data-stu-id="b3fec-173">2048</span></span><br />
<span data-ttu-id="b3fec-174">(&amp;H800)</span><span class="sxs-lookup"><span data-stu-id="b3fec-174">(&amp;H800)</span></span></p></td>
<td><p><span data-ttu-id="b3fec-175">Der Benutzer oder die Gruppe verfügt über die Berechtigung, den Entwurf des Objekts zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="b3fec-175">The user or group has permission to modify the design for the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3fec-176"><strong>adRightWriteOwner</strong></span><span class="sxs-lookup"><span data-stu-id="b3fec-176"><strong>adRightWriteOwner</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fec-177">524288</span><span class="sxs-lookup"><span data-stu-id="b3fec-177">524288</span></span><br />
<span data-ttu-id="b3fec-178">(&amp;H80000)</span><span class="sxs-lookup"><span data-stu-id="b3fec-178">(&amp;H80000)</span></span></p></td>
<td><p><span data-ttu-id="b3fec-179">Der Benutzer oder die Gruppe verfügt über die Berechtigung, den Besitzer des Objekts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b3fec-179">The user or group has permission to modify the owner of the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3fec-180"><strong>adRightWritePermissions</strong></span><span class="sxs-lookup"><span data-stu-id="b3fec-180"><strong>adRightWritePermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fec-181">262144</span><span class="sxs-lookup"><span data-stu-id="b3fec-181">262144</span></span><br />
<span data-ttu-id="b3fec-182">(&amp;H40000)</span><span class="sxs-lookup"><span data-stu-id="b3fec-182">(&amp;H40000)</span></span></p></td>
<td><p><span data-ttu-id="b3fec-183">Der Benutzer oder die Gruppe kann die spezifischen Berechtigungen für ein Objekt im Katalog bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="b3fec-183">The user or group can modify the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
</tbody>
</table>

