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
localization_priority: Normal
ms.openlocfilehash: c92a43ce2f4417fde83a544022a90cfca572bf60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292349"
---
# <a name="findnextrecord-macro-action"></a><span data-ttu-id="91c1a-102">FindNextRecord-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="91c1a-102">FindNextRecord macro action</span></span>


<span data-ttu-id="91c1a-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="91c1a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="91c1a-p101">Sie können die **SuchenNächstenDatensatz** -Aktion verwenden, um den nächsten Datensatz zu suchen, der die Kriterien erfüllt, die in der vorherigen **SuchenDatensatz** -Aktion oder durch den Wert im Dialogfeld **Suchen und Ersetzen** (klicken Sie auf der Registerkarte **Start** auf **Suchen**) angegeben wurden. Sie können die **SuchenNächsterDatensatz** -Aktion verwenden, um wiederholt nach Datensätzen zu suchen. Sie können auf diese Weise z. B. nacheinander alle Datensätze für einen bestimmten Kunden finden.</span><span class="sxs-lookup"><span data-stu-id="91c1a-p101">You can use the **FindNextRecord** action to find the next record that meets the criteria specified by the previous **FindRecord** action or the value in the **Find and Replace** dialog box (on the **Home** tab, click **Find**). You can use the **FindNextRecord** action to search repeatedly for records. For example, you can move successively through all the records for a specific customer.</span></span>

## <a name="setting"></a><span data-ttu-id="91c1a-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="91c1a-107">Setting</span></span>

<span data-ttu-id="91c1a-p102">Die **SuchenNächstenDatensatz** -Aktion hat keine Argumente. Die **SuchenNächstenDatensatz** -Aktion findet den nächsten Datensatz, der die Kriterien erfüllt, die entweder von der **SuchenDatensatz** -Aktion oder im Dialogfeld **Suchen und Ersetzen** festgelegt wurden. Die Argumente für die **SuchenDatensatz** -Aktion werden auch von den Optionen im Dialogfeld **Suchen und Ersetzen** verwendet.</span><span class="sxs-lookup"><span data-stu-id="91c1a-p102">The **FindNextRecord** action doesn't have any arguments. The **FindNextRecord** action finds the next record that meets the criteria set either by the **FindRecord** action or in the **Find and Replace** dialog box. The arguments for the **FindRecord** action are shared with the options in the **Find and Replace** dialog box.</span></span>

<span data-ttu-id="91c1a-p103">Verwenden Sie die **SuchenDatensatz** -Aktion, um die Suchkriterien festzulegen. Normalerweise geben Sie eine **SuchenDatensatz** -Aktion in ein Makro ein und suchen dann mithilfe der **SuchenNächstenDatensatz** -Aktion nacheinander die Datensätze, die dieselben Kriterien erfüllen. Sie können für die **SuchenNächstenDatensatz** -Aktion einen bedingten Ausdruck in die Spalte **Bedingung** der Aktionszeile eingeben, um nur nach Datensätzen zu suchen, wenn eine bestimmte Bedingung erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="91c1a-p103">To set the search criteria, use the **FindRecord** action. Typically, you enter a **FindRecord** action in a macro and then use the **FindNextRecord** action to find succeeding records that meet the same criteria. To search for records only when a certain condition is met, you can enter a conditional expression in the **Condition** column of the action row for the **FindNextRecord** action.</span></span>

## <a name="remarks"></a><span data-ttu-id="91c1a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91c1a-114">Remarks</span></span>

<span data-ttu-id="91c1a-115">Diese Aktion hat dieselbe Wirkung wie die Schaltfläche **Weitersuchen** im Dialogfeld **Suchen und Ersetzen**.</span><span class="sxs-lookup"><span data-stu-id="91c1a-115">This action has the same effect as using the **Find Next** button in the **Find and Replace** dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="91c1a-p104">[!HINWEIS] Die **SuchenDatensatz** -Aktion entspricht zwar dem Befehl **Suchen** auf der Registerkarte **Start** für Tabellen, Abfragen und Formulare, aber sie entspricht nicht dem Befehl **Suchen** im Menü **Bearbeiten** des Codefensters. Sie können weder die **SuchenDatensatz** -Aktion noch die **SuchenNächstenDatensatz** -Aktion verwenden, um in Modulen nach Text zu suchen.</span><span class="sxs-lookup"><span data-stu-id="91c1a-p104">Although the **FindRecord** action corresponds to the **Find** command on the **Home** tab for tables, queries, and forms, it doesn't correspond to the **Find** command on the **Edit** menu in the Code window. You can't use the **FindRecord** action or **FindNextRecord** action to search for text in modules.</span></span>

