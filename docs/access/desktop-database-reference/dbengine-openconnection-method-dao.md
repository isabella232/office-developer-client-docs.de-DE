---
title: DBEngine.OpenConnection-Methode (DAO)
TOCTitle: OpenConnection Method
ms:assetid: 778a581f-be42-94ee-e5c6-4cbc1843450d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196074(v=office.15)
ms:contentKeyID: 48545729
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053574
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 61014716b78af9cbfcd2b7c24e131cbd63c89095
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597457"
---
# <a name="dbengineopenconnection-method-dao"></a>DBEngine.OpenConnection-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . OpenConnection(***Name** _, _*_Options_*_, _*_ReadOnly_*_, _*_Verbinden_**)

*Ausdruck* Eine Variable, die ein **DBEngine**-Objekt darstellt.

## <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Ein Zeichenfolgenausdruck. Weitere Informationen erhalten Sie im Abschnitt "Hinweise".</p></td>
</tr>
<tr class="even">
<td><p><em>Optionen</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Legt verschiedene Optionen für die Verbindung fest, wie unter "Hinweise" beschrieben. Basierend auf diesem Wert fordert der ODBC-Treibermanager den Benutzer auf, Verbindungsdaten einzugeben, z. B. den Datenquellennamen (Data Source Name, DSN), den Benutzernamen oder das Kennwort.</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>True</strong>, um die Verbindung nur mit Lesezugriff zu öffnen, und <strong>False</strong>, wenn die Verbindung mit Lese-/Schreibzugriff geöffnet werden soll (Standard).</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine ODBC-Verbindungszeichenfolge. Die <strong><a href="connection-connect-property-dao.md">spezifischen</a></strong> Elemente und die Syntax dieser Zeichenfolge finden Sie in der Verbinden-Eigenschaft. Eine vorangestellte &quot; ODBC; &quot; ist erforderlich.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Rückgabewert

Verbindung

## <a name="remarks"></a>HinwBemerkungeneise

Mit der **OpenConnection**-Methode können Sie aus einem ODBC-Arbeitsbereich eine Verbindung zu einer ODBC-Datenquelle herstellen. Die **OpenConnection**-Methode ähnelt der **OpenDatabase**-Methode. Der wichtigste Unterschied besteht darin, dass **OpenConnection** nur in einem ODBCDirect-Arbeitsbereich verfügbar ist.

Wenn Sie einen registrierten ODBC-Datenquellennamen (DSN) im Connect-Argument angeben, kann das Name-Argument eine beliebige gültige Zeichenfolge sein und stellt außerdem die **Name-Eigenschaft** für das **Connection -Objekt** bereit. Wenn im Connect-Argument kein gültiger DSN enthalten ist, muss sich der Name auf einen gültigen ODBC-DSN beziehen, der auch die **Name-Eigenschaft** ist. Wenn weder name noch connect einen gültigen DSN enthält, kann der ODBC-Treiber-Manager (über das Optionsargument) festgelegt werden, um den Benutzer zur Eingabe der erforderlichen Verbindungsinformationen aufzufordern. Der durch die Eingabeaufforderung bereitgestellte DSN gibt dann die **Name**-Eigenschaft an.

Das Optionsargument bestimmt, ob und wann der Benutzer aufgefordert werden soll, die Verbindung herzustellen, und ob die Verbindung asynchron geöffnet werden soll. Sie können eine der folgenden Konstanten verwenden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbDriverNoPrompt</strong></p></td>
<td><p>Der ODBC-Treibermanager verwendet die in <em>dbname</em> und <em>connect</em> angegebene Verbindungszeichenfolge. Es tritt ein Laufzeitfehler auf, wenn Sie nicht genügend Informationen bereitstellen.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDriverPrompt</strong></p></td>
<td><p>Der ODBC-Treibermanager zeigt das Dialogfeld <strong>ODBC-Datenquelle</strong> an, das alle relevanten Informationen enthält, die in <em>dbname</em> oder <em>connect</em> angegeben wurden. Die Verbindungszeichenfolge entspricht dem DSN, den der Benutzer über Dialogfelder auswählt. Wenn der Benutzer keinen DSN angegeben hat, wird der standardmäßige DSN verwendet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbDriverComplete</strong></p></td>
<td><p>Standard. Enthält das Argument <em>connect</em> alle für die Verbindung erforderlichen Informationen, verwendet der ODBC-Treibermanager die Zeichenfolge in <em>connect</em>. Andernfalls verhält er sich so, als hätten Sie <strong>dbDriverPrompt</strong> angegeben.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDriverCompleteRequired</strong></p></td>
<td><p>Das Verhalten dieser Option entspricht dem von <strong>dbDriverComplete</strong>, mit der Ausnahme, dass der ODBC-Treiber die Eingabeaufforderungen für alle Informationen deaktiviert, die nicht für die Verbindung erforderlich sind.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>Die Methode wird asynchron ausgeführt. Diese Konstante kann mit jeder anderen <em>options</em>-Konstante verwendet werden.</p></td>
</tr>
</tbody>
</table>


**OpenConnection** gibt ein **Connection**-Objekt zurück, das Informationen zur Verbindung enthält. Das **Connection**-Objekt ähnelt einem **[Database](database-object-dao.md)** -Objekt. Der Hauptunterschied liegt darin, dass ein **Database**-Objekt in der Regel eine Datenbank repräsentiert, aber auch verwendet werden kann, um eine Verbindung zu einer ODBC-Datenquelle aus einem Microsoft Access-Arbeitsbereich darzustellen.

