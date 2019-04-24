---
title: SetWarnings-Makroaktion
TOCTitle: SetWarnings macro action
ms:assetid: ff95b919-b1ee-c0a0-851d-71894851bb1d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837313(v=office.15)
ms:contentKeyID: 48548965
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165020
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: acf541bde41c282b752532cb74d5ec4fa4a13ca9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308659"
---
# <a name="setwarnings-macro-action"></a><span data-ttu-id="73469-102">SetWarnings-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="73469-102">SetWarnings macro action</span></span>

<span data-ttu-id="73469-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="73469-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="73469-104">Verwenden Sie die **Warnmeldungen** -Aktion, um Systemmeldungen an- oder auszuschalten.</span><span class="sxs-lookup"><span data-stu-id="73469-104">You can use the **SetWarnings** action to turn system messages on or off.</span></span>

> [!NOTE]
> <span data-ttu-id="73469-105">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="73469-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="73469-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="73469-106">Setting</span></span>

<span data-ttu-id="73469-107">Die **Warnmeldungen**-Aktion hat das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="73469-107">The **SetWarnings** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="73469-108">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="73469-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="73469-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73469-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73469-110"><strong>Warnmeldungen An</strong></span><span class="sxs-lookup"><span data-stu-id="73469-110"><strong>Warnings On</strong></span></span></p></td>
<td><p><span data-ttu-id="73469-111">Gibt an, ob Systemmeldungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="73469-111">Specifies whether system messages are displayed.</span></span> <span data-ttu-id="73469-112">Klicken Sie auf <strong>Ja</strong> (zum Aktivieren von Systemmeldungen) oder <strong>Nein</strong> (zum Deaktivieren von Systemmeldungen) im Feld <strong>Warnungen</strong> im im Abschnitt <strong>Aktionsargumente</strong> des Bereichs Makro-Generator.</span><span class="sxs-lookup"><span data-stu-id="73469-112">Click <strong>Yes</strong> (to turn on system messages) or <strong>No</strong> (to turn off system messages) in the <strong>Warnings On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder Pane.</span></span> <span data-ttu-id="73469-113">Die Standardeinstellung ist <strong>Nein</strong>.</span><span class="sxs-lookup"><span data-stu-id="73469-113">The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="73469-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73469-114">Remarks</span></span>

<span data-ttu-id="73469-p102">Mithilfe dieser Aktion können Sie verhindern, dass gebundene Warnmeldungen und Meldungsfelder das Makro anhalten. Fehlermeldungen werden jedoch immer angezeigt. Außerdem werden von Microsoft Access nur Dialogfelder angezeigt, in denen nicht nur eine Schaltfläche ausgewählt werden muss (wie **OK**, **Abbrechen**, **Ja** oder **Nein**), sondern eine Eingabe erforderlich ist. Dazu gehören z. B. alle Dialogfelder, in denen Sie Text eingeben oder unter verschiedenen Optionen auswählen müssen.</span><span class="sxs-lookup"><span data-stu-id="73469-p102">You can use this action to prevent modal warnings and message boxes from stopping the macro. However, error messages are always displayed. Also, Microsoft Access displays any dialog boxes that require input other than just choosing a button (such as **OK**, **Cancel**, **Yes**, or **No**) — for example, any dialog box that requires you to enter text or select one of several options.</span></span>

<span data-ttu-id="73469-p103">Das Ausführen dieser Aktion mit dem Argument **Warnmeldungen An** auf **Nein** hat den gleichen Effekt wie das Drücken der EINGABETASTE in Warnmeldungen oder Meldungsfeldern. Normalerweise wird bei der Anzeige einer Warnmeldung oder eines Meldungsfelds auf eine Schaltfläche **OK** oder **Ja** geklickt.</span><span class="sxs-lookup"><span data-stu-id="73469-p103">Carrying out this action with the **Warnings On** argument set to **No** has the same effect as pressing ENTER whenever a warning or message box is displayed. Typically, an **OK** or **Yes** button is chosen in response to the warning or message.</span></span>

<span data-ttu-id="73469-120">Nach Abschluss des Makros werden die Systemmeldungen automatisch von Access wieder angeschaltet.</span><span class="sxs-lookup"><span data-stu-id="73469-120">When the macro finishes, Access automatically turns the display of system messages back on.</span></span>

<span data-ttu-id="73469-p104">Diese Aktion wird häufig in Verbindung mit der **Echo** -Aktion verwendet, bei der die Ergebnisse eines Makros bis zu dessen Abschluss ausgeblendet bleiben. Mit der **Warnmeldungen** -Aktion können Sie auch die Warnmeldungen und Meldungsfelder ausblenden.</span><span class="sxs-lookup"><span data-stu-id="73469-p104">Often, you'll use this action with the **Echo** action, which hides the results of a macro until it's finished. You can use the **SetWarnings** action to hide the warnings and message boxes as well.</span></span>

> [!WARNING]
> <span data-ttu-id="73469-p105">[!VORSICHT] Die **Warnmeldungen** -Aktion kann zwar die Interaktion mit Makros vereinfachen, das Ausschalten von Systemmeldungen sollte jedoch vorsichtig erfolgen. In einigen Fällen kann das Ausführen eines Makros unangebracht sein, wenn eine bestimmte Warnmeldung angezeigt wird. Verwenden Sie diese Aktion nur, wenn Sie sich über das Ergebnis aller Makroaktionen im Klaren sind.</span><span class="sxs-lookup"><span data-stu-id="73469-p105">Although the **SetWarnings** action can simplify interactions with macros, you must be careful about turning system messages off. In some situations, you won't want to continue a macro if a certain warning message is displayed. Unless you're confident of the outcome of all macro actions, you should avoid using this action.</span></span>

<span data-ttu-id="73469-126">Verwenden Sie die **SetWarnings** -Methode des **DoCmd** -Objekts, um die **SendenObjekt** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="73469-126">To run the **SetWarnings** action in a Visual Basic for Applications (VBA) module, use the **SetWarnings** method of the **DoCmd** object.</span></span>

