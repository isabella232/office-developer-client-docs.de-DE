---
title: ErrorValueEnum (Access Desktop Database Reference)
TOCTitle: ErrorValueEnum
ms:assetid: 2af99f32-6004-1225-367c-45d693f447b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249058(v=office.15)
ms:contentKeyID: 48543921
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c2d4207f157d361f3b8aba2ff80f46d06b2f328e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293322"
---
# <a name="errorvalueenum"></a><span data-ttu-id="ec7c8-102">ErrorValueEnum</span><span class="sxs-lookup"><span data-stu-id="ec7c8-102">ErrorValueEnum</span></span>

<span data-ttu-id="ec7c8-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec7c8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ec7c8-104">Gibt den Typ des ADO-Laufzeitfehlers an.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-104">Specifies the type of ADO run-time error.</span></span>

<span data-ttu-id="ec7c8-105">Es werden drei Fehlernummerntypen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="ec7c8-105">Three forms of the error number are listed:</span></span>

- <span data-ttu-id="ec7c8-p101">Positive Dezimalzahl - die niedrigen zwei Bytes der vollständigen Zahl im Dezimalstellenformat. Diese Nummer wird im Standard-Fehlermeldungsdialogfeld von Visual Basic angezeigt. Zum Beispiel Laufzeitfehler "3707".</span><span class="sxs-lookup"><span data-stu-id="ec7c8-p101">Positive decimal — the low two bytes of the full number in decimal format. This number is displayed in the default Visual Basic error message dialog box. For example, Run-time error '3707'.</span></span>

- <span data-ttu-id="ec7c8-109">Negative Dezimalzahl - die Dezimalübersetzung der vollständigen Fehlernummer.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-109">Negative decimal — The decimal translation of the full error number.</span></span>

- <span data-ttu-id="ec7c8-110">Hexadezimal - die hexadezimale Darstellung der vollständigen Fehlernummer.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-110">Hexadecimal — The hexadecimal representation of the full error number.</span></span> <span data-ttu-id="ec7c8-111">Der Windows-Einrichtungscode befindet sich in der vierten Ziffer.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-111">The Windows facility code is in the fourth digit.</span></span> <span data-ttu-id="ec7c8-112">Der Ortscode für ADO-Fehlernummern ist *A*. Beispiel: 0x800***ein***0E7B.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-112">The facility code for ADO error numbers is *A*. For example: 0x800***A***0E7B.</span></span>