> [!TIP]
> <span data-ttu-id="91c1a-118">[!TIPP] Wenn Sie das Argument **Nur aktuelles Feld** der **SuchenDatensatz** -Aktion auf **Ja** festgelegt haben, müssen Sie möglicherweise die **GeheZuSteuerelement** -Aktion verwenden, um den Fokus auf das Steuerelement zu setzen, das die gesuchten Daten enthält. Erst dann können Sie die **SuchenNächstenDatensatz** -Aktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="91c1a-118">If you've set the **Only Current Field** argument of the **FindRecord** action to **Yes**, you may need to use the **GoToControl** action to move the focus to the control containing the data you're searching for before you use the **FindNextRecord** action.</span></span>

<span data-ttu-id="91c1a-p105">Wenn der aktuell ausgewählte Text zu dem Zeitpunkt, zu dem die **SuchenNächstenDatensatz** -Makroaktion ausgeführt wird, mit dem Suchtext übereinstimmt, beginnt die Suche sofort im Anschluss an die Auswahl und findet in demselben Feld wie die Auswahl und in demselben Datensatz statt. Andernfalls beginnt die Suche am Anfang des aktuellen Datensatzes. Auf diese Weise können Sie mehrere Instanzen derselben Suchkriterien finden, die möglicherweise in einem einzelnen Datensatz angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="91c1a-p105">If the currently selected text is the same as the search text at the time the **FindNextRecord** macro action is carried out, the search begins immediately following the selection, in the same field as the selection, and in the same record. Otherwise, the search begins at the start of the current record. This enables you to find multiple instances of the same search criteria that might appear in a single record.</span></span>

<span data-ttu-id="91c1a-p106">Beachten Sie jedoch, dass bei Verwendung einer Befehlsschaltfläche zum Ausführen eines Makros, das die **SuchenNächstenDatensatz** -Aktion enthält, die erste Instanz der Suchkriterien mehrmals gefunden wird. Dieses Verhalten tritt auf, da beim Klicken auf die Befehlsschaltfläche der Fokus vom Feld mit dem entsprechenden Wert entfernt wird. Die **SuchenNächstenDatensatz** -Aktion beginnt die Suche dann ab dem Anfang des Datensatzes. Sie können dieses Problem vermeiden, indem Sie das Makro mithilfe eines Verfahrens ausführen, bei dem der Fokus nicht verändert wird, wie z. B. mit einer benutzerdefinierten Symbolleistenschaltfläche oder einer Tastenkombination, die in einem AutoKeys-Makro festgelegt wird. Sie können den Fokus im Makro aber auch auf das Feld setzen, das die Suchkriterien enthält, bevor Sie die **SuchenNächstenDatensatz** -Aktion ausführen.</span><span class="sxs-lookup"><span data-stu-id="91c1a-p106">However, note that if you use a command button to run a macro containing the **FindNextRecord** action, the first instance of the search criteria will be found repeatedly. This behavior occurs because clicking the command button removes the focus from the field containing the matching value. The **FindNextRecord** action will then begin searching from the start of the record. To avoid this problem, run the macro by using a technique that doesn't change the focus, such as a custom toolbar button or a key combination defined in an AutoKeys macro. Alternatively, set the focus in the macro to the field containing the search criteria before you carry out the **FindNextRecord** action.</span></span>

<span data-ttu-id="91c1a-127">Dasselbe Verhalten tritt ebenfalls auf, wenn Sie mithilfe einer Befehlsschaltfläche ein Makro ausführen, das die **SuchenDatensatz** -Aktion mit dem Argument **Am Anfang beginnen** enthält, sofern dieses Argument auf **Nein** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="91c1a-127">The same behavior also occurs if you use a command button to run a macro containing the **FindRecord** action with the **Find First** argument set to **No**.</span></span>

<span data-ttu-id="91c1a-128">Verwenden Sie die **FindNext** -Methode des **DoCmd** -Objekts, um die **SuchenNächstenDatensatz** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="91c1a-128">To run the **FindNextRecord** action in a Visual Basic for Applications module, use the **FindNext** method of the **DoCmd** object.</span></span>

