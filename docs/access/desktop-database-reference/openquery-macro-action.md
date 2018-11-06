---
title: OpenQuery-Makroaktion
TOCTitle: OpenQuery macro action
ms:assetid: 64bfce73-aeaf-9a78-895c-492e5da43ded
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195094(v=office.15)
ms:contentKeyID: 48545298
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89069
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fe08f6c6ab0eba46f7fff2713403f56e82983357
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999064"
---
# <a name="openquery-macro-action"></a><span data-ttu-id="b18cc-102">OpenQuery-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="b18cc-102">OpenQuery macro action</span></span>

<span data-ttu-id="b18cc-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b18cc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b18cc-p101">Mit der **ÖffnenAbfrage** -Aktion können Sie eine Auswahl- oder Kreuztabellenabfrage in der Datenblattansicht, in der Entwurfsansicht oder in der Seitenansicht öffnen. Mit dieser Aktion wird eine Aktionsabfrage ausgeführt. Sie können für die Abfrage auch einen Dateneingabemodus auswählen.</span><span class="sxs-lookup"><span data-stu-id="b18cc-p101">You can use the **OpenQuery** action to open a select or crosstab query in Datasheet view, Design view, or Print Preview. This action runs an action query. You can also select a data entry mode for the query.</span></span>

> [!NOTE]
> <span data-ttu-id="b18cc-p102">[!HINWEIS] Diese Aktion ist nur in einer Umgebung mit der Access-Datenbank (MDB oder ACCDB) verfügbar. Wenn Sie eine Umgebung mit einem Access-Projekt (ADP) verwenden, lesen Sie die Informationen zu den Aktionen **ÖffnenSicht**, **ÖffnenGespeicherteProzedur** oder **ÖffnenFunktion**.</span><span class="sxs-lookup"><span data-stu-id="b18cc-p102">This action is only available in the Access database environment (.mdb or .accdb). See the **OpenView**, **OpenStoredProcedure**, or **OpenFunction** actions if you are using the Access project environment (.adp).</span></span>

## <a name="setting"></a><span data-ttu-id="b18cc-109">Einstellung</span><span class="sxs-lookup"><span data-stu-id="b18cc-109">Setting</span></span>

<span data-ttu-id="b18cc-110">Die **ÖffnenAbfrage** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="b18cc-110">The **OpenQuery** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b18cc-111">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="b18cc-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b18cc-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b18cc-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b18cc-113"><strong>Abfragename</strong></span><span class="sxs-lookup"><span data-stu-id="b18cc-113"><strong>Query Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b18cc-p103">Der Name der Abfrage, die geöffnet werden soll. Im Feld <strong>Abfragename</strong> im Abschnitt <strong>Aktionsargumente</strong> im Bereich des Makro-Generators werden alle Abfragen in der aktuellen Datenbank angezeigt. Dies ist ein erforderliches Argument. Wenn Sie ein Makro ausführen, das die <strong>OpenQuery</strong> -Aktion in einer Bibliotheksdatenbank enthält, sucht Microsoft Access zunächst in der Bibliotheksdatenbank nach der Abfrage mit diesem Namen und anschließend in der aktuellen Datenbank.  </span><span class="sxs-lookup"><span data-stu-id="b18cc-p103">The name of the query to open. The <strong>Query Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all queries in the current database. This is a required argument.If you run a macro containing the <strong>OpenQuery</strong> action in a library database, Microsoft Access first looks for the query with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b18cc-117"><strong>Ansicht</strong></span><span class="sxs-lookup"><span data-stu-id="b18cc-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="b18cc-p104">Die Ansicht, in der die Abfrage geöffnet wird. Klicken Sie im Feld <strong>Ansicht</strong> auf <strong>Datenblatt</strong>, <strong>Entwurf</strong>, <strong>Seitenansicht</strong>, <strong>PivotTable</strong> oder <strong>PivotChart</strong>. Die Standardeinstellung ist <strong>Datenblatt</strong>.  </span><span class="sxs-lookup"><span data-stu-id="b18cc-p104">The view in which the query will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b18cc-121"><strong>Datenmodus</strong></span><span class="sxs-lookup"><span data-stu-id="b18cc-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="b18cc-p105">Der Dateneingabemodus für die Abfrage. Wird nur auf Abfragen angewendet, die in der Datenblattansicht geöffnet sind. Klicken Sie auf <strong>Hinzufügen</strong> (der Benutzer kann neue Datensätze hinzufügen, vorhandene Datensätze jedoch nicht bearbeiten), auf <strong>Bearbeiten</strong> (der Benutzer kann vorhandene Datensätze bearbeiten und neue hinzufügen) oder auf <strong>Schreibgeschützt</strong> (der Benutzer kann Datensätze nur anzeigen). Die Standardeinstellung ist <strong>Bearbeiten</strong>.  </span><span class="sxs-lookup"><span data-stu-id="b18cc-p105">The data entry mode for the query. This applies only to queries opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b18cc-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b18cc-126">Remarks</span></span>

