---
title: FindNextRecord-Makroaktion
TOCTitle: FindNextRecord macro action
ms:assetid: 57fb6457-9098-4e81-c693-78ccd262ce0b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194307(v=office.15)
ms:contentKeyID: 48544985
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89832
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: c83badfcf611de549b3ffe5b1ef9f8f85ba34a13
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612091"
---
# <a name="findnextrecord-macro-action"></a>FindNextRecord-Makroaktion


**Gilt für**: Access 2013, Office 2013

Sie können die **SuchenNächstenDatensatz** -Aktion verwenden, um den nächsten Datensatz zu suchen, der die Kriterien erfüllt, die in der vorherigen **SuchenDatensatz** -Aktion oder durch den Wert im Dialogfeld **Suchen und Ersetzen** (klicken Sie auf der Registerkarte **Start** auf **Suchen**) angegeben wurden. Sie können die **SuchenNächsterDatensatz** -Aktion verwenden, um wiederholt nach Datensätzen zu suchen. Sie können auf diese Weise z. B. nacheinander alle Datensätze für einen bestimmten Kunden finden.

## <a name="setting"></a>Einstellung

Die **SuchenNächstenDatensatz** -Aktion hat keine Argumente. Die **SuchenNächstenDatensatz** -Aktion findet den nächsten Datensatz, der die Kriterien erfüllt, die entweder von der **SuchenDatensatz** -Aktion oder im Dialogfeld **Suchen und Ersetzen** festgelegt wurden. Die Argumente für die **SuchenDatensatz** -Aktion werden auch von den Optionen im Dialogfeld **Suchen und Ersetzen** verwendet.

Verwenden Sie die **SuchenDatensatz** -Aktion, um die Suchkriterien festzulegen. Normalerweise geben Sie eine **SuchenDatensatz** -Aktion in ein Makro ein und suchen dann mithilfe der **SuchenNächstenDatensatz** -Aktion nacheinander die Datensätze, die dieselben Kriterien erfüllen. Sie können für die **SuchenNächstenDatensatz** -Aktion einen bedingten Ausdruck in die Spalte **Bedingung** der Aktionszeile eingeben, um nur nach Datensätzen zu suchen, wenn eine bestimmte Bedingung erfüllt ist.

## <a name="remarks"></a>HinwBemerkungeneise

Diese Aktion hat dieselbe Wirkung wie die Schaltfläche **Weitersuchen** im Dialogfeld **Suchen und Ersetzen**.

> [!NOTE]
> [!HINWEIS] Die **SuchenDatensatz** -Aktion entspricht zwar dem Befehl **Suchen** auf der Registerkarte **Start** für Tabellen, Abfragen und Formulare, aber sie entspricht nicht dem Befehl **Suchen** im Menü **Bearbeiten** des Codefensters. Sie können weder die **SuchenDatensatz** -Aktion noch die **SuchenNächstenDatensatz** -Aktion verwenden, um in Modulen nach Text zu suchen.

> [!TIP]
> [!TIPP] Wenn Sie das Argument **Nur aktuelles Feld** der **SuchenDatensatz** -Aktion auf **Ja** festgelegt haben, müssen Sie möglicherweise die **GeheZuSteuerelement** -Aktion verwenden, um den Fokus auf das Steuerelement zu setzen, das die gesuchten Daten enthält. Erst dann können Sie die **SuchenNächstenDatensatz** -Aktion verwenden.

Wenn der aktuell ausgewählte Text zu dem Zeitpunkt, zu dem die **SuchenNächstenDatensatz** -Makroaktion ausgeführt wird, mit dem Suchtext übereinstimmt, beginnt die Suche sofort im Anschluss an die Auswahl und findet in demselben Feld wie die Auswahl und in demselben Datensatz statt. Andernfalls beginnt die Suche am Anfang des aktuellen Datensatzes. Auf diese Weise können Sie mehrere Instanzen derselben Suchkriterien finden, die möglicherweise in einem einzelnen Datensatz angezeigt werden.

Beachten Sie jedoch, dass bei Verwendung einer Befehlsschaltfläche zum Ausführen eines Makros, das die **SuchenNächstenDatensatz** -Aktion enthält, die erste Instanz der Suchkriterien mehrmals gefunden wird. Dieses Verhalten tritt auf, da beim Klicken auf die Befehlsschaltfläche der Fokus vom Feld mit dem entsprechenden Wert entfernt wird. Die **SuchenNächstenDatensatz** -Aktion beginnt die Suche dann ab dem Anfang des Datensatzes. Sie können dieses Problem vermeiden, indem Sie das Makro mithilfe eines Verfahrens ausführen, bei dem der Fokus nicht verändert wird, wie z. B. mit einer benutzerdefinierten Symbolleistenschaltfläche oder einer Tastenkombination, die in einem AutoKeys-Makro festgelegt wird. Sie können den Fokus im Makro aber auch auf das Feld setzen, das die Suchkriterien enthält, bevor Sie die **SuchenNächstenDatensatz** -Aktion ausführen.

Dasselbe Verhalten tritt ebenfalls auf, wenn Sie mithilfe einer Befehlsschaltfläche ein Makro ausführen, das die **SuchenDatensatz** -Aktion mit dem Argument **Am Anfang beginnen** enthält, sofern dieses Argument auf **Nein** festgelegt ist.

Verwenden Sie die **FindNext** -Methode des **DoCmd** -Objekts, um die **SuchenNächstenDatensatz** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