> [!NOTE]
> <span data-ttu-id="ec7c8-113">OLE DB-Fehler können an Ihre ADO-Anwendung übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-113">OLE DB errors may be passed to your ADO application.</span></span> <span data-ttu-id="ec7c8-114">Diese können in der Regel von einem Windows-Einrichtungscode von *4* identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-114">Typically, these can be identified by a Windows facility code of *4*.</span></span> <span data-ttu-id="ec7c8-115">Beispiel: 0x800_**4**_.... Weitere Informationen zu diesen Nummern finden Sie in Kapitel 16 der *OLE DB Programmer es Reference.*</span><span class="sxs-lookup"><span data-stu-id="ec7c8-115">For example, 0x800_**4**_.... For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ec7c8-116">Konstante</span><span class="sxs-lookup"><span data-stu-id="ec7c8-116">Constant</span></span></p></th>
<th><p><span data-ttu-id="ec7c8-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ec7c8-117">Value</span></span></p></th>
<th><p><span data-ttu-id="ec7c8-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec7c8-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-119"><strong>adErrBoundToCommand</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-119"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-120">3707</span><span class="sxs-lookup"><span data-stu-id="ec7c8-120">3707</span></span><br />
<span data-ttu-id="ec7c8-121">-2146824581</span><span class="sxs-lookup"><span data-stu-id="ec7c8-121">-2146824581</span></span><br />
<span data-ttu-id="ec7c8-122">0x800A0E7B</span><span class="sxs-lookup"><span data-stu-id="ec7c8-122">0x800A0E7B</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-123">Kann die <strong>ActiveConnection</strong>-Eigenschaft eines <strong>Recordset</strong>-Objekts nicht ändern, das als Quelle ein <strong>Command</strong>-Objekt besitzt.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-123">Cannot change the <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object which has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-124"><strong>adErrCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-124"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-125">3732</span><span class="sxs-lookup"><span data-stu-id="ec7c8-125">3732</span></span><br />
<span data-ttu-id="ec7c8-126">-2146824556</span><span class="sxs-lookup"><span data-stu-id="ec7c8-126">-2146824556</span></span><br />
<span data-ttu-id="ec7c8-127">0x800A0E94</span><span class="sxs-lookup"><span data-stu-id="ec7c8-127">0x800A0E94</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-128">Server kann den Vorgang nicht abschließen.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-128">Server cannot complete the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-129"><strong>adErrCantChangeConnection</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-129"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-130">3748</span><span class="sxs-lookup"><span data-stu-id="ec7c8-130">3748</span></span><br />
<span data-ttu-id="ec7c8-131">-2146824540</span><span class="sxs-lookup"><span data-stu-id="ec7c8-131">-2146824540</span></span><br />
<span data-ttu-id="ec7c8-132">0x800A0EA4</span><span class="sxs-lookup"><span data-stu-id="ec7c8-132">0x800A0EA4</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-133">Verbindung wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-133">Connection was denied.</span></span> <span data-ttu-id="ec7c8-134">Die von Ihnen angeforderte neue Verbindung weist andere Eigenschaften als die bereits verwendete auf.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-134">New connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-135"><strong>adErrCantChangeProvider</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-135"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-136">3220</span><span class="sxs-lookup"><span data-stu-id="ec7c8-136">3220</span></span><br />
<span data-ttu-id="ec7c8-137">-2146825068</span><span class="sxs-lookup"><span data-stu-id="ec7c8-137">-2146825068</span></span><br />
<span data-ttu-id="ec7c8-138">0X800A0C94</span><span class="sxs-lookup"><span data-stu-id="ec7c8-138">0X800A0C94</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-139">Der angegebene Anbieter unterscheidet sich vom bereits verwendeten.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-139">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-140"><strong>adErrCantConvertvalue</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-140"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-141">3724</span><span class="sxs-lookup"><span data-stu-id="ec7c8-141">3724</span></span><br />
<span data-ttu-id="ec7c8-142">-2146824564</span><span class="sxs-lookup"><span data-stu-id="ec7c8-142">-2146824564</span></span><br />
<span data-ttu-id="ec7c8-143">0x800A0E8C</span><span class="sxs-lookup"><span data-stu-id="ec7c8-143">0x800A0E8C</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-144">Der Datenwert kann aus anderen Gründen als einem Vorzeichenkonflikt oder einem Datenüberlauf nicht konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-144">Data value cannot be converted for reasons other than sign mismatch or data overflow.</span></span> <span data-ttu-id="ec7c8-145">Beispielsweise hätte die Konvertierung Daten abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-145">For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-146"><strong>adErrCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-146"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-147">3725</span><span class="sxs-lookup"><span data-stu-id="ec7c8-147">3725</span></span><br />
<span data-ttu-id="ec7c8-148">-2146824563</span><span class="sxs-lookup"><span data-stu-id="ec7c8-148">-2146824563</span></span><br />
<span data-ttu-id="ec7c8-149">0x800A0E8D</span><span class="sxs-lookup"><span data-stu-id="ec7c8-149">0x800A0E8D</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-150">Datenwert kann nicht festgelegt oder abgerufen werden, da der Felddatentyp unbekannt war oder der Anbieter über unzureichende Ressourcen verfügte, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-150">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-151"><strong>adErrCatalogNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-151"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-152">3747</span><span class="sxs-lookup"><span data-stu-id="ec7c8-152">3747</span></span><br />
<span data-ttu-id="ec7c8-153">-2146824541</span><span class="sxs-lookup"><span data-stu-id="ec7c8-153">-2146824541</span></span><br />
<span data-ttu-id="ec7c8-154">0x800A0EA3</span><span class="sxs-lookup"><span data-stu-id="ec7c8-154">0x800A0EA3</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-155">Vorgang erfordert einen gültigen Wert für <strong>ParentCatalog</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-155">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-156"><strong>adErrColumnNotOnThisRow</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-156"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-157">3726</span><span class="sxs-lookup"><span data-stu-id="ec7c8-157">3726</span></span><br />
<span data-ttu-id="ec7c8-158">-2146824562</span><span class="sxs-lookup"><span data-stu-id="ec7c8-158">-2146824562</span></span><br />
<span data-ttu-id="ec7c8-159">0x800A0E8E</span><span class="sxs-lookup"><span data-stu-id="ec7c8-159">0x800A0E8E</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-160">Datensatz enthält dieses Feld nicht.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-160">Record does not contain this field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-161"><strong>adErrDataConversion</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-161"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-162">3421</span><span class="sxs-lookup"><span data-stu-id="ec7c8-162">3421</span></span><br />
<span data-ttu-id="ec7c8-163">-2146824867</span><span class="sxs-lookup"><span data-stu-id="ec7c8-163">-2146824867</span></span><br />
<span data-ttu-id="ec7c8-164">0x800A0D5D</span><span class="sxs-lookup"><span data-stu-id="ec7c8-164">0x800A0D5D</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-165">Anwendung verwendet für den aktuellen Vorgang einen Wert vom falschen Typ.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-165">Application uses a value of the wrong type for the current operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-166"><strong>adErrDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-166"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-167">3721</span><span class="sxs-lookup"><span data-stu-id="ec7c8-167">3721</span></span><br />
<span data-ttu-id="ec7c8-168">-2146824567</span><span class="sxs-lookup"><span data-stu-id="ec7c8-168">-2146824567</span></span><br />
<span data-ttu-id="ec7c8-169">0x800A0E89</span><span class="sxs-lookup"><span data-stu-id="ec7c8-169">0x800A0E89</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-170">Datenwert ist zu groß, um vom Felddatentyp dargestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-170">Data value is too large to be represented by the field data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-171"><strong>adErrDelResOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-171"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-172">3738</span><span class="sxs-lookup"><span data-stu-id="ec7c8-172">3738</span></span><br />
<span data-ttu-id="ec7c8-173">-2146824550</span><span class="sxs-lookup"><span data-stu-id="ec7c8-173">-2146824550</span></span><br />
<span data-ttu-id="ec7c8-174">0x800A0E9A</span><span class="sxs-lookup"><span data-stu-id="ec7c8-174">0x800A0E9A</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-175">URL des zu löschenden Objekts befindet sich außerhalb des aktuellen Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-175">URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-176"><strong>adErrDenyNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-176"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-177">3750</span><span class="sxs-lookup"><span data-stu-id="ec7c8-177">3750</span></span><br />
<span data-ttu-id="ec7c8-178">-2146824538</span><span class="sxs-lookup"><span data-stu-id="ec7c8-178">-2146824538</span></span><br />
<span data-ttu-id="ec7c8-179">0x800A0EA6</span><span class="sxs-lookup"><span data-stu-id="ec7c8-179">0x800A0EA6</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-180">Anbieter unterstützt keine Freigabebeschränkungen.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-180">Provider does not support sharing restrictions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-181"><strong>adErrDenyTypeNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-181"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-182">3751</span><span class="sxs-lookup"><span data-stu-id="ec7c8-182">3751</span></span><br />
<span data-ttu-id="ec7c8-183">-2146824537</span><span class="sxs-lookup"><span data-stu-id="ec7c8-183">-2146824537</span></span><br />
<span data-ttu-id="ec7c8-184">0x800A0EA7</span><span class="sxs-lookup"><span data-stu-id="ec7c8-184">0x800A0EA7</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-185">Anbieter unterstützt die angeforderte Art der Freigabebeschränkung nicht.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-185">Provider does not support the requested kind of sharing restriction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-186"><strong>adErrFeatureNotAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-186"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-187">3251</span><span class="sxs-lookup"><span data-stu-id="ec7c8-187">3251</span></span><br />
<span data-ttu-id="ec7c8-188">-2146825037</span><span class="sxs-lookup"><span data-stu-id="ec7c8-188">-2146825037</span></span><br />
<span data-ttu-id="ec7c8-189">0x800A0CB3</span><span class="sxs-lookup"><span data-stu-id="ec7c8-189">0x800A0CB3</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-190">Objekt oder Anbieter kann den angeforderten Vorgang nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-190">Object or provider is not capable of performing requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-191"><strong>adErrFieldsUpdateFailed</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-191"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-192">3749</span><span class="sxs-lookup"><span data-stu-id="ec7c8-192">3749</span></span><br />
<span data-ttu-id="ec7c8-193">-2146824539</span><span class="sxs-lookup"><span data-stu-id="ec7c8-193">-2146824539</span></span><br />
<span data-ttu-id="ec7c8-194">0x800A0EA5</span><span class="sxs-lookup"><span data-stu-id="ec7c8-194">0x800A0EA5</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-195">Fehler beim Aktualisieren von Feldern.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-195">Fields update failed.</span></span> <span data-ttu-id="ec7c8-196">Überprüfen Sie die <strong>Status</strong>-Eigenschaft der einzelnen Feldobjekte, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-196">For further information, examine the <strong>Status</strong> property of individual field objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-197"><strong>adErrIllegalOperation</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-197"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-198">3219</span><span class="sxs-lookup"><span data-stu-id="ec7c8-198">3219</span></span><br />
<span data-ttu-id="ec7c8-199">-2146825069</span><span class="sxs-lookup"><span data-stu-id="ec7c8-199">-2146825069</span></span><br />
<span data-ttu-id="ec7c8-200">0x800A0C93</span><span class="sxs-lookup"><span data-stu-id="ec7c8-200">0x800A0C93</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-201">Vorgang ist in diesem Zusammenhang unzulässig.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-201">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-202"><strong>adErrIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-202"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-203">3719</span><span class="sxs-lookup"><span data-stu-id="ec7c8-203">3719</span></span><br />
<span data-ttu-id="ec7c8-204">-2146824569</span><span class="sxs-lookup"><span data-stu-id="ec7c8-204">-2146824569</span></span><br />
<span data-ttu-id="ec7c8-205">0x800A0E87</span><span class="sxs-lookup"><span data-stu-id="ec7c8-205">0x800A0E87</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-206">Datenwert steht in Konflikt mit den Integritätseinschränkungen des Felds.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-206">Data value conflicts with the integrity constraints of the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-207"><strong>adErrInTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-207"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-208">3246</span><span class="sxs-lookup"><span data-stu-id="ec7c8-208">3246</span></span><br />
<span data-ttu-id="ec7c8-209">-2146825042</span><span class="sxs-lookup"><span data-stu-id="ec7c8-209">-2146825042</span></span><br />
<span data-ttu-id="ec7c8-210">0x800A0CAE</span><span class="sxs-lookup"><span data-stu-id="ec7c8-210">0x800A0CAE</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-211"><strong>Connection</strong>-Objekt kann nicht explizit während einer Transaktion geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-211"><strong>Connection</strong> object cannot be explicitly closed while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-212"><strong>adErrInvalidArgument</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-212"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-213">3001</span><span class="sxs-lookup"><span data-stu-id="ec7c8-213">3001</span></span><br />
<span data-ttu-id="ec7c8-214">-2146825287</span><span class="sxs-lookup"><span data-stu-id="ec7c8-214">-2146825287</span></span><br />
<span data-ttu-id="ec7c8-215">0x800A0BB9</span><span class="sxs-lookup"><span data-stu-id="ec7c8-215">0x800A0BB9</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-216">Argumente weisen den falschen Typ auf, liegen außerhalb des gültigen Bereichs oder stehen miteinander in Konflikt.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-216">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-217"><strong>adErrInvalidConnection</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-217"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-218">3709</span><span class="sxs-lookup"><span data-stu-id="ec7c8-218">3709</span></span><br />
<span data-ttu-id="ec7c8-219">-2146824579</span><span class="sxs-lookup"><span data-stu-id="ec7c8-219">-2146824579</span></span><br />
<span data-ttu-id="ec7c8-220">0x800A0E7D</span><span class="sxs-lookup"><span data-stu-id="ec7c8-220">0x800A0E7D</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-221">Die Verbindung kann nicht für diesen Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-221">The connection cannot be used to perform this operation.</span></span> <span data-ttu-id="ec7c8-222">Sie ist geschlossen oder in diesem Zusammenhang ungültig.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-222">It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-223"><strong>adErrInvalidParamInfo</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-223"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-224">3708</span><span class="sxs-lookup"><span data-stu-id="ec7c8-224">3708</span></span><br />
<span data-ttu-id="ec7c8-225">-2146824580</span><span class="sxs-lookup"><span data-stu-id="ec7c8-225">-2146824580</span></span><br />
<span data-ttu-id="ec7c8-226">0x800A0E7C</span><span class="sxs-lookup"><span data-stu-id="ec7c8-226">0x800A0E7C</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-227">Das <strong>Parameter</strong> -Objekt ist nicht ordnungsgemäß definiert.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-227"><strong>Parameter</strong> object is improperly defined.</span></span> <span data-ttu-id="ec7c8-228">Es wurden inkonsistente oder unvollständige Informationen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-228">Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-229"><strong>adErrInvalidTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-229"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-230">3714</span><span class="sxs-lookup"><span data-stu-id="ec7c8-230">3714</span></span><br />
<span data-ttu-id="ec7c8-231">-2146824574</span><span class="sxs-lookup"><span data-stu-id="ec7c8-231">-2146824574</span></span><br />
<span data-ttu-id="ec7c8-232">0x800A0E82</span><span class="sxs-lookup"><span data-stu-id="ec7c8-232">0x800A0E82</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-233">Die koordinierende Transaktion ist ungültig bzw. wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-233">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-234"><strong>adErrInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-234"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-235">3729</span><span class="sxs-lookup"><span data-stu-id="ec7c8-235">3729</span></span><br />
<span data-ttu-id="ec7c8-236">-2146824559</span><span class="sxs-lookup"><span data-stu-id="ec7c8-236">-2146824559</span></span><br />
<span data-ttu-id="ec7c8-237">0x800A0E91</span><span class="sxs-lookup"><span data-stu-id="ec7c8-237">0x800A0E91</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-238">URL enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-238">URL contains invalid characters.</span></span> <span data-ttu-id="ec7c8-239">Stellen Sie sicher, dass die URL fehlerfrei eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-239">Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-240"><strong>adErrItemNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-240"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-241">3265</span><span class="sxs-lookup"><span data-stu-id="ec7c8-241">3265</span></span><br />
<span data-ttu-id="ec7c8-242">-2146825023</span><span class="sxs-lookup"><span data-stu-id="ec7c8-242">-2146825023</span></span><br />
<span data-ttu-id="ec7c8-243">0x800A0CC1</span><span class="sxs-lookup"><span data-stu-id="ec7c8-243">0x800A0CC1</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-244">Element kann nicht in der Auflistung gefunden werden, die dem angeforderten Namen oder der angeforderten Ordnungszahl entspricht.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-244">Item cannot be found in the collection corresponding to the requested name or ordinal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-245"><strong>adErrNoCurrentRecord</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-245"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-246">3021</span><span class="sxs-lookup"><span data-stu-id="ec7c8-246">3021</span></span><br />
<span data-ttu-id="ec7c8-247">-2146825267</span><span class="sxs-lookup"><span data-stu-id="ec7c8-247">-2146825267</span></span><br />
<span data-ttu-id="ec7c8-248">0x800A0BCD</span><span class="sxs-lookup"><span data-stu-id="ec7c8-248">0x800A0BCD</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-p110"><strong>BOF</strong> oder <strong>EOF</strong> ist Wahr bzw. der aktuelle Datensatz wurde gelöscht. Für den angeforderten Vorgang ist ein aktueller Datensatz erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-p110">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted. Requested operation requires a current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-251"><strong>adErrNotExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-251"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-252">3715</span><span class="sxs-lookup"><span data-stu-id="ec7c8-252">3715</span></span><br />
<span data-ttu-id="ec7c8-253">-2146824573</span><span class="sxs-lookup"><span data-stu-id="ec7c8-253">-2146824573</span></span><br />
<span data-ttu-id="ec7c8-254">0x800A0E83</span><span class="sxs-lookup"><span data-stu-id="ec7c8-254">0x800A0E83</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-255">Vorgang kann während der Ausführung nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-255">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-256"><strong>adErrNotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-256"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-257">3710</span><span class="sxs-lookup"><span data-stu-id="ec7c8-257">3710</span></span><br />
<span data-ttu-id="ec7c8-258">-2146824578</span><span class="sxs-lookup"><span data-stu-id="ec7c8-258">-2146824578</span></span><br />
<span data-ttu-id="ec7c8-259">0x800A0E7E</span><span class="sxs-lookup"><span data-stu-id="ec7c8-259">0x800A0E7E</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-260">Vorgang kann während des Verarbeitungsereignisses nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-260">Operation cannot be performed while processing event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-261"><strong>adErrObjectClosed</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-261"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-262">3704</span><span class="sxs-lookup"><span data-stu-id="ec7c8-262">3704</span></span><br />
<span data-ttu-id="ec7c8-263">-2146824584</span><span class="sxs-lookup"><span data-stu-id="ec7c8-263">-2146824584</span></span><br />
<span data-ttu-id="ec7c8-264">0x800A0E78</span><span class="sxs-lookup"><span data-stu-id="ec7c8-264">0x800A0E78</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-265">Vorgang ist unzulässig, wenn das Objekt geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-265">Operation is not allowed when the object is closed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-266"><strong>adErrObjectInCollection</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-266"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-267">3367</span><span class="sxs-lookup"><span data-stu-id="ec7c8-267">3367</span></span><br />
<span data-ttu-id="ec7c8-268">-2146824921</span><span class="sxs-lookup"><span data-stu-id="ec7c8-268">-2146824921</span></span><br />
<span data-ttu-id="ec7c8-269">0x800A0D27</span><span class="sxs-lookup"><span data-stu-id="ec7c8-269">0x800A0D27</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-270">Das Objekt ist bereits in der Auflistung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-270">Object is already in collection.</span></span> <span data-ttu-id="ec7c8-271">Anfügen nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-271">Cannot append.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-272"><strong>adErrObjectNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-272"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-273">3420</span><span class="sxs-lookup"><span data-stu-id="ec7c8-273">3420</span></span><br />
<span data-ttu-id="ec7c8-274">-2146824868</span><span class="sxs-lookup"><span data-stu-id="ec7c8-274">-2146824868</span></span><br />
<span data-ttu-id="ec7c8-275">0x800A0D5C</span><span class="sxs-lookup"><span data-stu-id="ec7c8-275">0x800A0D5C</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-276">Objekt ist nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-276">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-277"><strong>adErrObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-277"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-278">3705</span><span class="sxs-lookup"><span data-stu-id="ec7c8-278">3705</span></span><br />
<span data-ttu-id="ec7c8-279">-2146824583</span><span class="sxs-lookup"><span data-stu-id="ec7c8-279">-2146824583</span></span><br />
<span data-ttu-id="ec7c8-280">0x800A0E79</span><span class="sxs-lookup"><span data-stu-id="ec7c8-280">0x800A0E79</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-281">Vorgang ist unzulässig, wenn das Objekt geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-281">Operation is not allowed when the object is open.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-282"><strong>adErrOpeningFile</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-282"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-283">3002</span><span class="sxs-lookup"><span data-stu-id="ec7c8-283">3002</span></span><br />
<span data-ttu-id="ec7c8-284">-2146825286</span><span class="sxs-lookup"><span data-stu-id="ec7c8-284">-2146825286</span></span><br />
<span data-ttu-id="ec7c8-285">0x800A0BBA</span><span class="sxs-lookup"><span data-stu-id="ec7c8-285">0x800A0BBA</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-286">Datei konnte nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-286">File could not be opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-287"><strong>adErrOperationCancelled</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-287"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-288">3712</span><span class="sxs-lookup"><span data-stu-id="ec7c8-288">3712</span></span><br />
<span data-ttu-id="ec7c8-289">-2146824576</span><span class="sxs-lookup"><span data-stu-id="ec7c8-289">-2146824576</span></span><br />
<span data-ttu-id="ec7c8-290">0x800A0E80</span><span class="sxs-lookup"><span data-stu-id="ec7c8-290">0x800A0E80</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-291">Vorgang wurde vom Benutzer abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-291">Operation has been cancelled by the user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-292"><strong>adErrOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-292"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-293">3734</span><span class="sxs-lookup"><span data-stu-id="ec7c8-293">3734</span></span><br />
<span data-ttu-id="ec7c8-294">-2146824554</span><span class="sxs-lookup"><span data-stu-id="ec7c8-294">-2146824554</span></span><br />
<span data-ttu-id="ec7c8-295">0x800A0E96</span><span class="sxs-lookup"><span data-stu-id="ec7c8-295">0x800A0E96</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-296">Der Vorgang kann nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-296">Operation cannot be performed.</span></span> <span data-ttu-id="ec7c8-297">Anbieter kann nicht genügend Speicherplatz abrufen.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-297">Provider cannot obtain enough storage space.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-298"><strong>adErrPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-298"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-299">3720</span><span class="sxs-lookup"><span data-stu-id="ec7c8-299">3720</span></span><br />
<span data-ttu-id="ec7c8-300">-2146824568</span><span class="sxs-lookup"><span data-stu-id="ec7c8-300">-2146824568</span></span><br />
<span data-ttu-id="ec7c8-301">0x800A0E88</span><span class="sxs-lookup"><span data-stu-id="ec7c8-301">0x800A0E88</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-302">Unzureichende Berechtigung verhindert Schreiben im Feld.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-302">Insufficent permission prevents writing to the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-303"><strong>adErrProviderFailed</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-303"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-304">3000</span><span class="sxs-lookup"><span data-stu-id="ec7c8-304">3000</span></span><br />
<span data-ttu-id="ec7c8-305">-2146825288</span><span class="sxs-lookup"><span data-stu-id="ec7c8-305">-2146825288</span></span><br />
<span data-ttu-id="ec7c8-306">0x800A0BB8</span><span class="sxs-lookup"><span data-stu-id="ec7c8-306">0x800A0BB8</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-307">Anbieter konnte den angeforderten Vorgang nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-307">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-308"><strong>adErrProviderNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-308"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-309">3706</span><span class="sxs-lookup"><span data-stu-id="ec7c8-309">3706</span></span><br />
<span data-ttu-id="ec7c8-310">-2146824582</span><span class="sxs-lookup"><span data-stu-id="ec7c8-310">-2146824582</span></span><br />
<span data-ttu-id="ec7c8-311">0x800A0E7A</span><span class="sxs-lookup"><span data-stu-id="ec7c8-311">0x800A0E7A</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-312">Der Anbieter wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-312">Provider cannot be found.</span></span> <span data-ttu-id="ec7c8-313">Er ist möglicherweise nicht ordnungsgemäß installiert.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-313">It may not be properly installed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-314"><strong>adErrReadFile</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-314"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-315">3003</span><span class="sxs-lookup"><span data-stu-id="ec7c8-315">3003</span></span><br />
<span data-ttu-id="ec7c8-316">-2146825285</span><span class="sxs-lookup"><span data-stu-id="ec7c8-316">-2146825285</span></span><br />
<span data-ttu-id="ec7c8-317">0x800A0BBB</span><span class="sxs-lookup"><span data-stu-id="ec7c8-317">0x800A0BBB</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-318">Datei konnte nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-318">File could not be read.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-319"><strong>adErrResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-319"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-320">3731</span><span class="sxs-lookup"><span data-stu-id="ec7c8-320">3731</span></span><br />
<span data-ttu-id="ec7c8-321">-2146824557</span><span class="sxs-lookup"><span data-stu-id="ec7c8-321">-2146824557</span></span><br />
<span data-ttu-id="ec7c8-322">0x800A0E93</span><span class="sxs-lookup"><span data-stu-id="ec7c8-322">0x800A0E93</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-323">Der Kopiervorgang kann nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-323">Copy operation cannot be performed.</span></span> <span data-ttu-id="ec7c8-324">Das durch die Ziel-URL genannte Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-324">Object named by destination URL already exists.</span></span> <span data-ttu-id="ec7c8-325">Geben Sie <strong>AdCopyOverwrite</strong> an, um das Objekt zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-325">Specify <strong>adCopyOverwrite</strong> to replace the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-326"><strong>adErrResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-326"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-327">3730</span><span class="sxs-lookup"><span data-stu-id="ec7c8-327">3730</span></span><br />
<span data-ttu-id="ec7c8-328">-2146824558</span><span class="sxs-lookup"><span data-stu-id="ec7c8-328">-2146824558</span></span><br />
<span data-ttu-id="ec7c8-329">0x800A0E92</span><span class="sxs-lookup"><span data-stu-id="ec7c8-329">0x800A0E92</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-p115">Objekt, das von der angegebenen URL dargestellt wird, wurde von mindestens einem Prozess gesperrt. Warten Sie, bis der Prozess abgeschlossen ist, und versuchen Sie dann, den Vorgang erneut auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-p115">Object represented by the specified URL is locked by one or more other processes. Wait until the process has finished and attempt the operation again.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-332"><strong>adErrResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-332"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-333">3735</span><span class="sxs-lookup"><span data-stu-id="ec7c8-333">3735</span></span><br />
<span data-ttu-id="ec7c8-334">-2146824553</span><span class="sxs-lookup"><span data-stu-id="ec7c8-334">-2146824553</span></span><br />
<span data-ttu-id="ec7c8-335">0x800A0E97</span><span class="sxs-lookup"><span data-stu-id="ec7c8-335">0x800A0E97</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-336">Quell- oder Ziel-URL befindet sich außerhalb des aktuellen Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-336">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-337"><strong>adErrSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-337"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-338">3722</span><span class="sxs-lookup"><span data-stu-id="ec7c8-338">3722</span></span><br />
<span data-ttu-id="ec7c8-339">-2146824566</span><span class="sxs-lookup"><span data-stu-id="ec7c8-339">-2146824566</span></span><br />
<span data-ttu-id="ec7c8-340">0x800A0E8A</span><span class="sxs-lookup"><span data-stu-id="ec7c8-340">0x800A0E8A</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-341">Datenwert steht in Konflikt mit dem Datentyp oder den Feldeinschränkungen.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-341">Data value conflicts with the data type or constraints of the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-342"><strong>adErrSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-342"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-343">3723</span><span class="sxs-lookup"><span data-stu-id="ec7c8-343">3723</span></span><br />
<span data-ttu-id="ec7c8-344">-2146824565</span><span class="sxs-lookup"><span data-stu-id="ec7c8-344">-2146824565</span></span><br />
<span data-ttu-id="ec7c8-345">0x800A0E8B</span><span class="sxs-lookup"><span data-stu-id="ec7c8-345">0x800A0E8B</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-346">Konvertierung schlug fehl, da der Datenwert ein Vorzeichen aufwies und der vom Anbieter verwendete Felddatentyp kein Vorzeichen aufwies.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-346">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-347"><strong>adErrStillConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-347"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-348">3713</span><span class="sxs-lookup"><span data-stu-id="ec7c8-348">3713</span></span><br />
<span data-ttu-id="ec7c8-349">-2146824575</span><span class="sxs-lookup"><span data-stu-id="ec7c8-349">-2146824575</span></span><br />
<span data-ttu-id="ec7c8-350">0x800A0E81</span><span class="sxs-lookup"><span data-stu-id="ec7c8-350">0x800A0E81</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-351">Vorgang kann beim asynchronen Verbinden nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-351">Operation cannot be performed while connecting aynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-352"><strong>adErrStillExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-352"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-353">3711</span><span class="sxs-lookup"><span data-stu-id="ec7c8-353">3711</span></span><br />
<span data-ttu-id="ec7c8-354">-2146824577</span><span class="sxs-lookup"><span data-stu-id="ec7c8-354">-2146824577</span></span><br />
<span data-ttu-id="ec7c8-355">0x800A0E7F</span><span class="sxs-lookup"><span data-stu-id="ec7c8-355">0x800A0E7F</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-356">Vorgang kann beim asynchronen Ausführen nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-356">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-357"><strong>adErrTreePermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-357"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-358">3728</span><span class="sxs-lookup"><span data-stu-id="ec7c8-358">3728</span></span><br />
<span data-ttu-id="ec7c8-359">-2146824560</span><span class="sxs-lookup"><span data-stu-id="ec7c8-359">-2146824560</span></span><br />
<span data-ttu-id="ec7c8-360">0x800A0E90</span><span class="sxs-lookup"><span data-stu-id="ec7c8-360">0x800A0E90</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-361">Die Berechtigungen sind für den Zugriff auf die Struktur oder Unterstruktur nicht ausreichend.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-361">Permissions are insufficient to access tree or subtree.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-362"><strong>adErrUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-362"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-363">3736</span><span class="sxs-lookup"><span data-stu-id="ec7c8-363">3736</span></span><br />
<span data-ttu-id="ec7c8-364">-2146824552</span><span class="sxs-lookup"><span data-stu-id="ec7c8-364">-2146824552</span></span><br />
<span data-ttu-id="ec7c8-365">0x800A0E98</span><span class="sxs-lookup"><span data-stu-id="ec7c8-365">0x800A0E98</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-366">Der Vorgang konnte nicht abgeschlossen werden, und der Status ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-366">Operation failed to complete and the status is unavailable.</span></span> <span data-ttu-id="ec7c8-367">Das Feld ist möglicherweise nicht verfügbar oder der Vorgang wurde nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-367">The field may be unavailable or the operation was not attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-368"><strong>adErrUnsafeOperation</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-368"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-369">3716</span><span class="sxs-lookup"><span data-stu-id="ec7c8-369">3716</span></span><br />
<span data-ttu-id="ec7c8-370">-2146824572</span><span class="sxs-lookup"><span data-stu-id="ec7c8-370">-2146824572</span></span><br />
<span data-ttu-id="ec7c8-371">0x800A0E84</span><span class="sxs-lookup"><span data-stu-id="ec7c8-371">0x800A0E84</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-372">Die Sicherheitseinstellungen auf diesem Computer lassen den Zugriff auf eine Datenquelle in einer anderen Domäne nicht zu.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-372">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-373"><strong>adErrURLDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-373"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-374">3727</span><span class="sxs-lookup"><span data-stu-id="ec7c8-374">3727</span></span><br />
<span data-ttu-id="ec7c8-375">-2146824561</span><span class="sxs-lookup"><span data-stu-id="ec7c8-375">-2146824561</span></span><br />
<span data-ttu-id="ec7c8-376">0x800A0E8F</span><span class="sxs-lookup"><span data-stu-id="ec7c8-376">0x800A0E8F</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-377">Die Quell-URL oder das übergeordnete Element der Ziel-URL ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-377">Either the source URL or the parent of the destination URL does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-378"><strong>adErrURLNamedRowDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-378"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-379">3737</span><span class="sxs-lookup"><span data-stu-id="ec7c8-379">3737</span></span><br />
<span data-ttu-id="ec7c8-380">-2146824551</span><span class="sxs-lookup"><span data-stu-id="ec7c8-380">-2146824551</span></span><br />
<span data-ttu-id="ec7c8-381">0x800A0E99</span><span class="sxs-lookup"><span data-stu-id="ec7c8-381">0x800A0E99</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-382">Der von dieser URL angegebene Datensatz ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-382">Record named by this URL does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-383"><strong>adErrVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-383"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-384">3733</span><span class="sxs-lookup"><span data-stu-id="ec7c8-384">3733</span></span><br />
<span data-ttu-id="ec7c8-385">-2146824555</span><span class="sxs-lookup"><span data-stu-id="ec7c8-385">-2146824555</span></span><br />
<span data-ttu-id="ec7c8-386">0x800A0E95</span><span class="sxs-lookup"><span data-stu-id="ec7c8-386">0x800A0E95</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-387">Der Anbieter konnte das von der URL angegebene Speichergerät nicht finden.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-387">Provider cannot locate the storage device indicated by the URL.</span></span> <span data-ttu-id="ec7c8-388">Stellen Sie sicher, dass die URL in der richtigen Schreibweise eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-388">Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-389"><strong>adErrWriteFile</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-389"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-390">3004</span><span class="sxs-lookup"><span data-stu-id="ec7c8-390">3004</span></span><br />
<span data-ttu-id="ec7c8-391">-2146825284</span><span class="sxs-lookup"><span data-stu-id="ec7c8-391">-2146825284</span></span><br />
<span data-ttu-id="ec7c8-392">0x800A0BBC</span><span class="sxs-lookup"><span data-stu-id="ec7c8-392">0x800A0BBC</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-393">Schreiben in Datei ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-393">Write to file failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-394"><strong>adWrnSecurityDialog</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-394"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-395">3717</span><span class="sxs-lookup"><span data-stu-id="ec7c8-395">3717</span></span><br />
<span data-ttu-id="ec7c8-396">-2146824571</span><span class="sxs-lookup"><span data-stu-id="ec7c8-396">-2146824571</span></span><br />
<span data-ttu-id="ec7c8-397">0x800A0E85</span><span class="sxs-lookup"><span data-stu-id="ec7c8-397">0x800A0E85</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-398">Nur für die interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-398">For internal use only.</span></span> <span data-ttu-id="ec7c8-399">Verwendung wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-399">Don't use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-400"><strong>adWrnSecurityDialogHeader</strong></span><span class="sxs-lookup"><span data-stu-id="ec7c8-400"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="ec7c8-401">3718</span><span class="sxs-lookup"><span data-stu-id="ec7c8-401">3718</span></span><br />
<span data-ttu-id="ec7c8-402">-2146824570</span><span class="sxs-lookup"><span data-stu-id="ec7c8-402">-2146824570</span></span><br />
<span data-ttu-id="ec7c8-403">0x800A0E86</span><span class="sxs-lookup"><span data-stu-id="ec7c8-403">0x800A0E86</span></span></p></td>
<td><p><span data-ttu-id="ec7c8-404">Nur für die interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-404">For internal use only.</span></span> <span data-ttu-id="ec7c8-405">Verwendung wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-405">Don't use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="ec7c8-406">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="ec7c8-406">ADO/WFC equivalent</span></span>

