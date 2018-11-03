---
title: PermissionEnum (Aufzählung) (DAO)
TOCTitle: PermissionEnum Enumeration
ms:assetid: dcce9940-f8a7-e915-1b69-05c341bea8cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835373(v=office.15)
ms:contentKeyID: 48548147
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed3abb0e3ff76ae19c6c19a3e2040b338e2b5ff3
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945866"
---
# <a name="permissionenum-enumeration-dao"></a>PermissionEnum (Aufzählung) (DAO)


**Betrifft**: Access 2013, Office 2013

Hiermit geben Sie zusammen mit der **Permissions**-Eigenschaft den Berechtigungstyp an.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbSecCreate</p></td>
<td><p>1</p></td>
<td><p>Der Benutzer kann neue Dokumente erstellen (nicht für Dokumentobjekte gültig).</p></td>
</tr>
<tr class="even">
<td><p>dbSecDBAdmin</p></td>
<td><p>8</p></td>
<td><p>Der Benutzer kann eine Datenbank replizieren und das Datenbankkennwort ändern (nicht für Dokumentobjekte gültig).</p></td>
</tr>
<tr class="odd">
<td><p>dbSecDBCreate</p></td>
<td><p>1</p></td>
<td><p>Der Benutzer kann neue Datenbanken erstellen. Diese Option ist nur im Datenbankencontainer in der Arbeitsgruppen-Informationsdatei (Systen.mdw) gültig. Diese Konstante ist nicht für Dokumentobjekte gültig.</p></td>
</tr>
<tr class="even">
<td><p>dbSecDBExclusive</p></td>
<td><p>4</p></td>
<td><p>Der Benutzer hat exklusiven Zugriff auf die Datenbank.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecDBOpen</p></td>
<td><p>2</p></td>
<td><p>Der Benutzer kann die Datenbank öffnen.</p></td>
</tr>
<tr class="even">
<td><p>dbSecDelete</p></td>
<td><p>65536</p></td>
<td><p>Der Benutzer kann das Objekt löschen.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecDeleteData</p></td>
<td><p>128</p></td>
<td><p>Der Benutzer kann Datensätze löschen.</p></td>
</tr>
<tr class="even">
<td><p>dbSecFullAccess</p></td>
<td><p>1048575</p></td>
<td><p>Der Benutzer hat Vollzugriff auf das Objekt.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecInsertData</p></td>
<td><p>32</p></td>
<td><p>Der Benutzer kann Datensätze hinzufügen.</p></td>
</tr>
<tr class="even">
<td><p>dbSecNoAccess</p></td>
<td><p>0</p></td>
<td><p>Der Benutzer hat keinen Zugriff auf das Objekt (nicht für Dokumentobjekte gültig).</p></td>
</tr>
<tr class="odd">
<td><p>dbSecReadDef</p></td>
<td><p>4</p></td>
<td><p>Der Benutzer kann die Tabellendefinition lesen, einschließlich Spalten- und Indexinformationen.</p></td>
</tr>
<tr class="even">
<td><p>dbSecReadSec</p></td>
<td><p>131072</p></td>
<td><p>Der Benutzer kann die sicherheitsbezogenen Informationen des Objekts lesen.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecReplaceData</p></td>
<td><p>64</p></td>
<td><p>Der Benutzer kann Datensätze ändern.</p></td>
</tr>
<tr class="even">
<td><p>dbSecRetrieveData</p></td>
<td><p>20</p></td>
<td><p>Der Benutzer kann Daten vom Dokumentobjekt abrufen.</p></td>
</tr>
<tr class="odd">
<td><p>über dbSecWriteDef</p></td>
<td><p>65548</p></td>
<td><p>Der Benutzer kann die Tabellendefinition ändern oder löschen, einschließlich Spalten- und Indexinformationen.</p></td>
</tr>
<tr class="even">
<td><p>dbSecWriteOwner</p></td>
<td><p>524288</p></td>
<td><p>Der Benutzer kann die Einstellung für die Owner-Eigenschaft ändern.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecWriteSec</p></td>
<td><p>262144</p></td>
<td><p>Der Benutzer kann Zugriffsberechtigungen ändern.</p></td>
</tr>
</tbody>
</table>

