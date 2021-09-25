---
title: Document-Elemente (DAO)
TOCTitle: Document Members
ms:assetid: 8de770e6-e4d1-372a-3ef8-8539c921b41f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197365(v=office.15)
ms:contentKeyID: 48546270
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7fdfd95721d0c5c8d93a9a26185883c18227da73
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581420"
---
# <a name="document-members-dao"></a>Document-Elemente (DAO)


**Gilt für**: Access 2013, Office 2013

Ein Document-Objekt schließt Informationen zu einer Objektinstanz ein. Bei dem Objekt kann es sich um eine Datenbank, gespeicherte Tabelle, Abfrage oder Beziehung handeln (gilt nur für Microsoft Access-Datenbanken).

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
<td><p><strong><a href="document-createproperty-method-dao.md">Createproperty</a></strong></p></td>
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
<td><p><strong><a href="document-container-property-dao.md">Container</a></strong></p></td>
<td><p>Gibt den Namen des <strong><a href="container-object-dao.md">Container</a></strong> -Objekts zurück, zu dem ein <strong>Document</strong>-Objekt gehört (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>Gibt das Datum und die Uhrzeit zurück, zu der ein Objekt erstellt wurde. Schreibgeschützter <strong>Variant</strong>-Wert.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>Gibt das Datum und die Uhrzeit der letzten Änderung eines Objekts zurück. Schreibgeschützter <strong>Variant</strong>-Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="document-name-property-dao.md">Name</a></strong></p></td>
<td><p>Gibt den Namen des angegebenen Objekts zurück. Read-only <strong>Zeichenfolge</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="document-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück. Schreibgeschützt.</p></td>
</tr>
</tbody>
</table>

