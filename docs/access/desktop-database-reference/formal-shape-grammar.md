---
title: Formal Shape Grammar
TOCTitle: Formal shape grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d30ff9146146bb0457a5aa383b2b720a4fdaeb78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292321"
---
# <a name="formal-shape-grammar"></a>Formal Shape Grammar

**Gilt für**: Access 2013, Office 2013

Dies ist die formale Grammatik zum Erstellen von Shape-Befehlen:

  - Erforderliche Grammatikbegriffe sind Textzeichenfolgen, die durch spitze Klammern ("\<\>") getrennt sind.

  - Optionale Ausdrücke werden durch eckige Klammern ("\[ \]") getrennt.

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
<td><p>Shape [&lt;Tabelle-exp&gt; [[as] &lt;Alias&gt;]] [&lt;Shape-Aktion&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;Tabelle-Exp&gt;</p></td>
<td><p>{&lt;Anbieter-Command-Text&gt;} |<br />
(&lt;Shape-Befehl&gt;) |<br />
Tabelle &lt;in Anführungszeichen-Name&gt; |<br />
&lt;zitiert-Name&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Shape-Aktion&gt;</p></td>
<td><p>Alias &lt;-field-list anfügen&gt; |</p>
<p>COMPUTE &lt;aliased-Field-List&gt; [by &lt;Field-List&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;aliased-field-list&gt;</p></td>
<td><p>&lt;aliased-Field&gt; [, &lt;aliased-Field... &gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Alias-Field&gt;</p></td>
<td><p>&lt;Field-exp&gt; [[as] &lt;Alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;Field-Exp&gt;</p></td>
<td><p>(&lt;Relation-exp&gt;) |</p>
<p>&lt;berechnet-Exp&gt; |</p>
<p>&lt;Aggregieren-Exp&gt; |</p>
<p>&lt;neu-Exp&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation_exp&gt;</p></td>
<td><p>&lt;Tabelle-exp&gt; [[as] &lt;Alias&gt;]</p>
<p>&lt;Tabelle-exp&gt; [[as] &lt;Alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;Relation-Ltg-Liste&gt;</p></td>
<td><p>&lt;Relation-Ltg&gt; [, &lt;Relation-Ltg&gt;...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Relation-Ltg&gt;</p></td>
<td><p>&lt;Field-Name&gt; unter &lt;Child-Ref&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;Child-Ref&gt;</p></td>
<td><p>&lt;Feldname&gt; |</p>
<p>PARAMETER &lt;param-Ref&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;param-Ref&gt;</p></td>
<td><p>&lt;Anzahl&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;Field-List&gt;</p></td>
<td><p>&lt;Feldnamen&gt; [, &lt;Feldname]&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Aggregieren-Exp&gt;</p></td>
<td><p>SUM (&lt;Qualified-Field-Name&gt;) |</p>
<p>AVG (&lt;Qualified-Field-Name&gt;) |</p>
<p>MIN (&lt;Qualified-Field-Name&gt;) |</p>
<p>MAX (&lt;Qualified-Field-Name&gt;) |</p>
<p>COUNT (&lt;Qualified-Alias&gt; | &lt;Qualified-Name&gt;) |</p>
<p>STDEV (&lt;Qualified-Field-Name&gt;) |</p>
<p>ANY (&lt;Qualified-Field-Name&gt;)</p></td>
</tr>
<tr class="even">
<td><p>&lt;berechnet-Exp&gt;</p></td>
<td><p>CALC (&lt;Ausdruck&gt;)</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Qualified-Field-Name&gt;</p></td>
<td><p>&lt;Alias&gt;. [&lt;Alias&gt;...] &lt;Feldname&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;Alias&gt;</p></td>
<td><p>&lt;zitiert-Name&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Feldname&gt;</p></td>
<td><p>&lt;Anführungs&gt; Zeichen-Name [ &lt;[&gt;as] Alias]</p></td>
</tr>
<tr class="even">
<td><p>&lt;zitiert-Name&gt;</p></td>
<td><p>&quot;&lt;Zeichenfolge&gt;&quot; |</p>
<p>'&lt;Zeichen&gt;Folge ' |</p>
<p>[&lt;Zeichen&gt;Folge] |</p>
<p>&lt;Namen&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;qualifizierter Name&gt;</p></td>
<td><p>Alias [. Alias...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;Namen&gt;</p></td>
<td><p>Alpha [alpha | Ziffer | _ | # |: |...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Anzahl&gt;</p></td>
<td><p>Ziffer [Ziffer...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;neu-Exp&gt;</p></td>
<td><p>Neuer &lt;field-type&gt; [(&lt;Number&gt; [, &lt;Number&gt;])]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Field-Typ&gt;</p></td>
<td><p>Ein OLE DB- oder ADO-Datentyp.</p></td>
</tr>
<tr class="even">
<td><p>&lt;string&gt;</p></td>
<td><p>Unicode-Char [Unicode-Char...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Ausdruck&gt;</p></td>
<td><p>Ein Visual Basic für Applikationen-Ausdruck, dessen Operanden andere Nicht-CALC-Spalten in der gleichen Zeile sind.</p></td>
</tr>
</tbody>
</table>

