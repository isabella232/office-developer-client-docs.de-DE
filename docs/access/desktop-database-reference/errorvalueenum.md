---
title: ErrorValueEnum (Access PC-Datenbank-Referenz)
TOCTitle: ErrorValueEnum
ms:assetid: 2af99f32-6004-1225-367c-45d693f447b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249058(v=office.15)
ms:contentKeyID: 48543921
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c2d4207f157d361f3b8aba2ff80f46d06b2f328e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717664"
---
# <a name="errorvalueenum"></a><span data-ttu-id="94b0c-102">ErrorValueEnum</span><span class="sxs-lookup"><span data-stu-id="94b0c-102">ErrorValueEnum</span></span>

<span data-ttu-id="94b0c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="94b0c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="94b0c-104">Gibt den Typ des ADO-Laufzeitfehlers an.</span><span class="sxs-lookup"><span data-stu-id="94b0c-104">Specifies the type of ADO run-time error.</span></span>

<span data-ttu-id="94b0c-105">Es werden drei Fehlernummerntypen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="94b0c-105">Three forms of the error number are listed:</span></span>

- <span data-ttu-id="94b0c-p101">Positive Dezimalzahl - die niedrigen zwei Bytes der vollständigen Zahl im Dezimalstellenformat. Diese Nummer wird im Standard-Fehlermeldungsdialogfeld von Visual Basic angezeigt. Zum Beispiel Laufzeitfehler "3707".</span><span class="sxs-lookup"><span data-stu-id="94b0c-p101">Positive decimal — the low two bytes of the full number in decimal format. This number is displayed in the default Visual Basic error message dialog box. For example, Run-time error '3707'.</span></span>

- <span data-ttu-id="94b0c-109">Negative Dezimalzahl - die Dezimalübersetzung der vollständigen Fehlernummer.</span><span class="sxs-lookup"><span data-stu-id="94b0c-109">Negative decimal — The decimal translation of the full error number.</span></span>

- <span data-ttu-id="94b0c-p102">Hexadezimal – die hexadezimale Darstellung der vollständigen Fehlernummer. Der Windows-Einrichtungscode befindet sich in der vierten Ziffer. *A* ist der Einrichtungscode für ADO-Fehlernummern. Beispielsweise: 0x800 ***A*** 0E7B.</span><span class="sxs-lookup"><span data-stu-id="94b0c-p102">Hexadecimal — The hexadecimal representation of the full error number. The Windows facility code is in the fourth digit. The facility code for ADO error numbers is *A*. For example: 0x800***A***0E7B.</span></span>

