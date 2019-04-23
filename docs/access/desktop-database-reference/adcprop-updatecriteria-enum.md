---
title: ADCPROP_UPDATECRITERIA_ENUM
TOCTitle: ADCPROP_UPDATECRITERIA_ENUM
ms:assetid: 70da63fa-fa75-9bb4-683d-0fcb4c4a2934
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249450(v=office.15)
ms:contentKeyID: 48545571
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8be93b0b7e4b32e3c040e871ff7d97a95f1e247e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282852"
---
# <a name="adcpropupdatecriteriaenum"></a>ADCPROP\_-\_UPDATECRITERIA-Enumeration

**Gilt für**: Access 2013, Office 2013

Gibt an, welche Felder zum Erkennen von Konflikten während einer optimistischen Aktualisierung einer Zeile der Datenquelle mit einem [Recordset](recordset-object-ado.md)-Objekt verwendet werden können.

Verwenden Sie diese Konstanten mit der dynamischen **Recordset**-Eigenschaft **Update Criteria**, auf die im [Index zu dynamischen ADO-Eigenschaften](ado-dynamic-property-index.md) verwiesen wird und die in der Dokumentation [Microsoft Cursor Service für OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) beschrieben ist.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adCriteriaAllCols</strong></p></td>
<td><p>1</p></td>
<td><p>Erkennt Konflikte, wenn eine Spalte der Datenquellenzeile geändert worden ist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCriteriaKey</strong></p></td>
<td><p>0</p></td>
<td><p>Erkennt Konflikte, wenn die Schlüsselspalte der Datenquellenzeile geändert wurde, was darauf hinweist, dass die Zeile gelöscht wurde.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCriteriaTimeStamp</strong></p></td>
<td><p>3</p></td>
<td><p>Erkennt Konflikte, wenn der Zeitstempel der Datenquellenzeile geändert wurde, was darauf hinweist, dass auf die Zeile zugegriffen wurde, nachdem das Recordset abgerufen worden war.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCriteriaUpdCols</strong></p></td>
<td><p>2</p></td>
<td><p>Erkennt Konflikte, wenn eine der Spalten der Datenquellenzeile geändert wurde, die den aktualisierten Feldern des Recordsets entsprechen.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Äquivalent

Paket: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums. AdcPropUpdateCriteria. allSPALTEN</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. AdcPropUpdateCriteria. KEY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. AdcPropUpdateCriteria. TIMESTAMP</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. AdcPropUpdateCriteria. UPDCOLS</p></td>
</tr>
</tbody>
</table>

