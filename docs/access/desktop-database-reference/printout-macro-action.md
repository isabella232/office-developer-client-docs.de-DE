---
title: Drucken-Makroaktion
TOCTitle: PrintOut Macro Action
ms:assetid: 13688158-1cf1-4b2e-d90a-271c8890e413
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845432(v=office.15)
ms:contentKeyID: 48543368
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm1697
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6a0aa0ae6d992410d5bed6126bfe49d7e84e9135
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878731"
---
# <a name="printout-macro-action"></a><span data-ttu-id="8e5bd-102">Drucken-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="8e5bd-102">PrintOut Macro Action</span></span>


<span data-ttu-id="8e5bd-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e5bd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8e5bd-p101">Zum Drucken des aktiven Objekts in der geöffneten Datenbank können Sie die **Drucken** -Aktion verwenden. Sie können Datenblätter, Berichte, Formulare, Datenzugriffsseiten und Module drucken.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-p101">You can use the **PrintOut** action to print the active object in the open database. You can print datasheets, reports, forms, data access pages, and modules.</span></span>


> [!NOTE]
> <P><span data-ttu-id="8e5bd-p102">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="8e5bd-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="8e5bd-108">Setting</span></span>

<span data-ttu-id="8e5bd-109">Die **Drucken** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-109">The **PrintOut** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8e5bd-110">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="8e5bd-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="8e5bd-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e5bd-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e5bd-112"><strong>Druckbereich</strong></span><span class="sxs-lookup"><span data-stu-id="8e5bd-112"><strong>Print Range</strong></span></span></p></td>
<td><p><span data-ttu-id="8e5bd-p103">Der zu druckende Bereich. Klicken Sie im Feld Druckbereich im Abschnitt Aktionsargumente des Bereichs Makro-Generator auf Alle (der Benutzer kann alle Objekte drucken), auf Markierung (der Benutzer kann den Teil des Objekts drucken, der markiert ist) oder auf Seite (der Benutzer kann einen Seitenbereich mit den Argumenten Von und Bis angeben). Die Standardeinstellung ist Alle.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-p103">The range to print. Click <strong>All</strong> (the user can print all of the object), <strong>Selection</strong> (the user can print the part of the object that's selected), or <strong>Pages</strong> (the user can specify a range of pages in the <strong>Page From</strong> and <strong>Page To</strong> arguments) in the <strong>Print Range</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>All</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e5bd-116"><strong>Von</strong></span><span class="sxs-lookup"><span data-stu-id="8e5bd-116"><strong>Page From</strong></span></span></p></td>
<td><p><span data-ttu-id="8e5bd-p104">Die erste zu druckende Seite. Der Druckvorgang wird am Anfang dieser Seite gestartet. Dieses Argument ist erforderlich, wenn Sie im Feld <strong>Druckbereich</strong> die Option <strong>Seiten</strong> auswählen.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-p104">The first page to print. Printing starts at the top of this page. This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e5bd-120"><strong>Bis</strong></span><span class="sxs-lookup"><span data-stu-id="8e5bd-120"><strong>Page To</strong></span></span></p></td>
<td><p><span data-ttu-id="8e5bd-p105">Die letzte zu druckende Seite. Der Druckvorgang wird unten auf dieser Seite beendet. Dieses Argument ist erforderlich, wenn Sie im Feld <strong>Druckbereich</strong> die Option <strong>Seiten</strong> auswählen.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-p105">The last page to print. Printing stops at the bottom of this page. This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e5bd-124"><strong>Druckqualität</strong></span><span class="sxs-lookup"><span data-stu-id="8e5bd-124"><strong>Print Quality</strong></span></span></p></td>
<td><p><span data-ttu-id="8e5bd-p106">Die Qualität des Ausdrucks. Klicken Sie auf <strong>Hoch</strong>, <strong>Mittel</strong>, <strong>Niedrig</strong> oder <strong>Entwurf</strong>. Je niedriger die Qualität, desto schneller wird das Objekt gedruckt. Die Standardeinstellung ist <strong>Hoch</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-p106">The print quality. Click <strong>High</strong>, <strong>Medium</strong>, <strong>Low</strong>, or <strong>Draft</strong>. The lower the quality, the faster the object prints. The default is <strong>High</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e5bd-129"><strong>Copies</strong></span><span class="sxs-lookup"><span data-stu-id="8e5bd-129"><strong>Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="8e5bd-p107">Die Anzahl der zu druckenden Exemplare. Die Standardeinstellung ist 1.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-p107">The number of copies to print. The default is 1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e5bd-132"><strong>Exemplare sortieren</strong></span><span class="sxs-lookup"><span data-stu-id="8e5bd-132"><strong>Collate Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="8e5bd-p108">Klicken Sie auf <strong>Ja</strong> (gedruckte Exemplare sortieren) oder <strong>Nein</strong> (Exemplare nicht sortieren). Das Objekt wird möglicherweise schneller gedruckt, wenn dieses Argument auf <strong>Nein</strong> festgelegt wird. Die Standardeinstellung ist <strong>Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-p108">Click <strong>Yes</strong> (collate the printed copies) or <strong>No</strong> (do not collate copies). The object may print faster if this argument is set to <strong>No</strong>. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8e5bd-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8e5bd-136">Remarks</span></span>

<span data-ttu-id="8e5bd-p109">Diese Aktion ist mit dem Auswählen eines Objekts, dem Klicken auf die Registerkarte **Datei** und dann dem Klicken auf **Drucken** vergleichbar. Mit dieser Aktion wird jedoch kein Dialogfeld **Drucken** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-p109">This action is similar to selecting an object, clicking the **File** tab and then clicking **Print**. With this action, however, no **Print** dialog box appears.</span></span>


> [!TIP]
> <P><span data-ttu-id="8e5bd-139">[!TIPP] Erstellen Sie ein Makro mit einer <STRONG>Drucken</STRONG> -Aktion mit diesen Einstellungen in den Argumenten, wenn Sie bestimmte Druckeinstellungen häufig verwenden.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-139">If you have particular print settings you use frequently, create a macro containing a <STRONG>PrintOut</STRONG> action with these settings in its arguments.</span></span></P>



<span data-ttu-id="8e5bd-p110">Die Argumente für diese Aktion entsprechen den Optionen im Dialogfeld **Drucken**. Im Gegensatz zur **SuchenDatensatz** -Aktion und dem Dialogfeld **Suchen und Ersetzen** werden die Argumenteinstellungen nicht mit den Optionen des Dialogfelds **Drucken** gemeinsam verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-p110">The arguments for this action correspond to options in the **Print** dialog box. However, unlike the **FindRecord** action and **Find and Replace** dialog box, the argument settings aren't shared with the **Print** dialog box options.</span></span>

<span data-ttu-id="8e5bd-142">Verwenden Sie die **PrintOut** -Methode des **DoCmd** -Objekts, um die **Drucken** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-142">To run the **PrintOut** action in a Visual Basic for Applications (VBA) module, use the **PrintOut** method of the **DoCmd** object.</span></span>

