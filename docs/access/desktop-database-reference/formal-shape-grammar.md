---
title: Formal Shape Grammar
TOCTitle: Formal shape grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1fcc725a554496f7aa6c7e9ad07402aecabf9416
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615452"
---
# <a name="formal-shape-grammar"></a>Formal Shape Grammar

**Gilt für**: Access 2013, Office 2013

Dies ist die formale Grammatik zum Erstellen von Shape-Befehlen:

  - Erforderliche Grammatikbegriffe sind Textzeichenfolgen, die durch spitze Klammern ("\<\>") getrennt sind.

  - Optionale Begriffe werden durch eckige Klammern (" ") getrennt. \[ \]

  - Alternativen werden durch einen Schrägstrich ("|") angegeben.

  - Wiederholte Alternativen werden durch Auslassungspunkte ("...") angegeben.

  - Durch *Alpha* wird eine Zeichenfolge aus alphabetischen Buchstaben angegeben.

  - Durch *Digit* wird eine Zeichenfolge aus Zahlen angegeben.

  - Durch *Unicode-digit* wird eine Zeichenfolge aus Unicode-Ziffern angegeben.

Alle andere Begriffe sind Literale.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Begriff</p></th>
<th><p>Definition</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;Shape-Befehl&gt;</p></td>
<td><p>SHAPE [ &lt; table-exp &gt; [[AS] &lt; alias &gt; ]][ &lt; shape-action &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;table-exp&gt;</p></td>
<td><p>{ &lt; provider-command-text &gt; } |<br />
( &lt; shape-command &gt; ) |<br />
&lt;TABLE-Name in Anführungszeichen&gt; |<br />
&lt;in Anführungszeichen&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Shape-Aktion&gt;</p></td>
<td><p>APPEND &lt; aliased-field-list&gt; |</p>
<p>COMPUTE &lt; aliased-field-list &gt; [BY &lt; field-list &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;aliased-field-list&gt;</p></td>
<td><p>&lt;aliased-field &gt; [, &lt; aliased-field... &gt; ]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Aliased-Field&gt;</p></td>
<td><p>&lt;Field-Exp &gt; [[AS]-Alias &lt; &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;field-exp&gt;</p></td>
<td><p>( &lt; relation-exp &gt; ) |</p>
<p>&lt;calculated-exp&gt; |</p>
<p>&lt;aggregate-exp&gt; |</p>
<p>&lt;new-exp&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation_exp&gt;</p></td>
<td><p>&lt;table-exp &gt; [[AS]-Alias &lt; &gt; ]</p>
<p>&lt;table-exp &gt; [[AS]-Alias &lt; &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;relation-cond-list&gt;</p></td>
<td><p>&lt;relation-cond &gt; [, &lt; relation-cond &gt; ...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation-cond&gt;</p></td>
<td><p>&lt;Feldname &gt; TO &lt; untergeordneter Verweis&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;untergeordnete Referenz&gt;</p></td>
<td><p>&lt;Feldname&gt; |</p>
<p>PARAMETER &lt; param-ref&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;param-ref&gt;</p></td>
<td><p>&lt;Anzahl&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;Feldliste&gt;</p></td>
<td><p>&lt;Feldname &gt; [, &lt; Feldname &gt; ]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;aggregate-exp&gt;</p></td>
<td><p>SUM( &lt; qualified-field-name &gt; ) |</p>
<p>AVG( &lt; qualified-field-name &gt; ) |</p>
<p>MIN( &lt; qualified-field-name &gt; ) |</p>
<p>MAX( &lt; qualified-field-name &gt; ) |</p>
<p>COUNT( &lt; qualified-alias &gt;  |  &lt; qualified-name &gt; ) |</p>
<p>STDEV( &lt; qualified-field-name &gt; ) |</p>
<p>ANY( &lt; qualified-field-name &gt; )</p></td>
</tr>
<tr class="even">
<td><p>&lt;calculated-exp&gt;</p></td>
<td><p>CALC( &lt; Ausdruck &gt; )</p></td>
</tr>
<tr class="odd">
<td><p>&lt;qualified-field-name&gt;</p></td>
<td><p>&lt;alias &gt; .[ &lt; Alias &gt; ...] &lt; Feldname&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;Alias&gt;</p></td>
<td><p>&lt;in Anführungszeichen&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Feldname&gt;</p></td>
<td><p>&lt;Anführungszeichen &gt; [[AS]-Alias &lt; &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;in Anführungszeichen&gt;</p></td>
<td><p>&quot;&lt;Schnur&gt;&quot; |</p>
<p>' &lt; string &gt; ' |</p>
<p>[ &lt; Zeichenfolge &gt; ] |</p>
<p>&lt;Namen&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;qualifizierter Name&gt;</p></td>
<td><p>alias[.alias...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;Namen&gt;</p></td>
<td><p>alpha [ alpha | Ziffer | _ | # | : | ...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Anzahl&gt;</p></td>
<td><p>Ziffer [Ziffer...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;new-exp&gt;</p></td>
<td><p>&lt;NEW-Feldtyp &gt; [( &lt; Zahl &gt; [, Zahl &lt; &gt; ])]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Feldtyp&gt;</p></td>
<td><p>Ein OLE DB- oder ADO-Datentyp.</p></td>
</tr>
<tr class="even">
<td><p>&lt;Zeichenfolge&gt;</p></td>
<td><p>unicode-char [unicode-char...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;expression&gt;</p></td>
<td><p>Ein Visual Basic für Applikationen-Ausdruck, dessen Operanden andere Nicht-CALC-Spalten in der gleichen Zeile sind.</p></td>
</tr>
</tbody>
</table>