> [!NOTE]
> <span data-ttu-id="94b0c-113">OLE DB-Fehler können an Ihre ADO-Anwendung übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="94b0c-113">OLE DB errors may be passed to your ADO application.</span></span> <span data-ttu-id="94b0c-114">Diese können in der Regel durch einen Windows Facility Code von *4*identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="94b0c-114">Typically, these can be identified by a Windows facility code of *4*.</span></span> <span data-ttu-id="94b0c-115">Beispielsweise 0x800_**4**_... Weitere Informationen zu diesen Nummern finden Sie in Kapitel 16 von der *OLE DB-Programmierreferenz.*</span><span class="sxs-lookup"><span data-stu-id="94b0c-115">For example, 0x800_**4**_.... For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="94b0c-116">Konstante</span><span class="sxs-lookup"><span data-stu-id="94b0c-116">Constant</span></span></p></th>
<th><p><span data-ttu-id="94b0c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="94b0c-117">Value</span></span></p></th>
<th><p><span data-ttu-id="94b0c-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94b0c-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-119"><strong>adErrBoundToCommand</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-119"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-120">3707</span><span class="sxs-lookup"><span data-stu-id="94b0c-120">3707</span></span><br />
<span data-ttu-id="94b0c-121">-2146824581</span><span class="sxs-lookup"><span data-stu-id="94b0c-121">-2146824581</span></span><br />
<span data-ttu-id="94b0c-122">0x800A0E7B</span><span class="sxs-lookup"><span data-stu-id="94b0c-122">0x800A0E7B</span></span></p></td>
<td><p><span data-ttu-id="94b0c-123">Kann die <strong>ActiveConnection</strong>-Eigenschaft eines <strong>Recordset</strong>-Objekts nicht ändern, das als Quelle ein <strong>Command</strong>-Objekt besitzt.</span><span class="sxs-lookup"><span data-stu-id="94b0c-123">Cannot change the <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object which has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-124"><strong>adErrCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-124"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-125">3732</span><span class="sxs-lookup"><span data-stu-id="94b0c-125">3732</span></span><br />
<span data-ttu-id="94b0c-126">-2146824556</span><span class="sxs-lookup"><span data-stu-id="94b0c-126">-2146824556</span></span><br />
<span data-ttu-id="94b0c-127">0x800A0E94</span><span class="sxs-lookup"><span data-stu-id="94b0c-127">0x800A0E94</span></span></p></td>
<td><p><span data-ttu-id="94b0c-128">Server kann den Vorgang nicht abschließen.</span><span class="sxs-lookup"><span data-stu-id="94b0c-128">Server cannot complete the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-129"><strong>adErrCantChangeConnection</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-129"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-130">3748</span><span class="sxs-lookup"><span data-stu-id="94b0c-130">3748</span></span><br />
<span data-ttu-id="94b0c-131">-2146824540</span><span class="sxs-lookup"><span data-stu-id="94b0c-131">-2146824540</span></span><br />
<span data-ttu-id="94b0c-132">0x800A0EA4</span><span class="sxs-lookup"><span data-stu-id="94b0c-132">0x800A0EA4</span></span></p></td>
<td><p><span data-ttu-id="94b0c-p104">Verbindung wurde verweigert. Die von Ihnen angeforderte neue Verbindung weist andere Eigenschaften als die bereits verwendete auf.</span><span class="sxs-lookup"><span data-stu-id="94b0c-p104">Connection was denied. New connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-135"><strong>adErrCantChangeProvider</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-135"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-136">3220</span><span class="sxs-lookup"><span data-stu-id="94b0c-136">3220</span></span><br />
<span data-ttu-id="94b0c-137">-2146825068</span><span class="sxs-lookup"><span data-stu-id="94b0c-137">-2146825068</span></span><br />
<span data-ttu-id="94b0c-138">0X800A0C94</span><span class="sxs-lookup"><span data-stu-id="94b0c-138">0X800A0C94</span></span></p></td>
<td><p><span data-ttu-id="94b0c-139">Der bereitgestellte Anbieter unterscheidet sich von dem bereits verwendeten Anbieter.</span><span class="sxs-lookup"><span data-stu-id="94b0c-139">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-140"><strong>adErrCantConvertvalue</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-140"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-141">3724</span><span class="sxs-lookup"><span data-stu-id="94b0c-141">3724</span></span><br />
<span data-ttu-id="94b0c-142">-2146824564</span><span class="sxs-lookup"><span data-stu-id="94b0c-142">-2146824564</span></span><br />
<span data-ttu-id="94b0c-143">0x800A0E8C</span><span class="sxs-lookup"><span data-stu-id="94b0c-143">0x800A0E8C</span></span></p></td>
<td><p><span data-ttu-id="94b0c-p105">Der Datenwert kann aus anderen Gründen als einem Vorzeichenkonflikt oder einem Datenüberlauf nicht konvertiert werden. Beispielsweise könnten bei der Konvertierung Daten abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="94b0c-p105">Data value cannot be converted for reasons other than sign mismatch or data overflow. For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-146"><strong>adErrCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-146"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-147">3725</span><span class="sxs-lookup"><span data-stu-id="94b0c-147">3725</span></span><br />
<span data-ttu-id="94b0c-148">-2146824563</span><span class="sxs-lookup"><span data-stu-id="94b0c-148">-2146824563</span></span><br />
<span data-ttu-id="94b0c-149">0x800A0E8D</span><span class="sxs-lookup"><span data-stu-id="94b0c-149">0x800A0E8D</span></span></p></td>
<td><p><span data-ttu-id="94b0c-150">Der Datenwert kann nicht festgelegt oder abgerufen werden, da der Felddatentyp unbekannt war, oder der Anbieter verfügte über unzureichende Ressourcen zum Ausführen des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="94b0c-150">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-151"><strong>adErrCatalogNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-151"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-152">3747</span><span class="sxs-lookup"><span data-stu-id="94b0c-152">3747</span></span><br />
<span data-ttu-id="94b0c-153">-2146824541</span><span class="sxs-lookup"><span data-stu-id="94b0c-153">-2146824541</span></span><br />
<span data-ttu-id="94b0c-154">0x800A0EA3</span><span class="sxs-lookup"><span data-stu-id="94b0c-154">0x800A0EA3</span></span></p></td>
<td><p><span data-ttu-id="94b0c-155">Für den Vorgang ist ein gültiger <strong>ParentCatalog</strong> erforderlich.</span><span class="sxs-lookup"><span data-stu-id="94b0c-155">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-156"><strong>adErrColumnNotOnThisRow</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-156"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-157">3726</span><span class="sxs-lookup"><span data-stu-id="94b0c-157">3726</span></span><br />
<span data-ttu-id="94b0c-158">-2146824562</span><span class="sxs-lookup"><span data-stu-id="94b0c-158">-2146824562</span></span><br />
<span data-ttu-id="94b0c-159">0x800A0E8E</span><span class="sxs-lookup"><span data-stu-id="94b0c-159">0x800A0E8E</span></span></p></td>
<td><p><span data-ttu-id="94b0c-160">Der Datensatz enthält dieses Feld nicht.</span><span class="sxs-lookup"><span data-stu-id="94b0c-160">Record does not contain this field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-161"><strong>adErrDataConversion</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-161"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-162">3421</span><span class="sxs-lookup"><span data-stu-id="94b0c-162">3421</span></span><br />
<span data-ttu-id="94b0c-163">-2146824867</span><span class="sxs-lookup"><span data-stu-id="94b0c-163">-2146824867</span></span><br />
<span data-ttu-id="94b0c-164">0x800A0D5D</span><span class="sxs-lookup"><span data-stu-id="94b0c-164">0x800A0D5D</span></span></p></td>
<td><p><span data-ttu-id="94b0c-165">Die Anwendung verwendet für den aktuellen Vorgang einen Wert des falschen Datentyps.</span><span class="sxs-lookup"><span data-stu-id="94b0c-165">Application uses a value of the wrong type for the current operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-166"><strong>adErrDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-166"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-167">3721</span><span class="sxs-lookup"><span data-stu-id="94b0c-167">3721</span></span><br />
<span data-ttu-id="94b0c-168">-2146824567</span><span class="sxs-lookup"><span data-stu-id="94b0c-168">-2146824567</span></span><br />
<span data-ttu-id="94b0c-169">0x800A0E89</span><span class="sxs-lookup"><span data-stu-id="94b0c-169">0x800A0E89</span></span></p></td>
<td><p><span data-ttu-id="94b0c-170">Der Datenwert ist zu groß, um vom Felddatentyp dargestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="94b0c-170">Data value is too large to be represented by the field data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-171"><strong>adErrDelResOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-171"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-172">3738</span><span class="sxs-lookup"><span data-stu-id="94b0c-172">3738</span></span><br />
<span data-ttu-id="94b0c-173">-2146824550</span><span class="sxs-lookup"><span data-stu-id="94b0c-173">-2146824550</span></span><br />
<span data-ttu-id="94b0c-174">0x800A0E9A</span><span class="sxs-lookup"><span data-stu-id="94b0c-174">0x800A0E9A</span></span></p></td>
<td><p><span data-ttu-id="94b0c-175">URL des zu löschenden Objekts befindet sich außerhalb des aktuellen Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="94b0c-175">URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-176"><strong>adErrDenyNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-176"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-177">3750</span><span class="sxs-lookup"><span data-stu-id="94b0c-177">3750</span></span><br />
<span data-ttu-id="94b0c-178">-2146824538</span><span class="sxs-lookup"><span data-stu-id="94b0c-178">-2146824538</span></span><br />
<span data-ttu-id="94b0c-179">0x800A0EA6</span><span class="sxs-lookup"><span data-stu-id="94b0c-179">0x800A0EA6</span></span></p></td>
<td><p><span data-ttu-id="94b0c-180">Der Anbieter unterstützt Freigabeeinschränkungen nicht.</span><span class="sxs-lookup"><span data-stu-id="94b0c-180">Provider does not support sharing restrictions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-181"><strong>adErrDenyTypeNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-181"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-182">3751</span><span class="sxs-lookup"><span data-stu-id="94b0c-182">3751</span></span><br />
<span data-ttu-id="94b0c-183">-2146824537</span><span class="sxs-lookup"><span data-stu-id="94b0c-183">-2146824537</span></span><br />
<span data-ttu-id="94b0c-184">0x800A0EA7</span><span class="sxs-lookup"><span data-stu-id="94b0c-184">0x800A0EA7</span></span></p></td>
<td><p><span data-ttu-id="94b0c-185">Der Anbieter unterstützt die angeforderte Art von Freigabeeinschränkung nicht.</span><span class="sxs-lookup"><span data-stu-id="94b0c-185">Provider does not support the requested kind of sharing restriction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-186"><strong>adErrFeatureNotAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-186"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-187">3251</span><span class="sxs-lookup"><span data-stu-id="94b0c-187">3251</span></span><br />
<span data-ttu-id="94b0c-188">-2146825037</span><span class="sxs-lookup"><span data-stu-id="94b0c-188">-2146825037</span></span><br />
<span data-ttu-id="94b0c-189">0x800A0CB3</span><span class="sxs-lookup"><span data-stu-id="94b0c-189">0x800A0CB3</span></span></p></td>
<td><p><span data-ttu-id="94b0c-190">Objekt oder Anbieter kann den angeforderten Vorgang nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="94b0c-190">Object or provider is not capable of performing requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-191"><strong>adErrFieldsUpdateFailed</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-191"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-192">3749</span><span class="sxs-lookup"><span data-stu-id="94b0c-192">3749</span></span><br />
<span data-ttu-id="94b0c-193">-2146824539</span><span class="sxs-lookup"><span data-stu-id="94b0c-193">-2146824539</span></span><br />
<span data-ttu-id="94b0c-194">0x800A0EA5</span><span class="sxs-lookup"><span data-stu-id="94b0c-194">0x800A0EA5</span></span></p></td>
<td><p><span data-ttu-id="94b0c-p106">Feldaktualisierung schlug fehl. Überprüfen Sie die <strong>Status</strong>-Eigenschaft der einzelnen Feldobjekte, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="94b0c-p106">Fields update failed. For further information, examine the <strong>Status</strong> property of individual field objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-197"><strong>adErrIllegalOperation</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-197"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-198">3219</span><span class="sxs-lookup"><span data-stu-id="94b0c-198">3219</span></span><br />
<span data-ttu-id="94b0c-199">-2146825069</span><span class="sxs-lookup"><span data-stu-id="94b0c-199">-2146825069</span></span><br />
<span data-ttu-id="94b0c-200">0x800A0C93</span><span class="sxs-lookup"><span data-stu-id="94b0c-200">0x800A0C93</span></span></p></td>
<td><p><span data-ttu-id="94b0c-201">Der Vorgang ist in diesem Zusammenhang nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="94b0c-201">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-202"><strong>adErrIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-202"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-203">3719</span><span class="sxs-lookup"><span data-stu-id="94b0c-203">3719</span></span><br />
<span data-ttu-id="94b0c-204">-2146824569</span><span class="sxs-lookup"><span data-stu-id="94b0c-204">-2146824569</span></span><br />
<span data-ttu-id="94b0c-205">0x800A0E87</span><span class="sxs-lookup"><span data-stu-id="94b0c-205">0x800A0E87</span></span></p></td>
<td><p><span data-ttu-id="94b0c-206">Der Datenwert steht in Konflikt mit den Integritätseinschränkungen des Felds.</span><span class="sxs-lookup"><span data-stu-id="94b0c-206">Data value conflicts with the integrity constraints of the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-207"><strong>adErrInTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-207"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-208">3246</span><span class="sxs-lookup"><span data-stu-id="94b0c-208">3246</span></span><br />
<span data-ttu-id="94b0c-209">-2146825042</span><span class="sxs-lookup"><span data-stu-id="94b0c-209">-2146825042</span></span><br />
<span data-ttu-id="94b0c-210">0x800A0CAE</span><span class="sxs-lookup"><span data-stu-id="94b0c-210">0x800A0CAE</span></span></p></td>
<td><p><span data-ttu-id="94b0c-211">Das <strong>Connection</strong> -Objekt kann während einer Transaktion nicht explizit geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="94b0c-211"><strong>Connection</strong> object cannot be explicitly closed while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-212"><strong>adErrInvalidArgument</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-212"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-213">3001</span><span class="sxs-lookup"><span data-stu-id="94b0c-213">3001</span></span><br />
<span data-ttu-id="94b0c-214">-2146825287</span><span class="sxs-lookup"><span data-stu-id="94b0c-214">-2146825287</span></span><br />
<span data-ttu-id="94b0c-215">0x800A0BB9</span><span class="sxs-lookup"><span data-stu-id="94b0c-215">0x800A0BB9</span></span></p></td>
<td><p><span data-ttu-id="94b0c-216">Argumente weisen den falschen Typ auf, liegen außerhalb des gültigen Bereichs oder stehen miteinander in Konflikt.</span><span class="sxs-lookup"><span data-stu-id="94b0c-216">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-217"><strong>adErrInvalidConnection</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-217"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-218">3709</span><span class="sxs-lookup"><span data-stu-id="94b0c-218">3709</span></span><br />
<span data-ttu-id="94b0c-219">-2146824579</span><span class="sxs-lookup"><span data-stu-id="94b0c-219">-2146824579</span></span><br />
<span data-ttu-id="94b0c-220">0x800A0E7D</span><span class="sxs-lookup"><span data-stu-id="94b0c-220">0x800A0E7D</span></span></p></td>
<td><p><span data-ttu-id="94b0c-p107">Die Verbindung kann nicht für diesen Vorgang verwendet werden. Die Verbindung ist entweder geschlossen oder in diesem Kontext ungültig.</span><span class="sxs-lookup"><span data-stu-id="94b0c-p107">The connection cannot be used to perform this operation. It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-223"><strong>adErrInvalidParamInfo</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-223"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-224">3708</span><span class="sxs-lookup"><span data-stu-id="94b0c-224">3708</span></span><br />
<span data-ttu-id="94b0c-225">-2146824580</span><span class="sxs-lookup"><span data-stu-id="94b0c-225">-2146824580</span></span><br />
<span data-ttu-id="94b0c-226">0x800A0E7C</span><span class="sxs-lookup"><span data-stu-id="94b0c-226">0x800A0E7C</span></span></p></td>
<td><p><span data-ttu-id="94b0c-p108">Das <strong>Parameter</strong> -Objekt ist nicht ordnungsgemäß definiert. Inkonsistente oder unvollständige Informationen wurden eingegeben.  </span><span class="sxs-lookup"><span data-stu-id="94b0c-p108"><strong>Parameter</strong> object is improperly defined. Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-229"><strong>adErrInvalidTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-229"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-230">3714</span><span class="sxs-lookup"><span data-stu-id="94b0c-230">3714</span></span><br />
<span data-ttu-id="94b0c-231">-2146824574</span><span class="sxs-lookup"><span data-stu-id="94b0c-231">-2146824574</span></span><br />
<span data-ttu-id="94b0c-232">0x800A0E82</span><span class="sxs-lookup"><span data-stu-id="94b0c-232">0x800A0E82</span></span></p></td>
<td><p><span data-ttu-id="94b0c-233">Die Koordinierungstransaktion ist ungültig oder wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="94b0c-233">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-234"><strong>adErrInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-234"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-235">3729</span><span class="sxs-lookup"><span data-stu-id="94b0c-235">3729</span></span><br />
<span data-ttu-id="94b0c-236">-2146824559</span><span class="sxs-lookup"><span data-stu-id="94b0c-236">-2146824559</span></span><br />
<span data-ttu-id="94b0c-237">0x800A0E91</span><span class="sxs-lookup"><span data-stu-id="94b0c-237">0x800A0E91</span></span></p></td>
<td><p><span data-ttu-id="94b0c-p109">URL enthält ungültige Zeichen. Stellen Sie sicher, dass die URL fehlerfrei eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="94b0c-p109">URL contains invalid characters. Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-240"><strong>adErrItemNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-240"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-241">3265</span><span class="sxs-lookup"><span data-stu-id="94b0c-241">3265</span></span><br />
<span data-ttu-id="94b0c-242">-2146825023</span><span class="sxs-lookup"><span data-stu-id="94b0c-242">-2146825023</span></span><br />
<span data-ttu-id="94b0c-243">0x800A0CC1</span><span class="sxs-lookup"><span data-stu-id="94b0c-243">0x800A0CC1</span></span></p></td>
<td><p><span data-ttu-id="94b0c-244">Das Element, das dem angeforderten Namen oder der angeforderten Zahl entspricht, wurde in der Auflistung nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="94b0c-244">Item cannot be found in the collection corresponding to the requested name or ordinal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-245"><strong>adErrNoCurrentRecord</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-245"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-246">3021</span><span class="sxs-lookup"><span data-stu-id="94b0c-246">3021</span></span><br />
<span data-ttu-id="94b0c-247">-2146825267</span><span class="sxs-lookup"><span data-stu-id="94b0c-247">-2146825267</span></span><br />
<span data-ttu-id="94b0c-248">0x800A0BCD</span><span class="sxs-lookup"><span data-stu-id="94b0c-248">0x800A0BCD</span></span></p></td>
<td><p><span data-ttu-id="94b0c-p110"><strong>BOF</strong> oder <strong>EOF</strong> ist Wahr bzw. der aktuelle Datensatz wurde gelöscht. Für den angeforderten Vorgang ist ein aktueller Datensatz erforderlich.</span><span class="sxs-lookup"><span data-stu-id="94b0c-p110">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted. Requested operation requires a current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-251"><strong>adErrNotExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-251"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-252">3715</span><span class="sxs-lookup"><span data-stu-id="94b0c-252">3715</span></span><br />
<span data-ttu-id="94b0c-253">-2146824573</span><span class="sxs-lookup"><span data-stu-id="94b0c-253">-2146824573</span></span><br />
<span data-ttu-id="94b0c-254">0x800A0E83</span><span class="sxs-lookup"><span data-stu-id="94b0c-254">0x800A0E83</span></span></p></td>
<td><p><span data-ttu-id="94b0c-255">Der Vorgang kann nicht verarbeitet werden, wenn er nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94b0c-255">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-256"><strong>adErrNotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-256"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-257">3710</span><span class="sxs-lookup"><span data-stu-id="94b0c-257">3710</span></span><br />
<span data-ttu-id="94b0c-258">-2146824578</span><span class="sxs-lookup"><span data-stu-id="94b0c-258">-2146824578</span></span><br />
<span data-ttu-id="94b0c-259">0x800A0E7E</span><span class="sxs-lookup"><span data-stu-id="94b0c-259">0x800A0E7E</span></span></p></td>
<td><p><span data-ttu-id="94b0c-260">Der Vorgang kann während der Verarbeitung des Ereignisses nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="94b0c-260">Operation cannot be performed while processing event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-261"><strong>adErrObjectClosed</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-261"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-262">3704</span><span class="sxs-lookup"><span data-stu-id="94b0c-262">3704</span></span><br />
<span data-ttu-id="94b0c-263">-2146824584</span><span class="sxs-lookup"><span data-stu-id="94b0c-263">-2146824584</span></span><br />
<span data-ttu-id="94b0c-264">0x800A0E78</span><span class="sxs-lookup"><span data-stu-id="94b0c-264">0x800A0E78</span></span></p></td>
<td><p><span data-ttu-id="94b0c-265">Der Vorgang ist nicht zulässig, wenn das Objekt geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="94b0c-265">Operation is not allowed when the object is closed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-266"><strong>adErrObjectInCollection</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-266"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-267">3367</span><span class="sxs-lookup"><span data-stu-id="94b0c-267">3367</span></span><br />
<span data-ttu-id="94b0c-268">-2146824921</span><span class="sxs-lookup"><span data-stu-id="94b0c-268">-2146824921</span></span><br />
<span data-ttu-id="94b0c-269">0x800A0D27</span><span class="sxs-lookup"><span data-stu-id="94b0c-269">0x800A0D27</span></span></p></td>
<td><p><span data-ttu-id="94b0c-p111">Objekt befindet sich bereits in der Auflistung. Anfügen nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="94b0c-p111">Object is already in collection. Cannot append.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-272"><strong>adErrObjectNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-272"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-273">3420</span><span class="sxs-lookup"><span data-stu-id="94b0c-273">3420</span></span><br />
<span data-ttu-id="94b0c-274">-2146824868</span><span class="sxs-lookup"><span data-stu-id="94b0c-274">-2146824868</span></span><br />
<span data-ttu-id="94b0c-275">0x800A0D5C</span><span class="sxs-lookup"><span data-stu-id="94b0c-275">0x800A0D5C</span></span></p></td>
<td><p><span data-ttu-id="94b0c-276">Das Objekt ist nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="94b0c-276">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-277"><strong>adErrObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-277"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-278">3705</span><span class="sxs-lookup"><span data-stu-id="94b0c-278">3705</span></span><br />
<span data-ttu-id="94b0c-279">-2146824583</span><span class="sxs-lookup"><span data-stu-id="94b0c-279">-2146824583</span></span><br />
<span data-ttu-id="94b0c-280">0x800A0E79</span><span class="sxs-lookup"><span data-stu-id="94b0c-280">0x800A0E79</span></span></p></td>
<td><p><span data-ttu-id="94b0c-281">Der Vorgang ist nicht zulässig, wenn das Objekt geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="94b0c-281">Operation is not allowed when the object is open.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-282"><strong>adErrOpeningFile</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-282"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-283">3002</span><span class="sxs-lookup"><span data-stu-id="94b0c-283">3002</span></span><br />
<span data-ttu-id="94b0c-284">-2146825286</span><span class="sxs-lookup"><span data-stu-id="94b0c-284">-2146825286</span></span><br />
<span data-ttu-id="94b0c-285">0x800A0BBA</span><span class="sxs-lookup"><span data-stu-id="94b0c-285">0x800A0BBA</span></span></p></td>
<td><p><span data-ttu-id="94b0c-286">Die Datei konnte nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="94b0c-286">File could not be opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-287"><strong>adErrOperationCancelled</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-287"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-288">3712</span><span class="sxs-lookup"><span data-stu-id="94b0c-288">3712</span></span><br />
<span data-ttu-id="94b0c-289">-2146824576</span><span class="sxs-lookup"><span data-stu-id="94b0c-289">-2146824576</span></span><br />
<span data-ttu-id="94b0c-290">0x800A0E80</span><span class="sxs-lookup"><span data-stu-id="94b0c-290">0x800A0E80</span></span></p></td>
<td><p><span data-ttu-id="94b0c-291">Vorgang wurde vom Benutzer abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="94b0c-291">Operation has been cancelled by the user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-292"><strong>adErrOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-292"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-293">3734</span><span class="sxs-lookup"><span data-stu-id="94b0c-293">3734</span></span><br />
<span data-ttu-id="94b0c-294">-2146824554</span><span class="sxs-lookup"><span data-stu-id="94b0c-294">-2146824554</span></span><br />
<span data-ttu-id="94b0c-295">0x800A0E96</span><span class="sxs-lookup"><span data-stu-id="94b0c-295">0x800A0E96</span></span></p></td>
<td><p><span data-ttu-id="94b0c-p112">Vorgang kann nicht ausgeführt werden. Anbieter kann nicht genügend Speicherplatz abrufen.</span><span class="sxs-lookup"><span data-stu-id="94b0c-p112">Operation cannot be performed. Provider cannot obtain enough storage space.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-298"><strong>adErrPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-298"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-299">3720</span><span class="sxs-lookup"><span data-stu-id="94b0c-299">3720</span></span><br />
<span data-ttu-id="94b0c-300">-2146824568</span><span class="sxs-lookup"><span data-stu-id="94b0c-300">-2146824568</span></span><br />
<span data-ttu-id="94b0c-301">0x800A0E88</span><span class="sxs-lookup"><span data-stu-id="94b0c-301">0x800A0E88</span></span></p></td>
<td><p><span data-ttu-id="94b0c-302">Unzureichende Berechtigung verhindert Schreiben im Feld.</span><span class="sxs-lookup"><span data-stu-id="94b0c-302">Insufficent permission prevents writing to the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-303"><strong>adErrProviderFailed</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-303"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-304">3000</span><span class="sxs-lookup"><span data-stu-id="94b0c-304">3000</span></span><br />
<span data-ttu-id="94b0c-305">-2146825288</span><span class="sxs-lookup"><span data-stu-id="94b0c-305">-2146825288</span></span><br />
<span data-ttu-id="94b0c-306">0x800A0BB8</span><span class="sxs-lookup"><span data-stu-id="94b0c-306">0x800A0BB8</span></span></p></td>
<td><p><span data-ttu-id="94b0c-307">Der Anbieter konnte den angeforderten Vorgang nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="94b0c-307">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-308"><strong>adErrProviderNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-308"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-309">3706</span><span class="sxs-lookup"><span data-stu-id="94b0c-309">3706</span></span><br />
<span data-ttu-id="94b0c-310">-2146824582</span><span class="sxs-lookup"><span data-stu-id="94b0c-310">-2146824582</span></span><br />
<span data-ttu-id="94b0c-311">0x800A0E7A</span><span class="sxs-lookup"><span data-stu-id="94b0c-311">0x800A0E7A</span></span></p></td>
<td><p><span data-ttu-id="94b0c-p113">Anbieter kann nicht gefunden werden. Er ist möglicherweise nicht ordnungsgemäß installiert.</span><span class="sxs-lookup"><span data-stu-id="94b0c-p113">Provider cannot be found. It may not be properly installed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-314"><strong>adErrReadFile</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-314"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-315">3003</span><span class="sxs-lookup"><span data-stu-id="94b0c-315">3003</span></span><br />
<span data-ttu-id="94b0c-316">-2146825285</span><span class="sxs-lookup"><span data-stu-id="94b0c-316">-2146825285</span></span><br />
<span data-ttu-id="94b0c-317">0x800A0BBB</span><span class="sxs-lookup"><span data-stu-id="94b0c-317">0x800A0BBB</span></span></p></td>
<td><p><span data-ttu-id="94b0c-318">Die Datei konnte nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="94b0c-318">File could not be read.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-319"><strong>adErrResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-319"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-320">3731</span><span class="sxs-lookup"><span data-stu-id="94b0c-320">3731</span></span><br />
<span data-ttu-id="94b0c-321">-2146824557</span><span class="sxs-lookup"><span data-stu-id="94b0c-321">-2146824557</span></span><br />
<span data-ttu-id="94b0c-322">0x800A0E93</span><span class="sxs-lookup"><span data-stu-id="94b0c-322">0x800A0E93</span></span></p></td>
<td><p><span data-ttu-id="94b0c-p114">Kopiervorgang kann nicht ausgeführt werden. Von Ziel-URL benanntes Objekt ist bereits vorhanden. Geben Sie <strong>AdCopyOverwrite</strong> an, um das Objekt zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="94b0c-p114">Copy operation cannot be performed. Object named by destination URL already exists. Specify <strong>adCopyOverwrite</strong> to replace the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-326"><strong>adErrResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-326"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-327">3730</span><span class="sxs-lookup"><span data-stu-id="94b0c-327">3730</span></span><br />
<span data-ttu-id="94b0c-328">-2146824558</span><span class="sxs-lookup"><span data-stu-id="94b0c-328">-2146824558</span></span><br />
<span data-ttu-id="94b0c-329">0x800A0E92</span><span class="sxs-lookup"><span data-stu-id="94b0c-329">0x800A0E92</span></span></p></td>
<td><p><span data-ttu-id="94b0c-p115">Objekt, das von der angegebenen URL dargestellt wird, wurde von mindestens einem Prozess gesperrt. Warten Sie, bis der Prozess abgeschlossen ist, und versuchen Sie dann, den Vorgang erneut auszuführen.</span><span class="sxs-lookup"><span data-stu-id="94b0c-p115">Object represented by the specified URL is locked by one or more other processes. Wait until the process has finished and attempt the operation again.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-332"><strong>adErrResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-332"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-333">3735</span><span class="sxs-lookup"><span data-stu-id="94b0c-333">3735</span></span><br />
<span data-ttu-id="94b0c-334">-2146824553</span><span class="sxs-lookup"><span data-stu-id="94b0c-334">-2146824553</span></span><br />
<span data-ttu-id="94b0c-335">0x800A0E97</span><span class="sxs-lookup"><span data-stu-id="94b0c-335">0x800A0E97</span></span></p></td>
<td><p><span data-ttu-id="94b0c-336">Die Quell- oder Ziel-URL liegt außerhalb des Bereichs des aktuellen Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="94b0c-336">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-337"><strong>adErrSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-337"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-338">3722</span><span class="sxs-lookup"><span data-stu-id="94b0c-338">3722</span></span><br />
<span data-ttu-id="94b0c-339">-2146824566</span><span class="sxs-lookup"><span data-stu-id="94b0c-339">-2146824566</span></span><br />
<span data-ttu-id="94b0c-340">0x800A0E8A</span><span class="sxs-lookup"><span data-stu-id="94b0c-340">0x800A0E8A</span></span></p></td>
<td><p><span data-ttu-id="94b0c-341">Der Datenwert steht in Konflikt mit dem Datentyp oder mit Einschränkungen des Felds.</span><span class="sxs-lookup"><span data-stu-id="94b0c-341">Data value conflicts with the data type or constraints of the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-342"><strong>adErrSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-342"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-343">3723</span><span class="sxs-lookup"><span data-stu-id="94b0c-343">3723</span></span><br />
<span data-ttu-id="94b0c-344">-2146824565</span><span class="sxs-lookup"><span data-stu-id="94b0c-344">-2146824565</span></span><br />
<span data-ttu-id="94b0c-345">0x800A0E8B</span><span class="sxs-lookup"><span data-stu-id="94b0c-345">0x800A0E8B</span></span></p></td>
<td><p><span data-ttu-id="94b0c-346">Fehler bei der Konvertierung, da der Datenwert ein Vorzeichen hat, der vom Anbieter verwendete Felddatentyp aber kein Vorzeichen aufweist.</span><span class="sxs-lookup"><span data-stu-id="94b0c-346">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-347"><strong>adErrStillConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-347"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-348">3713</span><span class="sxs-lookup"><span data-stu-id="94b0c-348">3713</span></span><br />
<span data-ttu-id="94b0c-349">-2146824575</span><span class="sxs-lookup"><span data-stu-id="94b0c-349">-2146824575</span></span><br />
<span data-ttu-id="94b0c-350">0x800A0E81</span><span class="sxs-lookup"><span data-stu-id="94b0c-350">0x800A0E81</span></span></p></td>
<td><p><span data-ttu-id="94b0c-351">Vorgang kann beim asynchronen Verbinden nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="94b0c-351">Operation cannot be performed while connecting aynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-352"><strong>adErrStillExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-352"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-353">3711</span><span class="sxs-lookup"><span data-stu-id="94b0c-353">3711</span></span><br />
<span data-ttu-id="94b0c-354">-2146824577</span><span class="sxs-lookup"><span data-stu-id="94b0c-354">-2146824577</span></span><br />
<span data-ttu-id="94b0c-355">0x800A0E7F</span><span class="sxs-lookup"><span data-stu-id="94b0c-355">0x800A0E7F</span></span></p></td>
<td><p><span data-ttu-id="94b0c-356">Der Vorgang kann im asynchronen Modus nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="94b0c-356">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-357"><strong>adErrTreePermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-357"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-358">3728</span><span class="sxs-lookup"><span data-stu-id="94b0c-358">3728</span></span><br />
<span data-ttu-id="94b0c-359">-2146824560</span><span class="sxs-lookup"><span data-stu-id="94b0c-359">-2146824560</span></span><br />
<span data-ttu-id="94b0c-360">0x800A0E90</span><span class="sxs-lookup"><span data-stu-id="94b0c-360">0x800A0E90</span></span></p></td>
<td><p><span data-ttu-id="94b0c-361">Unzureichende Berechtigungen für den Zugriff auf die Struktur oder die Unterstruktur.</span><span class="sxs-lookup"><span data-stu-id="94b0c-361">Permissions are insufficient to access tree or subtree.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-362"><strong>adErrUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-362"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-363">3736</span><span class="sxs-lookup"><span data-stu-id="94b0c-363">3736</span></span><br />
<span data-ttu-id="94b0c-364">-2146824552</span><span class="sxs-lookup"><span data-stu-id="94b0c-364">-2146824552</span></span><br />
<span data-ttu-id="94b0c-365">0x800A0E98</span><span class="sxs-lookup"><span data-stu-id="94b0c-365">0x800A0E98</span></span></p></td>
<td><p><span data-ttu-id="94b0c-p116">Vorgang konnte nicht abgeschlossen werden und der Status ist nicht verfügbar. Das Feld ist möglicherweise nicht verfügbar oder der Vorgang wurde nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94b0c-p116">Operation failed to complete and the status is unavailable. The field may be unavailable or the operation was not attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-368"><strong>adErrUnsafeOperation</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-368"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-369">3716</span><span class="sxs-lookup"><span data-stu-id="94b0c-369">3716</span></span><br />
<span data-ttu-id="94b0c-370">-2146824572</span><span class="sxs-lookup"><span data-stu-id="94b0c-370">-2146824572</span></span><br />
<span data-ttu-id="94b0c-371">0x800A0E84</span><span class="sxs-lookup"><span data-stu-id="94b0c-371">0x800A0E84</span></span></p></td>
<td><p><span data-ttu-id="94b0c-372">Die Sicherheitseinstellungen dieses Computers lassen den Zugriff auf eine Datenquelle in einer anderen Domäne nicht zu.</span><span class="sxs-lookup"><span data-stu-id="94b0c-372">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-373"><strong>adErrURLDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-373"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-374">3727</span><span class="sxs-lookup"><span data-stu-id="94b0c-374">3727</span></span><br />
<span data-ttu-id="94b0c-375">-2146824561</span><span class="sxs-lookup"><span data-stu-id="94b0c-375">-2146824561</span></span><br />
<span data-ttu-id="94b0c-376">0x800A0E8F</span><span class="sxs-lookup"><span data-stu-id="94b0c-376">0x800A0E8F</span></span></p></td>
<td><p><span data-ttu-id="94b0c-377">Entweder die Quell-URL oder das übergeordnete Element der Ziel-URL ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="94b0c-377">Either the source URL or the parent of the destination URL does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-378"><strong>adErrURLNamedRowDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-378"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-379">3737</span><span class="sxs-lookup"><span data-stu-id="94b0c-379">3737</span></span><br />
<span data-ttu-id="94b0c-380">-2146824551</span><span class="sxs-lookup"><span data-stu-id="94b0c-380">-2146824551</span></span><br />
<span data-ttu-id="94b0c-381">0x800A0E99</span><span class="sxs-lookup"><span data-stu-id="94b0c-381">0x800A0E99</span></span></p></td>
<td><p><span data-ttu-id="94b0c-382">Der von dieser URL genannte Datensatz ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="94b0c-382">Record named by this URL does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-383"><strong>adErrVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-383"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-384">3733</span><span class="sxs-lookup"><span data-stu-id="94b0c-384">3733</span></span><br />
<span data-ttu-id="94b0c-385">-2146824555</span><span class="sxs-lookup"><span data-stu-id="94b0c-385">-2146824555</span></span><br />
<span data-ttu-id="94b0c-386">0x800A0E95</span><span class="sxs-lookup"><span data-stu-id="94b0c-386">0x800A0E95</span></span></p></td>
<td><p><span data-ttu-id="94b0c-p117">Anbieter findet das von der URL angegebene Speichergerät nicht. Stellen Sie sicher, dass die URL in der richtigen Schreibweise eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="94b0c-p117">Provider cannot locate the storage device indicated by the URL. Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-389"><strong>adErrWriteFile</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-389"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-390">3004</span><span class="sxs-lookup"><span data-stu-id="94b0c-390">3004</span></span><br />
<span data-ttu-id="94b0c-391">-2146825284</span><span class="sxs-lookup"><span data-stu-id="94b0c-391">-2146825284</span></span><br />
<span data-ttu-id="94b0c-392">0x800A0BBC</span><span class="sxs-lookup"><span data-stu-id="94b0c-392">0x800A0BBC</span></span></p></td>
<td><p><span data-ttu-id="94b0c-393">Fehler beim Schreiben in die Datei.</span><span class="sxs-lookup"><span data-stu-id="94b0c-393">Write to file failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-394"><strong>adWrnSecurityDialog</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-394"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-395">3717</span><span class="sxs-lookup"><span data-stu-id="94b0c-395">3717</span></span><br />
<span data-ttu-id="94b0c-396">-2146824571</span><span class="sxs-lookup"><span data-stu-id="94b0c-396">-2146824571</span></span><br />
<span data-ttu-id="94b0c-397">0x800A0E85</span><span class="sxs-lookup"><span data-stu-id="94b0c-397">0x800A0E85</span></span></p></td>
<td><p><span data-ttu-id="94b0c-p118">Nur für die interne Verwendung. Verwendung wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="94b0c-p118">For internal use only. Don't use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-400"><strong>adWrnSecurityDialogHeader</strong></span><span class="sxs-lookup"><span data-stu-id="94b0c-400"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="94b0c-401">3718</span><span class="sxs-lookup"><span data-stu-id="94b0c-401">3718</span></span><br />
<span data-ttu-id="94b0c-402">-2146824570</span><span class="sxs-lookup"><span data-stu-id="94b0c-402">-2146824570</span></span><br />
<span data-ttu-id="94b0c-403">0x800A0E86</span><span class="sxs-lookup"><span data-stu-id="94b0c-403">0x800A0E86</span></span></p></td>
<td><p><span data-ttu-id="94b0c-p119">Nur für die interne Verwendung. Verwendung wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="94b0c-p119">For internal use only. Don't use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="94b0c-406">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="94b0c-406">ADO/WFC equivalent</span></span>

