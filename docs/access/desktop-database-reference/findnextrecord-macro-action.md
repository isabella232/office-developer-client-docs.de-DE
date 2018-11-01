---
title: SuchenNächstenDatensatz-Makroaktion
TOCTitle: FindNextRecord Macro Action
ms:assetid: 57fb6457-9098-4e81-c693-78ccd262ce0b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194307(v=office.15)
ms:contentKeyID: 48544985
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89832
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 05dec445360d5c42636880982e27e0abd46d048e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883652"
---
# <a name="findnextrecord-macro-action"></a>SuchenNächstenDatensatz-Makroaktion


**Betrifft**: Access 2013, Office 2013

Sie können die **SuchenNächstenDatensatz** -Aktion verwenden, um den nächsten Datensatz zu suchen, der die Kriterien erfüllt, die in der vorherigen **SuchenDatensatz** -Aktion oder durch den Wert im Dialogfeld **Suchen und Ersetzen** (klicken Sie auf der Registerkarte **Start** auf **Suchen**) angegeben wurden. Sie können die **SuchenNächsterDatensatz** -Aktion verwenden, um wiederholt nach Datensätzen zu suchen. Sie können auf diese Weise z. B. nacheinander alle Datensätze für einen bestimmten Kunden finden.

## <a name="setting"></a>Einstellung

Die **SuchenNächstenDatensatz** -Aktion hat keine Argumente. Die **SuchenNächstenDatensatz** -Aktion findet den nächsten Datensatz, der die Kriterien erfüllt, die entweder von der **SuchenDatensatz** -Aktion oder im Dialogfeld **Suchen und Ersetzen** festgelegt wurden. Die Argumente für die **SuchenDatensatz** -Aktion werden auch von den Optionen im Dialogfeld **Suchen und Ersetzen** verwendet.

Verwenden Sie die **SuchenDatensatz** -Aktion, um die Suchkriterien festzulegen. Normalerweise geben Sie eine **SuchenDatensatz** -Aktion in ein Makro ein und suchen dann mithilfe der **SuchenNächstenDatensatz** -Aktion nacheinander die Datensätze, die dieselben Kriterien erfüllen. Sie können für die **SuchenNächstenDatensatz** -Aktion einen bedingten Ausdruck in die Spalte **Bedingung** der Aktionszeile eingeben, um nur nach Datensätzen zu suchen, wenn eine bestimmte Bedingung erfüllt ist.

## <a name="remarks"></a>Hinweise

Diese Aktion hat dieselbe Wirkung wie die Schaltfläche **Weitersuchen** im Dialogfeld **Suchen und Ersetzen**.


> [!NOTE]
> <P>[!HINWEIS] Die <STRONG>SuchenDatensatz</STRONG> -Aktion entspricht zwar dem Befehl <STRONG>Suchen</STRONG> auf der Registerkarte <STRONG>Start</STRONG> für Tabellen, Abfragen und Formulare, aber sie entspricht nicht dem Befehl <STRONG>Suchen</STRONG> im Menü <STRONG>Bearbeiten</STRONG> des Codefensters. Sie können weder die <STRONG>SuchenDatensatz</STRONG> -Aktion noch die <STRONG>SuchenNächstenDatensatz</STRONG> -Aktion verwenden, um in Modulen nach Text zu suchen.</P>




> [!TIP]
> <P>[!TIPP] Wenn Sie das Argument <STRONG>Nur aktuelles Feld</STRONG> der <STRONG>SuchenDatensatz</STRONG> -Aktion auf <STRONG>Ja</STRONG> festgelegt haben, müssen Sie möglicherweise die <STRONG>GeheZuSteuerelement</STRONG> -Aktion verwenden, um den Fokus auf das Steuerelement zu setzen, das die gesuchten Daten enthält. Erst dann können Sie die <STRONG>SuchenNächstenDatensatz</STRONG> -Aktion verwenden.</P>



Wenn der aktuell ausgewählte Text zu dem Zeitpunkt, zu dem die **SuchenNächstenDatensatz** -Makroaktion ausgeführt wird, mit dem Suchtext übereinstimmt, beginnt die Suche sofort im Anschluss an die Auswahl und findet in demselben Feld wie die Auswahl und in demselben Datensatz statt. Andernfalls beginnt die Suche am Anfang des aktuellen Datensatzes. Auf diese Weise können Sie mehrere Instanzen derselben Suchkriterien finden, die möglicherweise in einem einzelnen Datensatz angezeigt werden.

Beachten Sie jedoch, dass bei Verwendung einer Befehlsschaltfläche zum Ausführen eines Makros, das die **SuchenNächstenDatensatz** -Aktion enthält, die erste Instanz der Suchkriterien mehrmals gefunden wird. Dieses Verhalten tritt auf, da beim Klicken auf die Befehlsschaltfläche der Fokus vom Feld mit dem entsprechenden Wert entfernt wird. Die **SuchenNächstenDatensatz** -Aktion beginnt die Suche dann ab dem Anfang des Datensatzes. Sie können dieses Problem vermeiden, indem Sie das Makro mithilfe eines Verfahrens ausführen, bei dem der Fokus nicht verändert wird, wie z. B. mit einer benutzerdefinierten Symbolleistenschaltfläche oder einer Tastenkombination, die in einem AutoKeys-Makro festgelegt wird. Sie können den Fokus im Makro aber auch auf das Feld setzen, das die Suchkriterien enthält, bevor Sie die **SuchenNächstenDatensatz** -Aktion ausführen.

Dasselbe Verhalten tritt ebenfalls auf, wenn Sie mithilfe einer Befehlsschaltfläche ein Makro ausführen, das die **SuchenDatensatz** -Aktion mit dem Argument **Am Anfang beginnen** enthält, sofern dieses Argument auf **Nein** festgelegt ist.

Verwenden Sie die **FindNext** -Methode des **DoCmd** -Objekts, um die **SuchenNächstenDatensatz** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

