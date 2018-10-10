---
title: RightsEnum (Access PC-Datenbank-Referenz)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ffc964be66649536b89e7f95ace1325eddee6169
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474117"
---
# <a name="rightsenum"></a><span data-ttu-id="5ad24-102">RightsEnum</span><span class="sxs-lookup"><span data-stu-id="5ad24-102">RightsEnum</span></span>


<span data-ttu-id="5ad24-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ad24-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5ad24-104">Gibt die Rechte oder Berechtigungen einer Gruppe oder eines Benutzers für ein Objekt an.</span><span class="sxs-lookup"><span data-stu-id="5ad24-104">Specifies the rights or permissions for a group or user on an object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ad24-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="5ad24-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="5ad24-106">Wert</span><span class="sxs-lookup"><span data-stu-id="5ad24-106">Value</span></span></p></th>
<th><p><span data-ttu-id="5ad24-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ad24-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ad24-108"><strong>adRightCreate</strong></span><span class="sxs-lookup"><span data-stu-id="5ad24-108"><strong>adRightCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad24-109">16384</span><span class="sxs-lookup"><span data-stu-id="5ad24-109">16384</span></span><br />
<span data-ttu-id="5ad24-110">(&amp;H4000)</span><span class="sxs-lookup"><span data-stu-id="5ad24-110">(&amp;H4000)</span></span></p></td>
<td><p><span data-ttu-id="5ad24-111">Der Benutzer oder die Gruppe verfügt über die Berechtigung, neue Objekte dieses 'Typs zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5ad24-111">The user or group has permission to create new objects of this type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ad24-112"><strong>adRightDelete</strong></span><span class="sxs-lookup"><span data-stu-id="5ad24-112"><strong>adRightDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad24-113">65536</span><span class="sxs-lookup"><span data-stu-id="5ad24-113">65536</span></span><br />
<span data-ttu-id="5ad24-114">(&amp;H10000)</span><span class="sxs-lookup"><span data-stu-id="5ad24-114">(&amp;H10000)</span></span></p></td>
<td><p><span data-ttu-id="5ad24-p101">Der Benutzer oder die Gruppe verfügt über die Berechtigung, Daten aus einem Objekt zu löschen. Für Objekte wie <strong>Tables</strong> verfügt der Benutzer über die Berechtigung, Datenwerte aus Datensätzen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="5ad24-p101">The user or group has permission to delete data from an object. For objects such as <strong>Tables</strong>, the user has permission to delete data values from records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ad24-117"><strong>adRightDrop</strong></span><span class="sxs-lookup"><span data-stu-id="5ad24-117"><strong>adRightDrop</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad24-118">256</span><span class="sxs-lookup"><span data-stu-id="5ad24-118">256</span></span><br />
<span data-ttu-id="5ad24-119">(&amp;H100)</span><span class="sxs-lookup"><span data-stu-id="5ad24-119">(&amp;H100)</span></span></p></td>
<td><p><span data-ttu-id="5ad24-p102">Der Benutzer oder die Gruppe verfügt über die Berechtigung, Objekte aus dem Katalog zu entfernen. Beispielsweise kann <strong>Tables</strong> durch einen DROP TABLE SQL-Befehl gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="5ad24-p102">The user or group has permission to remove objects from the catalog. For example, <strong>Tables</strong> can be deleted by a DROP TABLE SQL command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ad24-122"><strong>adRightExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="5ad24-122"><strong>adRightExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad24-123">512</span><span class="sxs-lookup"><span data-stu-id="5ad24-123">512</span></span><br />
<span data-ttu-id="5ad24-124">(&amp;H200)</span><span class="sxs-lookup"><span data-stu-id="5ad24-124">(&amp;H200)</span></span></p></td>
<td><p><span data-ttu-id="5ad24-125">Der Benutzer oder die Gruppe verfügen über die Berechtigung, exklusiv auf das Objekt zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="5ad24-125">The user or group has permission to access the object exclusively.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ad24-126"><strong>adRightExecute</strong></span><span class="sxs-lookup"><span data-stu-id="5ad24-126"><strong>adRightExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad24-127">536870912</span><span class="sxs-lookup"><span data-stu-id="5ad24-127">536870912</span></span><br />
<span data-ttu-id="5ad24-128">(&amp;H20000000)</span><span class="sxs-lookup"><span data-stu-id="5ad24-128">(&amp;H20000000)</span></span></p></td>
<td><p><span data-ttu-id="5ad24-129">Der Benutzer oder die Gruppe verfügt über die Berechtigung, das Objekt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5ad24-129">The user or group has permission to execute the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ad24-130"><strong>adRightFull</strong></span><span class="sxs-lookup"><span data-stu-id="5ad24-130"><strong>adRightFull</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad24-131">268435456</span><span class="sxs-lookup"><span data-stu-id="5ad24-131">268435456</span></span><br />
<span data-ttu-id="5ad24-132">(&amp;H10000000)</span><span class="sxs-lookup"><span data-stu-id="5ad24-132">(&amp;H10000000)</span></span></p></td>
<td><p><span data-ttu-id="5ad24-133">Der Benutzer oder die Gruppe verfügt über alle Berechtigungen für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="5ad24-133">The user or group has all permissions on the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ad24-134"><strong>adRightInsert</strong></span><span class="sxs-lookup"><span data-stu-id="5ad24-134"><strong>adRightInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad24-135">32768</span><span class="sxs-lookup"><span data-stu-id="5ad24-135">32768</span></span><br />
<span data-ttu-id="5ad24-136">(&amp;H8000)</span><span class="sxs-lookup"><span data-stu-id="5ad24-136">(&amp;H8000)</span></span></p></td>
<td><p><span data-ttu-id="5ad24-p103">Der Benutzer oder die Gruppe verfügt über die Berechtigung, das Objekt einzufügen. Für Objekte wie <strong>Tables</strong> verfügt der Benutzer über die Berechtigung, Daten in die Tabelle einzufügen.</span><span class="sxs-lookup"><span data-stu-id="5ad24-p103">The user or group has permission to insert the object. For objects such as <strong>Tables</strong>, the user has permission to insert data into the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ad24-139"><strong>adRightMaximumAllowed</strong></span><span class="sxs-lookup"><span data-stu-id="5ad24-139"><strong>adRightMaximumAllowed</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad24-140">33554432 (&amp;H2000000)</span><span class="sxs-lookup"><span data-stu-id="5ad24-140">33554432 (&amp;H2000000)</span></span></p></td>
<td><p><span data-ttu-id="5ad24-p104">Der Benutzer oder die Gruppe verfügt über die durch den Anbieter maximal zulässige Anzahl von Berechtigungen. Spezifische Berechtigungen sind anbieterabhängig.</span><span class="sxs-lookup"><span data-stu-id="5ad24-p104">The user or group has the maximum number of permissions allowed by the provider. Specific permissions are provider-dependent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ad24-143"><strong>adRightNone</strong></span><span class="sxs-lookup"><span data-stu-id="5ad24-143"><strong>adRightNone</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad24-144">0</span><span class="sxs-lookup"><span data-stu-id="5ad24-144">0</span></span></p></td>
<td><p><span data-ttu-id="5ad24-145">Der Benutzer oder die Gruppe verfügt über keine Berechtigungen für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="5ad24-145">The user or group has no permissions for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ad24-146"><strong>adRightRead</strong></span><span class="sxs-lookup"><span data-stu-id="5ad24-146"><strong>adRightRead</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad24-147">-2147483648</span><span class="sxs-lookup"><span data-stu-id="5ad24-147">-2147483648</span></span><br />
<span data-ttu-id="5ad24-148">(&amp;H80000000)</span><span class="sxs-lookup"><span data-stu-id="5ad24-148">(&amp;H80000000)</span></span></p></td>
<td><p><span data-ttu-id="5ad24-p105">Der Benutzer oder die Gruppe verfügt über eine Leseberechtigung für das Objekt. Für Objekte wie <a href="table-object-adox.md">Tables</a> verfügt der Benutzer über die Berechtigung, Daten in der Tabelle zu lesen.</span><span class="sxs-lookup"><span data-stu-id="5ad24-p105">The user or group has permission to read the object. For objects such as <a href="table-object-adox.md">Tables</a>, the user has permission to read the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ad24-151"><strong>adRightReadDesign</strong></span><span class="sxs-lookup"><span data-stu-id="5ad24-151"><strong>adRightReadDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad24-152">1024</span><span class="sxs-lookup"><span data-stu-id="5ad24-152">1024</span></span><br />
<span data-ttu-id="5ad24-153">(&amp;H400)</span><span class="sxs-lookup"><span data-stu-id="5ad24-153">(&amp;H400)</span></span></p></td>
<td><p><span data-ttu-id="5ad24-154">Der Benutzer oder die Gruppe verfügt über die Berechtigung, den Entwurf für das Objekt zu lesen.</span><span class="sxs-lookup"><span data-stu-id="5ad24-154">The user or group has permission to read the design for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ad24-155"><strong>adRightReadPermissions</strong></span><span class="sxs-lookup"><span data-stu-id="5ad24-155"><strong>adRightReadPermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad24-156">131072</span><span class="sxs-lookup"><span data-stu-id="5ad24-156">131072</span></span><br />
<span data-ttu-id="5ad24-157">(&amp;H20000)</span><span class="sxs-lookup"><span data-stu-id="5ad24-157">(&amp;H20000)</span></span></p></td>
<td><p><span data-ttu-id="5ad24-158">Der Benutzer oder die Gruppe kann die spezifischen Berechtigungen für ein Objekt im Katalog anzeigen, aber nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="5ad24-158">The user or group can view, but not change, the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ad24-159"><strong>adRightReference</strong></span><span class="sxs-lookup"><span data-stu-id="5ad24-159"><strong>adRightReference</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad24-160">8192</span><span class="sxs-lookup"><span data-stu-id="5ad24-160">8192</span></span><br />
<span data-ttu-id="5ad24-161">(&amp;H2000)</span><span class="sxs-lookup"><span data-stu-id="5ad24-161">(&amp;H2000)</span></span></p></td>
<td><p><span data-ttu-id="5ad24-162">Der Benutzer oder die Gruppe verfügt über die Berechtigung, auf das Objekt zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="5ad24-162">The user or group has permission to reference the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ad24-163"><strong>adRightUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="5ad24-163"><strong>adRightUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad24-164">1073741824</span><span class="sxs-lookup"><span data-stu-id="5ad24-164">1073741824</span></span><br />
<span data-ttu-id="5ad24-165">(&amp;H40000000)</span><span class="sxs-lookup"><span data-stu-id="5ad24-165">(&amp;H40000000)</span></span></p></td>
<td><p><span data-ttu-id="5ad24-p106">Der Benutzer oder die Gruppe verfügt über die Berechtigung, das Objekt zu aktualisieren. Für Objekte wie <strong>Tables</strong> verfügt der Benutzer über die Berechtigung, die Daten in der Tabelle zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5ad24-p106">The user or group has permission to update the object. For objects such as <strong>Tables</strong>, the user has permission to update the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ad24-168"><strong>adRightWithGrant</strong></span><span class="sxs-lookup"><span data-stu-id="5ad24-168"><strong>adRightWithGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad24-169">4096</span><span class="sxs-lookup"><span data-stu-id="5ad24-169">4096</span></span><br />
<span data-ttu-id="5ad24-170">(&amp;H1000)</span><span class="sxs-lookup"><span data-stu-id="5ad24-170">(&amp;H1000)</span></span></p></td>
<td><p><span data-ttu-id="5ad24-171">Der Benutzer oder die Gruppe verfügt über die Berechtigung, Berechtigungen für das Objekt zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="5ad24-171">The user or group has permission to grant permissions on the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ad24-172"><strong>adRightWriteDesign</strong></span><span class="sxs-lookup"><span data-stu-id="5ad24-172"><strong>adRightWriteDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad24-173">2048</span><span class="sxs-lookup"><span data-stu-id="5ad24-173">2048</span></span><br />
<span data-ttu-id="5ad24-174">(&amp;H800)</span><span class="sxs-lookup"><span data-stu-id="5ad24-174">(&amp;H800)</span></span></p></td>
<td><p><span data-ttu-id="5ad24-175">Der Benutzer oder die Gruppe verfügt über die Berechtigung, den Entwurf des Objekts zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="5ad24-175">The user or group has permission to modify the design for the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ad24-176"><strong>adRightWriteOwner</strong></span><span class="sxs-lookup"><span data-stu-id="5ad24-176"><strong>adRightWriteOwner</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad24-177">524288</span><span class="sxs-lookup"><span data-stu-id="5ad24-177">524288</span></span><br />
<span data-ttu-id="5ad24-178">(&amp;H80000)</span><span class="sxs-lookup"><span data-stu-id="5ad24-178">(&amp;H80000)</span></span></p></td>
<td><p><span data-ttu-id="5ad24-179">Der Benutzer oder die Gruppe verfügt über die Berechtigung, den Besitzer des Objekts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5ad24-179">The user or group has permission to modify the owner of the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ad24-180"><strong>adRightWritePermissions</strong></span><span class="sxs-lookup"><span data-stu-id="5ad24-180"><strong>adRightWritePermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad24-181">262144</span><span class="sxs-lookup"><span data-stu-id="5ad24-181">262144</span></span><br />
<span data-ttu-id="5ad24-182">(&amp;H40000)</span><span class="sxs-lookup"><span data-stu-id="5ad24-182">(&amp;H40000)</span></span></p></td>
<td><p><span data-ttu-id="5ad24-183">Der Benutzer oder die Gruppe kann die spezifischen Berechtigungen für ein Objekt im Katalog bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="5ad24-183">The user or group can modify the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
</tbody>
</table>

