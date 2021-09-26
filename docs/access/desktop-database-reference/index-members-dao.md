---
title: Indexmember (DAO)
TOCTitle: Index Members
ms:assetid: e261c5fa-ca7d-0d63-1c29-48e9231b39d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835712(v=office.15)
ms:contentKeyID: 48548290
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b29d6bd758edc6e4614d12daf2483b12d09fbf0e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589477"
---
# <a name="index-members-dao"></a>Indexmember (DAO)


**Gilt für**: Access 2013, Office 2013

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
<td><p><strong><a href="index-createfield-method-dao.md">Createfield</a></strong></p></td>
<td><p>Erstellt ein neues <strong><a href="field-object-dao.md">Field</a></strong>-Objekt (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-createproperty-method-dao.md">Createproperty</a></strong></p></td>
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
<td><p><strong><a href="index-clustered-property-dao.md">Gruppierten</a></strong></p></td>
<td><p>Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, ab ein <strong>Index</strong>-Objekt einen gruppierten Index für eine Tabelle darstellt (gilt nur für Microsoft Access-Arbeitsbereiche). <strong>Boolean</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der die Anzahl von eindeutigen, in der verknüpften Tabelle eingeschlossen Werten für das <strong><a href="index-object-dao.md">Index</a></strong> -Objekt angibt (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-fields-property-dao.md">Fields</a></strong></p></td>
<td><p>Gibt eine <strong>Fields</strong>-Auflistung zurück, die alle gespeicherten <strong>Field</strong>-Objekte für das angegebene Objekt enthält. Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-foreign-property-dao.md">Ausländisch</a></strong></p></td>
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
<td><p><strong><a href="index-primary-property-dao.md">Primäre</a></strong></p></td>
<td><p>Legt einen Wert fest, der angibt, ob ein <strong><a href="index-object-dao.md">Index</a></strong> -Objekt einen Primärschlüsselindex für eine Tabelle darstellt, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück. Schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-required-property-dao.md">Erforderlich</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der angibt, ob für ein <strong><a href="field-object-dao.md">Field</a></strong> -Objekt ein Nicht-Null-Wert erforderlich ist, oder legt den betreffenden Wert fest.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-unique-property-dao.md">Einzigartige</a></strong></p></td>
<td><p>Legt einen Wert fest, der angibt, ob ein <strong><a href="index-object-dao.md">Index</a></strong> -Objekt einen eindeutigen Index (Schlüssel) für eine Tabelle darstellt, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
</tbody>
</table>

