---
title: Shape-Befehle im Allgemeinen
TOCTitle: Shape Commands in General
ms:assetid: ad555aa7-bc64-b495-a98d-e927061a5809
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249814(v=office.15)
ms:contentKeyID: 48547039
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5cf2dc58ee3fa9205b9657366d8706b64b0aa58a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861029"
---
# <a name="shape-commands-in-general"></a>Shape-Befehle im Allgemeinen


**Betrifft**: Access 2013 | Office 2013

Durch Datenstrukturierung werden die Spalten eines geformten **Recordset** -Objekts, die Beziehungen zwischen den durch die Spalten dargestellten Entitäten und die Methode, mit der das **Recordset** -Objekt mit Daten aufgefüllt wird, definiert.

Ein geformtes **Recordset** -Objekt kann aus den folgenden Spaltentypen bestehen.

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


Ein Shape-Befehl kann eine Klausel enthalten, durch die ein Abfragebefehl an einen zugrunde liegenden Datenprovider angegeben wird, durch den ein Recordset-Objekt zurückgegeben wird. Die Syntax der Abfrage hängt von den Anforderungen des zugrunde liegenden Datenproviders ab. Normalerweise handelt es sich dabei um die SQL-Sprache, obwohl für ADO keine bestimmte Abfragesprache erforderlich ist.

Sie können eine SQL JOIN-Klausel verwenden, um zwei Tabellen miteinander in Beziehung zu setzen. Durch ein hierarchisches **Recordset** -Objekt werden die Informationen jedoch möglicherweise effizienter dargestellt. In jeder Zeile eines durch JOIN erstellten **Recordset** -Objekts werden Informationen aus einer der Tabellen redundant wiederholt. Ein hierarchisches **Recordset** -Objekt hat nur ein übergeordnetes **Recordset** -Objekt für jedes einzelne mehrerer untergeordneter **Recordset** -Objekte.

<<<<<<< HEAD-Shape-Befehle können durch **Recordset** -Objekte oder durch Festlegen der [CommandText](commandtext-property-ado.md) -Eigenschaft des [Command](command-object-ado.md) -Objekts und anschließendes Aufrufen der [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) -Methode ausgegeben werden.
=== Shape-Befehle können durch **Recordset** -Objekte oder durch Festlegen der [CommandText](commandtext-property-ado.md) -Eigenschaft des [Command](command-object-ado.md) -Objekts und anschließendes Aufrufen der [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) -Methode ausgegeben werden.
>>>>>>> master

Shape-Befehle können geschachtelt werden. Das heißt, der übergeordnete Befehl oder der untergeordnete Befehl kann selbst ein weiterer Shape-Befehl sein.

Vom Shape-Anbieter wird immer ein Clientcursor zurückgegeben, selbst wenn der Benutzer die Cursorplatzierung adUseServer angibt.

Weitere Informationen zum Navigieren in einem hierarchischen **Recordset** -Objekt finden Sie unter [Zugreifen auf Zeilen in einem hierarchischen Recordset](accessing-rows-in-a-hierarchical-recordset.md).

Genaue Informationen zu syntaktisch richtigen Shape-Befehlen finden Sie unter Formale Grammatik für Formen.

## <a name="see-also"></a>Siehe auch

- [Ausstellen von Befehlen für den zugrunde liegenden Datenprovider](issuing-commands-to-the-underlying-data-provider.md)

