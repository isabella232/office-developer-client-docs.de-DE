---
title: Shape-Befehle im Allgemeinen
TOCTitle: Shape commands in general
ms:assetid: ad555aa7-bc64-b495-a98d-e927061a5809
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249814(v=office.15)
ms:contentKeyID: 48547039
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 399836158084f07b30b06a9fb099da74527d0cb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308652"
---
# <a name="shape-commands-in-general"></a>Shape-Befehle im Allgemeinen

**Gilt für**: Access 2013, Office 2013

Durch Datenstrukturierung werden die Spalten eines geformten **Recordset** -Objekts, die Beziehungen zwischen den durch die Spalten dargestellten Entitäten und die Methode, mit der das **Recordset** -Objekt mit Daten aufgefüllt wird, definiert.

Ein geformtes **Recordset**-Objekt kann aus den folgenden Spaltentypen bestehen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Spaltentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>data</p></td>
<td><p>Felder eines <strong>Recordset</strong>-Objekts, die von einem Abfragebefehl an einen Datenprovider, eine Tabelle oder ein vorher geformtes <strong>Recordset</strong>-Objekt zurückgegeben werden.</p></td>
</tr>
<tr class="even">
<td><p>Kapitel</p></td>
<td><p>Ein Verweis auf ein anderes <strong>Recordset</strong>-Objekt, das als <em>Kapitel</em> bezeichnet wird. Kapitelspalten ermöglichen des Definieren einer <em>Übergeordnet-Untergeordnet</em>-Beziehung, in der das <em>übergeordnete</em> Element das <strong>Recordset</strong>-Objekt ist, das die Kapitelspalte enthält, und das <em>untergeordnete</em> Element das durch das Kapitel dargestellte <strong>Recordset</strong>-Objekt ist.</p></td>
</tr>
<tr class="odd">
<td><p>Aggregat</p></td>
<td><p>Der Wert der Spalte wird abgeleitet durch Ausführen einer <em>Aggregatfunktion</em> für alle Zeilen oder eine Spalte aller Zeilen eines untergeordneten <strong>Recordset</strong>-Objekts. (Siehe "Aggregatfunktionen" im folgenden Thema, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregatfunktion, die CALC-Funktion und das NEW-Schlüsselwort</a>.)</p></td>
</tr>
<tr class="even">
<td><p>Berechneter Ausdruck</p></td>
<td><p>Der Wert der Spalte wird abgeleitet durch Berechnen eines Visual Basic für Applikationen-Ausdrucks für Spalten in der gleichen Zeile des <strong>Recordset</strong>-Objekts. Der Ausdruck ist das Argument für die CALC-Funktion. (Siehe "Berechneter Ausdruck" im folgenden Thema, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregatfunktion, die CALC-Funktion und das NEW-Schlüsselwort</a> und in <a href="visual-basic-for-applications-functions.md">Visual Basic für Applikationen (Funktionen)</a>.)</p></td>
</tr>
<tr class="odd">
<td><p>Neu</p></td>
<td><p>Leere erstellte Felder, die später mit Daten aufgefüllt werden können. Die Spalte wird mit dem NEW-Schlüsselwort definiert. (Siehe "NEW-Schlüsselwort" im folgenden Thema, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregatfunktion, die CALC-Funktion und das NEW-Schlüsselwort</a>.)</p></td>
</tr>
</tbody>
</table>


A shape command may contain a clause specifying a query command to an underlying data provider that will return a **Recordset** object. The query's syntax depends on the requirements of the underlying data provider. This will usually be Structured Query Language (SQL), although ADO does not require the use of any particular query language.

Sie können eine SQL JOIN-Klausel verwenden, um zwei Tabellen miteinander in Beziehung zu setzen. Durch ein hierarchisches **Recordset** -Objekt werden die Informationen jedoch möglicherweise effizienter dargestellt. In jeder Zeile eines durch JOIN erstellten **Recordset** -Objekts werden Informationen aus einer der Tabellen redundant wiederholt. Ein hierarchisches **Recordset** -Objekt hat nur ein übergeordnetes **Recordset** -Objekt für jedes einzelne mehrerer untergeordneter **Recordset** -Objekte.

Shape commands can be issued by **Recordset** objects or by setting the [CommandText](commandtext-property-ado.md) property of the [Command](command-object-ado.md) object and then calling the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.

Shape commands can be nested. Das heißt, der *übergeordnete Befehl* oder *untergeordnete* Befehl kann selbst ein anderer Shape-Befehl sein.

The shape provider always returns a client cursor, even when the user specifies a cursor location of **adUseServer**.

Weitere Informationen zum Navigieren in einem hierarchischen **Recordset** -Objekt finden Sie unter [Zugreifen auf Zeilen in einem hierarchischen Recordset](accessing-rows-in-a-hierarchical-recordset.md).

For precise information about syntactically correct shape commands, see [Formal Shape Grammar](formal-shape-grammar.md).

## <a name="see-also"></a>Siehe auch

- [Ausgeben von Befehlen an den zuGrunde liegenden Datenanbieter](issuing-commands-to-the-underlying-data-provider.md)