<span data-ttu-id="ec7c8-407">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="ec7c8-407">Package: **com.ms.wfc.data**</span></span>

<span data-ttu-id="ec7c8-408">Nur die folgenden Teilmengen von ADO/WFC-Entsprechungen sind definiert.</span><span class="sxs-lookup"><span data-stu-id="ec7c8-408">Only the following subsets of ADO/WFC equivalents are defined.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ec7c8-409">Konstante</span><span class="sxs-lookup"><span data-stu-id="ec7c8-409">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-410">AdoEnums. ERRORVALUE. BOUNDTOCOMMAND</span><span class="sxs-lookup"><span data-stu-id="ec7c8-410">AdoEnums.ErrorValue.BOUNDTOCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-411">AdoEnums. ERRORVALUE. dataKONVERTIERUNG</span><span class="sxs-lookup"><span data-stu-id="ec7c8-411">AdoEnums.ErrorValue.DATACONVERSION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-412">AdoEnums. ERRORVALUE. FEATURENOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ec7c8-412">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-413">AdoEnums. ERRORVALUE. ILLEGALOPERATION</span><span class="sxs-lookup"><span data-stu-id="ec7c8-413">AdoEnums.ErrorValue.ILLEGALOPERATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-414">AdoEnums. ERRORVALUE. inTRANSACTion</span><span class="sxs-lookup"><span data-stu-id="ec7c8-414">AdoEnums.ErrorValue.INTRANSACTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-415">AdoEnums. ERRORVALUE. INVALIDARGUMENT</span><span class="sxs-lookup"><span data-stu-id="ec7c8-415">AdoEnums.ErrorValue.INVALIDARGUMENT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-416">AdoEnums. ERRORVALUE. INVALIDCONNECTION</span><span class="sxs-lookup"><span data-stu-id="ec7c8-416">AdoEnums.ErrorValue.INVALIDCONNECTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-417">AdoEnums. ERRORVALUE. INVALIDPARAMINFO</span><span class="sxs-lookup"><span data-stu-id="ec7c8-417">AdoEnums.ErrorValue.INVALIDPARAMINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-418">AdoEnums. ERRORVALUE. ITEMNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="ec7c8-418">AdoEnums.ErrorValue.ITEMNOTFOUND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-419">AdoEnums. ERRORVALUE. NOCURRENTRECORD</span><span class="sxs-lookup"><span data-stu-id="ec7c8-419">AdoEnums.ErrorValue.NOCURRENTRECORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-420">AdoEnums. ERRORVALUE. NOTEXECUTING</span><span class="sxs-lookup"><span data-stu-id="ec7c8-420">AdoEnums.ErrorValue.NOTEXECUTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-421">AdoEnums. ERRORVALUE. NOTREENTRANT</span><span class="sxs-lookup"><span data-stu-id="ec7c8-421">AdoEnums.ErrorValue.NOTREENTRANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-422">AdoEnums. ERRORVALUE. objectGESCHLOSSEN</span><span class="sxs-lookup"><span data-stu-id="ec7c8-422">AdoEnums.ErrorValue.OBJECTCLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-423">AdoEnums. ERRORVALUE. OBJECTINCOLLECTION</span><span class="sxs-lookup"><span data-stu-id="ec7c8-423">AdoEnums.ErrorValue.OBJECTINCOLLECTION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-424">AdoEnums. ERRORVALUE. OBJECTNOTSET</span><span class="sxs-lookup"><span data-stu-id="ec7c8-424">AdoEnums.ErrorValue.OBJECTNOTSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-425">AdoEnums. ERRORVALUE. objectOPEN</span><span class="sxs-lookup"><span data-stu-id="ec7c8-425">AdoEnums.ErrorValue.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-426">AdoEnums. ERRORVALUE. OPERATIONCANCELLED</span><span class="sxs-lookup"><span data-stu-id="ec7c8-426">AdoEnums.ErrorValue.OPERATIONCANCELLED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-427">AdoEnums. ERRORVALUE. PROVIDERNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="ec7c8-427">AdoEnums.ErrorValue.PROVIDERNOTFOUND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-428">AdoEnums. ERRORVALUE. STILLCONNECTING</span><span class="sxs-lookup"><span data-stu-id="ec7c8-428">AdoEnums.ErrorValue.STILLCONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec7c8-429">AdoEnums. ERRORVALUE. STILLEXECUTING</span><span class="sxs-lookup"><span data-stu-id="ec7c8-429">AdoEnums.ErrorValue.STILLEXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec7c8-430">AdoEnums. ERRORVALUE. UNSAFEOPERATION</span><span class="sxs-lookup"><span data-stu-id="ec7c8-430">AdoEnums.ErrorValue.UNSAFEOPERATION</span></span></p></td>
</tr>
</tbody>
</table>

