---
title: Index-Member (DAO)
TOCTitle: Index Members
ms:assetid: e261c5fa-ca7d-0d63-1c29-48e9231b39d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835712(v=office.15)
ms:contentKeyID: 48548290
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 895f29a5dd3e7ed267b96d6a46dc2c8710b4998e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709159"
---
# <a name="index-members-dao"></a>Index-Member (DAO)


**Betrifft**: Access 2013, Office 2013

Index-Objekte geben die Reihenfolge an, in der auf Datensätze aus Datenbanktabellen zugegriffen wird, und sie geben an, ob doppelte Datensätze akzeptiert werden. Dadurch stellen sie einen effizienten Zugriff auf Daten sicher. Bei externen Datenbanken beschreiben Index-Objekte die für externe Tabellen eingerichteten Indizes (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="methods"></a>Methoden

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></p></td>
<td><p>Erstellt ein neues <strong><a href="field-object-dao.md">Field</a></strong> -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Erstellt ein neues, benutzerdefiniertes <strong><a href="property-object-dao.md">Property</a></strong> -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Eigenschaften

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="index-clustered-property-dao.md">Clustered</a></strong></p></td>
<td><p>Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, ab ein <strong>Index</strong>-Objekt einen gruppierten Index für eine Tabelle darstellt (gilt nur für Microsoft Access-Arbeitsbereiche). <strong>Boolean</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der die Anzahl von eindeutigen, in der verknüpften Tabelle eingeschlossen Werten für das <strong><a href="index-object-dao.md">Index</a></strong> -Objekt angibt (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-fields-property-dao.md">Felder</a></strong></p></td>
<td><p>Gibt eine <strong>Fields</strong>-Auflistung zurück, die alle gespeicherten <strong>Field</strong>-Objekte für das angegebene Objekt enthält. Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-foreign-property-dao.md">Foreign</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der angibt, ob ein <strong><a href="index-object-dao.md">Index</a></strong> -Objekt einen Fremdschlüssel in einer Tabelle angibt (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></p></td>
<td><p>Legt einen Wert fest, der angibt, ob Datensätze, deren Indexfelder Nullwerte enthalten, über Indexeinträge verfügen (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-name-property-dao.md">Name</a></strong></p></td>
<td><p>Gibt den Namen des angegebenen Objekts zurück oder legt diesen fest. <strong>String</strong>-Wert mit Lese-/Schreibzugriff, wenn das Objekt noch keiner Auflistung angefügt wurde. Schreibgeschützter <strong>String</strong>-Wert, wenn das Objekt einer Auflistung angefügt wurde.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-primary-property-dao.md">Primary</a></strong></p></td>
<td><p>Legt einen Wert fest, der angibt, ob ein <strong><a href="index-object-dao.md">Index</a></strong> -Objekt einen Primärschlüsselindex für eine Tabelle darstellt, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-properties-property-dao.md">Eigenschaften</a></strong></p></td>
<td><p>Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück. Schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-required-property-dao.md">Erforderlich</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der angibt, ob ein <strong><a href="field-object-dao.md">Field</a></strong> -Objekt einen Nicht-Null-Wert erfordert, oder legt den betreffenden Wert fest.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-unique-property-dao.md">Unique</a></strong></p></td>
<td><p>Legt einen Wert fest, der angibt, ob ein <strong><a href="index-object-dao.md">Index</a></strong> -Objekt einen eindeutigen Index (Schlüssel) für eine Tabelle darstellt, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
</tbody>
</table>