<span data-ttu-id="b18cc-127">Wenn Sie **Datenblatt** für das Argument **Ansicht** verwenden, zeigt Access das Resultset an, sofern die Abfrage eine Auswahl-, Kreuztabellen-, Union- oder Pass-Through-Abfrage ist, deren **ReturnsRecords** -Eigenschaft auf **Ja** festgelegt ist. Zudem führt Access die Abfrage aus, wenn es sich um eine Aktions-, Datendefinitions- oder Pass-Through-Abfrage handelt, deren **ReturnsRecords** -Eigenschaft auf **Nein** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b18cc-127">If you use **Datasheet** for the **View** argument, Access displays the result set if the query is a select, crosstab, union, or pass-through query whose **ReturnsRecords** property is set to **Yes**; and it runs the query if it is an action, data-definition, or pass-through query whose **ReturnsRecords** property is set to **No**.</span></span>

<span data-ttu-id="b18cc-p106">Die **ÖffnenAbfrage** -Aktion bewirkt dasselbe, wie wenn Sie auf die Abfrage im Navigationsbereich doppelklicken oder mit der rechten Maustaste auf die Abfrage im Navigationsbereich klicken und dann eine Ansicht auswählen. Mit dieser Aktion können Sie zusätzliche Optionen auswählen.</span><span class="sxs-lookup"><span data-stu-id="b18cc-p106">The **OpenQuery** action is similar to double-clicking the query in the Navigation Pane, or right-clicking the query in the Navigation Pane and selecting a view. With this action you can select additional options.</span></span>

> [!TIP]
> - <span data-ttu-id="b18cc-p107">Sie können eine Abfrage aus dem Navigationsbereich in die Aktionszeile eines Makros ziehen. Damit wird automatisch eine **ÖffnenAbfrage** -Aktion erstellt, mit der die Abfrage in der Datenblattansicht geöffnet wird. Wenn Sie in die Entwurfsansicht wechseln, während die Abfrage geöffnet ist, werden die Einstellungen für das Argument **Datenmodus** für die Abfrage entfernt. Diese Einstellung ist nicht wirksam, auch wenn der Benutzer zur Datenblattansicht zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="b18cc-p107">You can drag a query from the Navigation Pane to a macro action row. This automatically creates an **OpenQuery** action that opens the query in Datasheet view. Switching to Design view while the query is open removes the **Data Mode** argument setting for the query. This setting isn't in effect even if the user returns to Datasheet view.</span></span>
> - <span data-ttu-id="b18cc-134">Wenn Sie nicht möchten, dass die Systemmeldungen angezeigt werden, die normalerweise angezeigt werden (und anzeigen, dass es sich um eine Aktionsabfrage handelt, und angeben, wie viele Datensätze betroffen sind), wenn eine Aktionsabfrage ausgeführt wird, können Sie die Anzeige dieser Meldungen mithilfe der **Warnmeldungen** -Aktion unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="b18cc-134">If you don't want to display the system messages that normally appear when an action query is run (indicating it is an action query and showing how many records will be affected), you can use the **SetWarnings** action to suppress the display of these messages.</span></span>

<span data-ttu-id="b18cc-135">Wenn Sie die **ÖffnenAbfrage** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) ausführen möchten, verwenden Sie die **OpenQuery** -Methode des **DoCmd** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="b18cc-135">To run the **OpenQuery** action in a Visual Basic for Applications (VBA) module, use the **OpenQuery** method of the **DoCmd** object.</span></span>

