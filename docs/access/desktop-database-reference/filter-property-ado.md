---
description: Filter-Eigenschaft
title: Filter-Eigenschaft (ADO)
TOCTitle: Filter property (ADO)
ms:assetid: 5abc528a-a6ee-34de-5d44-a3249194b0a0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249314(v=office.15)
ms:contentKeyID: 48545053
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b15abbd02ee91013f6ec2d52c88554d1a4f80d96
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626547"
---
# <a name="filter-property-ado"></a>Filter-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt einen Filter für Daten in einem [Recordset](recordset-object-ado.md) an.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Legt einen **Variant** -Wert fest oder gibt ihn zurück, der Folgendes enthalten kann:

  - **Kriterienzeichenfolge** - eine Zeichenfolge aus einer oder mehreren Klauseln, die mit **AND** - oder **OR** -Operatoren verkettet sind.

  - **Textmarkenarray** - ein Array mit eindeutigen Textmarkenwerten, die auf Datensätze im **Recordset** -Objekt verweisen.

  - Ein [FilterGroupEnum](filtergroupenum.md)-Wert.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **Filter**-Eigenschaft, um Datensätze in einem **Recordset**-Objekt gezielt herauszufiltern. Das gefilterte **Recordset**-Objekt wird zum aktuellen Cursor. Andere Eigenschaften, deren Rückgabewerte auf dem aktuellen Cursor basieren, werden dadurch beeinflusst, wie z. B. [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), [RecordCount](recordcount-property-ado.md) und [PageCount](pagecount-property-ado.md). Das liegt daran, dass der aktuelle Datensatz durch das Festlegen der **Filter**-Eigenschaft auf einen bestimmten Wert zum ersten Datensatz wechselt, der dem neuen Wert entspricht.