<span data-ttu-id="94b0c-407">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="94b0c-407">Package: **com.ms.wfc.data**</span></span>

<span data-ttu-id="94b0c-408">Nur die folgenden Teilmengen von ADO/WFC-Entsprechungen sind definiert.</span><span class="sxs-lookup"><span data-stu-id="94b0c-408">Only the following subsets of ADO/WFC equivalents are defined.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="94b0c-409">Konstante</span><span class="sxs-lookup"><span data-stu-id="94b0c-409">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-410">AdoEnums.ErrorValue.BOUNDTOCOMMAND</span><span class="sxs-lookup"><span data-stu-id="94b0c-410">AdoEnums.ErrorValue.BOUNDTOCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-411">AdoEnums.ErrorValue.DATACONVERSION</span><span class="sxs-lookup"><span data-stu-id="94b0c-411">AdoEnums.ErrorValue.DATACONVERSION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-412">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="94b0c-412">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-413">AdoEnums.ErrorValue.ILLEGALOPERATION</span><span class="sxs-lookup"><span data-stu-id="94b0c-413">AdoEnums.ErrorValue.ILLEGALOPERATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-414">AdoEnums.ErrorValue.INTRANSACTION</span><span class="sxs-lookup"><span data-stu-id="94b0c-414">AdoEnums.ErrorValue.INTRANSACTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-415">AdoEnums.ErrorValue.INVALIDARGUMENT</span><span class="sxs-lookup"><span data-stu-id="94b0c-415">AdoEnums.ErrorValue.INVALIDARGUMENT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-416">AdoEnums.ErrorValue.INVALIDCONNECTION</span><span class="sxs-lookup"><span data-stu-id="94b0c-416">AdoEnums.ErrorValue.INVALIDCONNECTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-417">AdoEnums.ErrorValue.INVALIDPARAMINFO</span><span class="sxs-lookup"><span data-stu-id="94b0c-417">AdoEnums.ErrorValue.INVALIDPARAMINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-418">AdoEnums.ErrorValue.ITEMNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="94b0c-418">AdoEnums.ErrorValue.ITEMNOTFOUND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-419">AdoEnums.ErrorValue.NOCURRENTRECORD</span><span class="sxs-lookup"><span data-stu-id="94b0c-419">AdoEnums.ErrorValue.NOCURRENTRECORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-420">AdoEnums.ErrorValue.NOTEXECUTING</span><span class="sxs-lookup"><span data-stu-id="94b0c-420">AdoEnums.ErrorValue.NOTEXECUTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-421">AdoEnums.ErrorValue.NOTREENTRANT</span><span class="sxs-lookup"><span data-stu-id="94b0c-421">AdoEnums.ErrorValue.NOTREENTRANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-422">AdoEnums.ErrorValue.OBJECTCLOSED</span><span class="sxs-lookup"><span data-stu-id="94b0c-422">AdoEnums.ErrorValue.OBJECTCLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-423">AdoEnums.ErrorValue.OBJECTINCOLLECTION</span><span class="sxs-lookup"><span data-stu-id="94b0c-423">AdoEnums.ErrorValue.OBJECTINCOLLECTION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-424">AdoEnums.ErrorValue.OBJECTNOTSET</span><span class="sxs-lookup"><span data-stu-id="94b0c-424">AdoEnums.ErrorValue.OBJECTNOTSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-425">AdoEnums.ErrorValue.OBJECTOPEN</span><span class="sxs-lookup"><span data-stu-id="94b0c-425">AdoEnums.ErrorValue.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-426">AdoEnums.ErrorValue.OPERATIONCANCELLED</span><span class="sxs-lookup"><span data-stu-id="94b0c-426">AdoEnums.ErrorValue.OPERATIONCANCELLED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-427">AdoEnums.ErrorValue.PROVIDERNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="94b0c-427">AdoEnums.ErrorValue.PROVIDERNOTFOUND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-428">AdoEnums.ErrorValue.STILLCONNECTING</span><span class="sxs-lookup"><span data-stu-id="94b0c-428">AdoEnums.ErrorValue.STILLCONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b0c-429">AdoEnums.ErrorValue.STILLEXECUTING</span><span class="sxs-lookup"><span data-stu-id="94b0c-429">AdoEnums.ErrorValue.STILLEXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b0c-430">AdoEnums.ErrorValue.UNSAFEOPERATION</span><span class="sxs-lookup"><span data-stu-id="94b0c-430">AdoEnums.ErrorValue.UNSAFEOPERATION</span></span></p></td>
</tr>
</tbody>
</table>

