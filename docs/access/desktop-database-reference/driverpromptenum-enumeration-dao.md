---
title: DriverPromptEnum Enumeration (DAO)
TOCTitle: DriverPromptEnum Enumeration
ms:assetid: 8dda5e9f-a58f-a62d-eb49-5966d4a1e086
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197361(v=office.15)
ms:contentKeyID: 48546266
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c20542c89537f16f20c9d3e30cbc14ce115bf4d6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476036"
---
# <a name="driverpromptenum-enumeration-dao"></a>DriverPromptEnum Enumeration (DAO)


**Betrifft**: Access 2013 | Office 2013

Gibt an, ob und zu welchem Zeitpunkt der Benutzer aufgefordert wird, eine Verbindung herzustellen.

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
<td><p>dbDriverComplete</p></td>
<td><p>0</p></td>
<td><p>Wenn die eingegebene Verbindungszeichenfolge das Schlüsselwort DSN enthält, verwendet der Treibermanager die in "connect" angegebene Zeichenfolge. Andernfalls verhält er sich so, als ob <strong>dbDriverPrompt</strong> angegeben worden wäre.</p></td>
</tr>
<tr class="even">
<td><p>dbDriverCompleteRequired</p></td>
<td><p>3</p></td>
<td><p>(Standard) Das Verhalten entspricht dem von <strong>dbDriverComplete</strong>, mit der Ausnahme, dass der Treiber die Steuerelemente für alle Informationen deaktiviert, die nicht für die Verbindung erforderlich sind.</p></td>
</tr>
<tr class="odd">
<td><p>dbDriverNoPrompt</p></td>
<td><p>1</p></td>
<td><p>Der Treibermanager verwendet die in "connect" angegebene Verbindungszeichenfolge. Wenn nicht ausreichend Informationen angegeben werden, wird ein auffangbarer Fehler zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>dbDriverPrompt</p></td>
<td><p>2</p></td>
<td><p>Der Treibermanager zeigt das Dialogfeld <strong>ODBC-Datenquellen</strong> an. Die zum Herstellen der Verbindung verwendete Verbindungszeichenfolge wird anhand des ausgewählten Datenquellennamens (Data Source Name, DSN) erstellt und vom Benutzer mithilfe der Dialogfelder fertig gestellt.</p></td>
</tr>
</tbody>
</table>