Die Kriterienzeichenfolge besteht aus Klauseln im Format *FieldName-Operator-Value* (z. B. "LastName = 'Smith'"). Sie können Verbundklauseln erstellen, indem Sie einzelne Klauseln mit **AND** (z. B. "LastName = 'Smith' AND FirstName = 'John'") oder **OR** (z. B. ") verketten. Sie können Verbundklauseln erstellen, indem Sie einzelne Klauseln mit **AND** verketten (z. B. "LastName = 'Smith' AND FirstName = 'John'") oder **OR** (z. B. "LastName = 'Smith' OR LastName = 'Jones'"). Halten Sie sich für Kriterienzeichenfolgen an die folgenden Richtlinien:

  - *Feldname* muss ein gültiger Feldname aus dem **Recordset**-Objekt sein. Wenn der Feldname Leerzeichen enthält, müssen Sie ihn in eckige Klammern einschließen.

  - *Der Operator* muss einer der folgenden Werte sein: \<, \> , \<=, \> =, , = oder \<\> **LIKE**.

  - *Wert* ist der Wert, mit dem Sie die Feldwerte vergleichen (z. B. 'Smith', \# 8/24/95, \# 12,345 oder $50,00). Verwenden Sie einfache Anführungszeichen mit Zeichenfolgen und Nummernzeichen ( \# ) mit Datumsangaben. Bei Zahlen können Sie Dezimalzeichen, Dollarzeichen und die wissenschaftliche Schreibweise verwenden. Wenn **LIKE** als *Operator* fungiert, kann *Wert* Platzhalterzeichen enthalten. Nur das Sternchen ( \* ) und das Prozentzeichen (%) sind zulässig, und sie müssen das letzte Zeichen in der Zeichenfolge sein. *Wert* darf nicht Null sein.

    > [!NOTE]
    > [!HINWEIS] Wenn einzelne Anführungszeichen in den Filterwert eingeschlossen werden sollen, verwenden Sie zwei einzelne Anführungszeichen zur Darstellung. Soll beispielsweise nach "O'Malley" gefiltert werden, lautet die Kriterienzeichenfolge "col1 = 'O''Malley'". Setzen Sie die Zeichenfolge zwischen Nummernzeichen (#), um einzelne Anführungszeichen am Anfang und am Ende des Filterwerts einzuschließen. Wenn Sie z. B. nach '1' filtern möchten, muss die Kriterienzeichenfolge "col1 = #'1'#" lauten.

-   Es gibt keine Rangfolge zwischen **AND und** **OR.** Die Klauseln können in Klammern zusammengefasst werden. Sie können jedoch keine Klauseln gruppieren, die mit einem **OR** verknüpft sind, und dann die Gruppe mit **einer** anderen Klausel mit and verknüpfen, wie im folgenden Codeausschnitt gezeigt:  
 `(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John'`  
  
-   Diesen Filter müssten Sie stattdessen folgendermaßen erstellen:  
 `(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John')`  

  - In einer **LIKE-Klausel** können Sie einen Platzhalter am Anfang und Am Ende des Musters verwenden (z. B. LastName Like ' \* mit \* ') oder nur am Ende des Musters (z. B. LastName Like 'Smit \* ').

Die Filterkonstanten vereinfachen das Lösen einzelner Datensatzkonflikte bei der Batchaktualisierung, indem Sie beispielsweise nur die Datensätze anzeigen, die durch den letzten Aufruf der [UpdateBatch](updatebatch-method-ado.md)-Methode beeinflusst wurden.

Die **Filter** -Eigenschaft direkt festzulegen schlägt möglicherweise wegen Konflikten mit den zugrunde liegenden Daten fehl (z. B. wenn ein Datensatz bereits von einem anderen Benutzer gelöscht wurde). In diesem Fall gibt der Anbieter Warnungen an die [Errors](errors-collection-ado.md)-Auflistung zurück, beendet die Ausführung des Programms jedoch nicht. Ein Laufzeitfehler tritt nur dann auf, wenn bei allen angeforderten Datensätzen Konflikte bestehen. Suchen Sie mithilfe der [Status](status-property-ado-recordset.md)-Eigenschaft nach Datensätzen mit Konflikten.

Das Festlegen der **Filter** -Eigenschaft auf eine leere Zeichenfolge ("") hat denselben Effekt wie die Verwendung der Konstante **adFilterNone**.

Sobald die **Filter** -Eigenschaft festgelegt wird, wechselt die aktuelle Datensatzposition zum ersten Datensatz in der gefilterten Teilmenge der Datensätze im **Recordset** -Objekt. Wird die **Filter** -Eigenschaft deaktiviert, wechselt dementsprechend die aktuelle Datensatzposition zum ersten Datensatz im **Recordset** -Objekt.

Unter der [Bookmark](bookmark-property-ado.md)-Eigenschaft finden Sie eine Erklärung der Textmarkenwerte, aus denen Sie ein Array zur Verwendung mit der **Filter** -Eigenschaft erstellen können.

Nur **Filter** in Form von Kriterienzeichenfolgen (z. B. OrderDate \> '31.12.1999') wirken sich auf den Inhalt eines permanenten **Recordsets** aus. **Filter**, die mit einem Array aus **Textmarken** oder mithilfe eines Werts aus **FilterGroupEnum** erstellt wurden, haben keinen Einfluss auf den Inhalt des permanenten Recordsets. Diese Regeln gelten für **Recordset**-Objekte, die mit clientbasierten oder serverbasierten Cursorn erstellt wurden.

> [!NOTE]
> [!HINWEIS] Angenommen, Sie wenden das Kennzeichen **adFilterPendingRecords** auf ein gefiltertes und geändertes **Recordset** -Objekt im Batchaktualisierungsmodus an. In diesem Fall ist das resultierende **Recordset** -Objekt leer, wenn der Filter auf dem Schlüsselfeld einer Tabelle mit einem Schlüssel basierte und die Änderung zu den Schlüsselfeldwerten vorgenommen wurden. Das resultierende **Recordset** -Objekt ist nicht leer, wenn eine der folgenden Aussagen zutrifft:
> - Die Filterung basierte in einer Tabelle mit einem Schlüssel auf Nichtschlüsselfeldern.
> - Die Filterung basierte in einer Tabelle mit mehreren Schlüsseln auf allen Feldern.
> - Änderungen wurden in einer Tabelle mit einem Schlüssel zu Nichtschlüsselfeldern vorgenommen.
> - Änderungen wurden in einer Tabelle mit mehreren Schlüsseln zu allen Feldern vorgenommen.

In der folgenden Tabelle werden die Ergebnisse von **adFilterPendingRecords** in verschiedenen Filter- und Änderungskombinationen zusammengefasst. Die linke Spalte zeigt die möglichen Änderungen. Änderungen können für alle Nichtschlüsselfelder, für das Schlüsselfeld in einer Tabelle mit einem Schlüssel oder für alle Schlüsselfelder in einer Tabelle mit mehreren Schlüsseln erfolgen. Die obere Zeile enthält das Filterkriterium. Die Filterung kann auf allen Nichtschlüsselfeldern, dem Schlüsselfeld in einer Tabelle mit einem Schlüssel oder allen Schlüsselfeldern in einer Tabelle mit mehreren Schlüsseln basieren. Die sich überschneidenden Zellen enthalten die Ergebnisse: + bedeutet, dass **adFilterPendingRecords** ein nicht leeres **Recordset** -Objekt ergibt; **-** zeigt ein leeres **Recordset** -Objekt an.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
</p></th>
<th><p>Nichtschlüssel</p></th>
<th><p>Ein Schlüssel</p></th>
<th><p>Mehrere Schlüssel</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Nichtschlüssel</p></td>
<td><p>+</p></td>
<td><p>+</p></td>
<td><p>+</p></td>
</tr>
<tr class="even">
<td><p>Ein Schlüssel</p></td>
<td><p>+</p></td>
<td><p>-</p></td>
<td><p>Nicht zutreffend</p></td>
</tr>
<tr class="odd">
<td><p>Mehrere Schlüssel</p></td>
<td><p>+</p></td>
<td><p>–</p></td>
<td><p>+</p></td>
</tr>
</tbody>
</table>

