---
title: FieldStatusEnum (Access PC-Datenbank-Referenz)
TOCTitle: FieldStatusEnum
ms:assetid: 49570042-8435-8618-3ba1-7006c47735e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249225(v=office.15)
ms:contentKeyID: 48544635
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ccf98f2a740e2a077d6e2451102bfc72bcd1b40
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709516"
---
# <a name="fieldstatusenum"></a><span data-ttu-id="197c5-102">FieldStatusEnum</span><span class="sxs-lookup"><span data-stu-id="197c5-102">FieldStatusEnum</span></span>

<span data-ttu-id="197c5-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="197c5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="197c5-104">Gibt den Status eines **Field** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="197c5-104">Specifies the status of a **Field** object.</span></span>

<span data-ttu-id="197c5-105">Die **AdFieldPending\*** -Werte geben den Vorgang an, der zum Festlegen des Status geführt hat, und können mit anderen Statuswerten kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="197c5-105">The **adFieldPending\*** values indicate the operation that caused the status to be set, and may be combined with other status values.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="197c5-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="197c5-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="197c5-107">Wert</span><span class="sxs-lookup"><span data-stu-id="197c5-107">Value</span></span></p></th>
<th><p><span data-ttu-id="197c5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="197c5-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="197c5-109"><strong>adFieldAlreadyExists</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-109"><strong>adFieldAlreadyExists</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-110">26</span><span class="sxs-lookup"><span data-stu-id="197c5-110">26</span></span></p></td>
<td><p><span data-ttu-id="197c5-111">Gibt an, dass das angegebene Feld bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="197c5-111">Indicates that the specified field already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="197c5-112"><strong>adFieldBadStatus</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-112"><strong>adFieldBadStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-113">12</span><span class="sxs-lookup"><span data-stu-id="197c5-113">12</span></span></p></td>
<td><p><span data-ttu-id="197c5-p101">Gibt an, dass aus ADO ein ungültiger Statuswert an den OLE DB-Anbieter gesendet wurde. Mögliche Ursachen sind u. a. ein OLE DB 1.0- oder 1.1-Anbieter oder eine fehlerhafte Kombination aus <a href="value-property-ado.md">Wert</a> und <a href="status-property-ado-field.md">Status</a>.</span><span class="sxs-lookup"><span data-stu-id="197c5-p101">Indicates that an invalid status value was sent from ADO to the OLE DB provider. Possible causes include an OLE DB 1.0 or 1.1 provider, or an improper combination of <a href="value-property-ado.md">Value</a> and <a href="status-property-ado-field.md">Status</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="197c5-116"><strong>adFieldCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-116"><strong>adFieldCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-117">20</span><span class="sxs-lookup"><span data-stu-id="197c5-117">20</span></span></p></td>
<td><p><span data-ttu-id="197c5-118">Gibt an, dass der Server der URL, die von <a href="source-property-ado-record.md">Quelle</a> angegeben wird, den Vorgang nicht abschließen konnte.</span><span class="sxs-lookup"><span data-stu-id="197c5-118">Indicates that the server of the URL specified by <a href="source-property-ado-record.md">Source</a> could not complete the operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="197c5-119"><strong>adFieldCannotDeleteSource</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-119"><strong>adFieldCannotDeleteSource</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-120">23</span><span class="sxs-lookup"><span data-stu-id="197c5-120">23</span></span></p></td>
<td><p><span data-ttu-id="197c5-121">Gibt an, dass eine Struktur oder eine Unterstruktur während eines Verschiebevorgangs an eine neue Position verschoben wurde, aber die Quelle nicht gelöscht werden konnte.</span><span class="sxs-lookup"><span data-stu-id="197c5-121">Indicates that during a move operation, a tree or subtree was moved to a new location, but the source could not be deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="197c5-122"><strong>adFieldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-122"><strong>adFieldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-123">2</span><span class="sxs-lookup"><span data-stu-id="197c5-123">2</span></span></p></td>
<td><p><span data-ttu-id="197c5-124">Gibt an, dass das Feld nicht ohne Datenverlust abgerufen oder gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="197c5-124">Indicates that the field cannot be retrieved or stored without loss of data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="197c5-125"><strong>adFieldCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-125"><strong>adFieldCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-126">7</span><span class="sxs-lookup"><span data-stu-id="197c5-126">7</span></span></p></td>
<td><p><span data-ttu-id="197c5-127">Gibt an, dass das Feld nicht hinzugefügt werden konnte, da der Anbieter eine Einschränkung (wie die Anzahl zulässiger Felder) überschritten hat.</span><span class="sxs-lookup"><span data-stu-id="197c5-127">Indicates that the field could not be added because the provider exceeded a limitation (such as the number of fields allowed).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="197c5-128"><strong>adFieldDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-128"><strong>adFieldDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-129">6</span><span class="sxs-lookup"><span data-stu-id="197c5-129">6</span></span></p></td>
<td><p><span data-ttu-id="197c5-130">Gibt an, dass die vom Anbieter zurückgegebenen Daten einen Überlauf beim Datentyp des Felds verursachten.</span><span class="sxs-lookup"><span data-stu-id="197c5-130">Indicates that the data returned from the provider overflowed the data type of the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="197c5-131"><strong>adFieldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-131"><strong>adFieldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-132">13</span><span class="sxs-lookup"><span data-stu-id="197c5-132">13</span></span></p></td>
<td><p><span data-ttu-id="197c5-133">Gibt an, dass beim Festlegen von Daten der Standardwert verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="197c5-133">Indicates that the default value for the field was used when setting data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="197c5-134"><strong>adFieldDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-134"><strong>adFieldDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-135">16</span><span class="sxs-lookup"><span data-stu-id="197c5-135">16</span></span></p></td>
<td><p><span data-ttu-id="197c5-136">Gibt an, dass das angegebene Feld nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="197c5-136">Indicates that the field specified does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="197c5-137"><strong>adFieldIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-137"><strong>adFieldIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-138">15</span><span class="sxs-lookup"><span data-stu-id="197c5-138">15</span></span></p></td>
<td><p><span data-ttu-id="197c5-p102">Gibt an, dass dieses Feld übersprungen wurde, als in der Quelle Datenwerte festgelegt wurden. Der Anbieter legte keinen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="197c5-p102">Indicates that this field was skipped when setting data values in the source. The provider set no value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="197c5-141"><strong>adFieldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-141"><strong>adFieldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-142">10</span><span class="sxs-lookup"><span data-stu-id="197c5-142">10</span></span></p></td>
<td><p><span data-ttu-id="197c5-143">Gibt an, dass das Feld nicht geändert werden kann, da es eine berechnete oder abgeleitete Entität ist.</span><span class="sxs-lookup"><span data-stu-id="197c5-143">Indicates that the field cannot be modified because it is a calculated or derived entity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="197c5-144"><strong>adFieldInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-144"><strong>adFieldInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-145">17</span><span class="sxs-lookup"><span data-stu-id="197c5-145">17</span></span></p></td>
<td><p><span data-ttu-id="197c5-146">Gibt an, dass die URL der Datenquelle ungültige Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="197c5-146">Indicates that the data source URL contains invalid characters.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="197c5-147"><strong>adFieldIsNull</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-147"><strong>adFieldIsNull</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-148">3</span><span class="sxs-lookup"><span data-stu-id="197c5-148">3</span></span></p></td>
<td><p><span data-ttu-id="197c5-149">Gibt an, dass der Anbieter einen VARIANT-Wert vom Typ VT_NULL zurückgegeben hat und das Feld nicht leer ist.</span><span class="sxs-lookup"><span data-stu-id="197c5-149">Indicates that the provider returned a VARIANT value of type VT_NULL and that the field is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="197c5-150"><strong>adFieldOK</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-150"><strong>adFieldOK</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-151">0</span><span class="sxs-lookup"><span data-stu-id="197c5-151">0</span></span></p></td>
<td><p><span data-ttu-id="197c5-p103">Standardwert. Gibt an, dass das Feld erfolgreich hinzugefügt oder gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="197c5-p103">Default. Indicates that the field was successfully added or deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="197c5-154"><strong>adFieldOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-154"><strong>adFieldOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-155">22</span><span class="sxs-lookup"><span data-stu-id="197c5-155">22</span></span></p></td>
<td><p><span data-ttu-id="197c5-156">Gibt an, dass der Anbieter nicht genügend Speicherplatz abrufen kann, um einen Verschiebe- oder Kopiervorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="197c5-156">Indicates that the provider is unable to obtain enough storage space to complete a move or copy operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="197c5-157"><strong>adFieldPendingChange</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-157"><strong>adFieldPendingChange</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-158">0 x 40000</span><span class="sxs-lookup"><span data-stu-id="197c5-158">0x40000</span></span></p></td>
<td><p><span data-ttu-id="197c5-p104">Gibt an, dass das Feld entweder gelöscht und dann erneut hinzugefügt wurde, gegebenenfalls mit einem anderen Datentyp, oder dass sich der Wert des Felds geändert hat, das zuvor einen Status von adFieldOK aufwies. Die endgültige Form des Felds bedeutet eine Änderung der Fields-Auflistung, nachdem die Update-Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="197c5-p104">Indicates either that the field has been deleted and then re-added, perhaps with a different data type, or that the value of the field that previously had a status of adFieldOK has changed. The final form of the field will modify the <a href="fields-collection-ado.md">Fields</a> collection after the <a href="update-method-ado.md">Update</a> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="197c5-161"><strong>adFieldPendingDelete</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-161"><strong>adFieldPendingDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-162">0 x 20000</span><span class="sxs-lookup"><span data-stu-id="197c5-162">0x20000</span></span></p></td>
<td><p><span data-ttu-id="197c5-p105">Gibt an, dass der <strong>Delete</strong>-Vorgang zum Festlegen des Status führte. Nachdem die <strong>Update</strong>-Methode aufgerufen wurde, wurde das Feld zum Löschen aus der <strong>Fields</strong>-Auflistung markiert.</span><span class="sxs-lookup"><span data-stu-id="197c5-p105">Indicates that the <strong>Delete</strong> operation caused the status to be set. The field has been marked for deletion from the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="197c5-165"><strong>adFieldPendingInsert</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-165"><strong>adFieldPendingInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-166">0 x 10000</span><span class="sxs-lookup"><span data-stu-id="197c5-166">0x10000</span></span></p></td>
<td><p><span data-ttu-id="197c5-167">Gibt an, dass der <strong>Append</strong> -Vorgang zum Festlegen den Status verursacht.</span><span class="sxs-lookup"><span data-stu-id="197c5-167">Indicates that the <strong>Append</strong> operation caused the status to be set.</span></span> <span data-ttu-id="197c5-168">Das <strong>Feld</strong> wurde markiert, der <strong>Fields</strong> -Auflistung hinzugefügt werden soll, nachdem die <strong>Update</strong> -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="197c5-168">The <strong>Field</strong> has been marked to be added to the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="197c5-169"><strong>adFieldPendingUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-169"><strong>adFieldPendingUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-170">0 x 80000</span><span class="sxs-lookup"><span data-stu-id="197c5-170">0x80000</span></span></p></td>
<td><p><span data-ttu-id="197c5-171">Gibt an, dass der Anbieter nicht ermitteln kann, welcher Vorgang zum Festlegen des Feldstatus führte.</span><span class="sxs-lookup"><span data-stu-id="197c5-171">Indicates that the provider cannot determine what operation caused field status to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="197c5-172"><strong>adFieldPendingUnknownDelete</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-172"><strong>adFieldPendingUnknownDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-173">0 x 100000</span><span class="sxs-lookup"><span data-stu-id="197c5-173">0x100000</span></span></p></td>
<td><p><span data-ttu-id="197c5-174">Gibt an, dass der Anbieter nicht ermitteln kann, welcher Vorgang zum Festlegen des Status führte, und dass das Feld aus der <strong>Fields</strong>-Auflistung gelöscht wird, nachdem die <strong>Update</strong>-Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="197c5-174">Indicates that the provider cannot determine what operation caused field status to be set, and that the field will be deleted from the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="197c5-175"><strong>adFieldPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-175"><strong>adFieldPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-176">9</span><span class="sxs-lookup"><span data-stu-id="197c5-176">9</span></span></p></td>
<td><p><span data-ttu-id="197c5-177">Gibt an, dass das Feld nicht geändert werden kann, da es als schreibgeschützt definiert ist.</span><span class="sxs-lookup"><span data-stu-id="197c5-177">Indicates that the field cannot be modified because it is defined as read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="197c5-178"><strong>adFieldReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-178"><strong>adFieldReadOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-179">24</span><span class="sxs-lookup"><span data-stu-id="197c5-179">24</span></span></p></td>
<td><p><span data-ttu-id="197c5-180">Gibt an, dass das Feld in der Datenquelle als schreibgeschützt definiert ist.</span><span class="sxs-lookup"><span data-stu-id="197c5-180">Indicates that the field in the data source is defined as read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="197c5-181"><strong>adFieldResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-181"><strong>adFieldResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-182">19</span><span class="sxs-lookup"><span data-stu-id="197c5-182">19</span></span></p></td>
<td><p><span data-ttu-id="197c5-183">Gibt an, dass der Anbieter den Vorgang nicht ausführen konnte, da an der Ziel-URL bereits ein Objekt vorhanden ist und das Objekt nicht überschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="197c5-183">Indicates that the provider was unable to perform the operation because an object already exists at the destination URL and it is not able to overwrite the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="197c5-184"><strong>adFieldResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-184"><strong>adFieldResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-185">18</span><span class="sxs-lookup"><span data-stu-id="197c5-185">18</span></span></p></td>
<td><p><span data-ttu-id="197c5-186">Gibt an, dass der Anbieter den Vorgang nicht ausführen konnte, da die Datenquelle von mindestens einer Anwendung oder mindestens einem Prozess gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="197c5-186">Indicates that the provider was unable to perform the operation because the data source is locked by one or more other application or process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="197c5-187"><strong>adFieldResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-187"><strong>adFieldResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-188">25</span><span class="sxs-lookup"><span data-stu-id="197c5-188">25</span></span></p></td>
<td><p><span data-ttu-id="197c5-189">Gibt an, dass sich eine Quell- oder Ziel-URL außerhalb des aktuellen Datensatzbereichs befindet.</span><span class="sxs-lookup"><span data-stu-id="197c5-189">Indicates that a source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="197c5-190"><strong>adFieldSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-190"><strong>adFieldSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-191">11</span><span class="sxs-lookup"><span data-stu-id="197c5-191">11</span></span></p></td>
<td><p><span data-ttu-id="197c5-192">Gibt an, dass der Wert die Datenquellschemaeinschränkung des Felds verletzt hat.</span><span class="sxs-lookup"><span data-stu-id="197c5-192">Indicates that the value violated the data source schema constraint for the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="197c5-193"><strong>adFieldSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-193"><strong>adFieldSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-194">5</span><span class="sxs-lookup"><span data-stu-id="197c5-194">5</span></span></p></td>
<td><p><span data-ttu-id="197c5-195">Gibt an, dass der vom Anbieter zurückgegebene Datenwert Vorzeichen hatte, der Datentyp des ADO-Feldwerts jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="197c5-195">Indicates that data value returned by the provider was signed but the data type of the ADO field value was unsigned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="197c5-196"><strong>adFieldTruncated</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-196"><strong>adFieldTruncated</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-197">4</span><span class="sxs-lookup"><span data-stu-id="197c5-197">4</span></span></p></td>
<td><p><span data-ttu-id="197c5-198">Gibt an, dass Daten variabler Länge beim Lesen aus der Datenquelle abgeschnitten wurden.</span><span class="sxs-lookup"><span data-stu-id="197c5-198">Indicates that variable-length data was truncated when reading from the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="197c5-199"><strong>adFieldUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-199"><strong>adFieldUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-200">8</span><span class="sxs-lookup"><span data-stu-id="197c5-200">8</span></span></p></td>
<td><p><span data-ttu-id="197c5-p107">Gibt an, dass der Anbieter den Wert beim Lesen aus der Datenquelle nicht ermitteln konnte. Beispielsweise wurde die Zeile gerade erstellt, der Standardwert für die Spalte war nicht verfügbar und ein neuer Wert wurde noch nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="197c5-p107">Indicates that the provider could not determine the value when reading from the data source. For example, the row was just created, the default value for the column was not available, and a new value had not yet been specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="197c5-203"><strong>adFieldVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="197c5-203"><strong>adFieldVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="197c5-204">21</span><span class="sxs-lookup"><span data-stu-id="197c5-204">21</span></span></p></td>
<td><p><span data-ttu-id="197c5-205">Gibt an, dass der Anbieter das von der URL angegebene Speichervolume nicht finden kann.</span><span class="sxs-lookup"><span data-stu-id="197c5-205">Indicates that the provider is unable to locate the storage volume indicated by the URL.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="197c5-206">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="197c5-206">ADO/WFC equivalent</span></span>

<span data-ttu-id="197c5-207">Diese Konstanten haben keine ADO/WFC-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="197c5-207">These constants do not have ADO/WFC equivalents.</span></span>

