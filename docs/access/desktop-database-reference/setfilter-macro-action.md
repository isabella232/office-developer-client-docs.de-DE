---
title: FestlegenFilter-Makroaktion
TOCTitle: SetFilter Macro Action
ms:assetid: dee699e2-0840-1612-23ce-199ef8d30566
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835438(v=office.15)
ms:contentKeyID: 48548203
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm122943
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fad18c6e7a9ca185e15598b532bbc6de4e5b4f9a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475448"
---
# <a name="setfilter-macro-action"></a><span data-ttu-id="f7db2-102">FestlegenFilter-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="f7db2-102">SetFilter Macro Action</span></span>

<span data-ttu-id="f7db2-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7db2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f7db2-104">Mit der **FestlegenFilter** -Aktion wenden Sie auf die Datensätze im aktiven Datenblatt, Formular, Bericht oder in der aktuellen Tabelle einen Filter an.</span><span class="sxs-lookup"><span data-stu-id="f7db2-104">You can use the **SetFilter** action to apply a filter to the records in the active datasheet, form, report, or table.</span></span>

## <a name="setting"></a><span data-ttu-id="f7db2-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="f7db2-105">Setting</span></span>

<span data-ttu-id="f7db2-106">Die **FestlegenFilter** -Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7db2-106">The **SetFilter** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f7db2-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="f7db2-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f7db2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7db2-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7db2-109">Filter Name</span><span class="sxs-lookup"><span data-stu-id="f7db2-109">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="f7db2-110">Wenn angegeben, der Name einer Abfrage oder eines Filters, der als Abfrage gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="f7db2-110">If provided, the name of a query or of a filter saved as a query.</span></span> <span data-ttu-id="f7db2-111">Dieses Argument oder das Argument WhereCondition ist in einer Clientdatenbank erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f7db2-111">This argument or the WhereCondition argument is required in a client database.</span></span> <span data-ttu-id="f7db2-112">In Webdatenbanken ist dieses Argument nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f7db2-112">In a Web database, this argument is not available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7db2-113">Where Condition</span><span class="sxs-lookup"><span data-stu-id="f7db2-113">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="f7db2-p102">Wenn angegeben, eine SQL-WHERE-Klausel, mit der die Datensätze im Datenblatt, Formular, Bericht oder in der Tabelle eingeschränkt werden. In Webdatenbanken ist dieses Argument erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f7db2-p102">If provided, a SQL WHERE clause that restricts the records in the datasheet, form, report, or table. In a Web database, this argument is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7db2-116">Control Name</span><span class="sxs-lookup"><span data-stu-id="f7db2-116">Control Name</span></span></p></td>
<td><p><span data-ttu-id="f7db2-p103">Wenn angegeben, der Name des Steuerelements, das dem zu filternden Unterformular oder Unterbericht entspricht. Wenn das Argument leer ist, wird das aktuelle Objekt gefiltert.</span><span class="sxs-lookup"><span data-stu-id="f7db2-p103">If provided, the name of the control that corresponds to the subform or subreport to be filtered. If empty, the current object is filtered.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f7db2-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f7db2-119">Remarks</span></span>

<span data-ttu-id="f7db2-120">In einer Webdatenbank darf das Bedingung-Argument nicht mit einem Gleichheitszeichen (=) beginnen.</span><span class="sxs-lookup"><span data-stu-id="f7db2-120">In a web database, the Where Condition argument cannot begin with an equal sign (=).</span></span>

<span data-ttu-id="f7db2-121">Beim Ausführen dieser Aktion wird der Filter auf die Tabelle, das Formular, den Bericht oder das Datenblatt (z. B. Abfrageergebnis) angewendet, das aktiv ist und den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="f7db2-121">When you run this action, the filter is applied to the table, form, report or datasheet (for example, query result) that is active and has the focus.</span></span>

<span data-ttu-id="f7db2-p104">Mit der  **Filter** -Eigenschaft des aktiven Objekts können Sie das WhereCondition-Argument speichern und zu einem späteren Zeitpunkt anwenden. Filter werden zusammen mit den Objekten gespeichert, in denen sie erstellt wurden. Sie werden zwar automatisch geladen, wenn das Objekt geöffnet wird, aber werden nicht automatisch angewendet.</span><span class="sxs-lookup"><span data-stu-id="f7db2-p104">The **Filter** property of the active object is used to save the WhereCondition argument and apply it at a later time. Filters are saved with the objects in which they are created. They are automatically loaded when the object is opened, but they are not automatically applied.</span></span>

<span data-ttu-id="f7db2-125">Legen Sie in einer Clientdatenbank um automatisch einen Filter anwenden, wenn das Objekt geöffnet ist, die **BeimLadenFiltern** -Eigenschaft auf true fest.</span><span class="sxs-lookup"><span data-stu-id="f7db2-125">In a client database, to automatically apply a filter when the object is opened, set the **FilterOnLoad** property to True.</span></span>

<span data-ttu-id="f7db2-126">Wenn Sie in einer Webdatenbank beim Öffnen eines Objekts automatisch einen Filter anwenden möchten, fügen Sie einem Makro die **FestlegenFilter** -Aktion hinzu, und fügen Sie das Makro dem **BeiLaden** -Ereignis des Objekts hinzu.</span><span class="sxs-lookup"><span data-stu-id="f7db2-126">In a web database, to automatically apply a filter when the object is opened, add the **SetFilter** action to a macro, and add the macro to the object's **OnLoad** event.</span></span>

## <a name="example"></a><span data-ttu-id="f7db2-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f7db2-127">Example</span></span>

<span data-ttu-id="f7db2-128">Das folgende Beispiel zeigt die Verwendung der Aktion SetFilter zum Filtern des Formulars, in dem das Makro definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f7db2-128">The following example shows how to use the SetFilter action to filter the form in which the macro is defined.</span></span>

<span data-ttu-id="f7db2-129">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="f7db2-129">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    SetFilter
        Filter Name
        Where Condtion =[display_name] Like "*cheese*"
        Control Name
```
