---
title: PrintOut-Makroaktion
TOCTitle: PrintOut macro action
ms:assetid: 13688158-1cf1-4b2e-d90a-271c8890e413
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845432(v=office.15)
ms:contentKeyID: 48543368
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm1697
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 04212a8bf63d5039c6548463612f006f0d116229
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301407"
---
# <a name="printout-macro-action"></a><span data-ttu-id="bd424-102">PrintOut-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="bd424-102">PrintOut macro action</span></span>

<span data-ttu-id="bd424-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd424-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bd424-p101">Zum Drucken des aktiven Objekts in der geöffneten Datenbank können Sie die **Drucken** -Aktion verwenden. Sie können Datenblätter, Berichte, Formulare, Datenzugriffsseiten und Module drucken.</span><span class="sxs-lookup"><span data-stu-id="bd424-p101">You can use the **PrintOut** action to print the active object in the open database. You can print datasheets, reports, forms, data access pages, and modules.</span></span>

> [!NOTE]
> <span data-ttu-id="bd424-106">Diese Aktion ist nicht zulässig, wenn die Datenbank nicht vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="bd424-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="bd424-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="bd424-107">Setting</span></span>

<span data-ttu-id="bd424-108">Die **Drucken**-Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="bd424-108">The **PrintOut** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd424-109">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="bd424-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="bd424-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd424-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd424-111"><strong>Druckbereich</strong></span><span class="sxs-lookup"><span data-stu-id="bd424-111"><strong>Print Range</strong></span></span></p></td>
<td><p><span data-ttu-id="bd424-112">Der zu druckende Range.</span><span class="sxs-lookup"><span data-stu-id="bd424-112">The range to print.</span></span> <span data-ttu-id="bd424-113">Klicken Sie auf <strong>alle</strong> (der Benutzer kann das gesamte Objekt drucken), <strong>Auswahl</strong> (der Benutzer kann den Teil des ausgewählten Objekts drucken) oder <strong>Seiten</strong> (der Benutzer kann einen Bereich von Seiten in der <strong>Seite von</strong> und <strong>auf Seiten zu</strong> Argumenten angeben) in der <strong> Feld Druckbereich</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs Makro-Generator.</span><span class="sxs-lookup"><span data-stu-id="bd424-113">Click <strong>All</strong> (the user can print all of the object), <strong>Selection</strong> (the user can print the part of the object that's selected), or <strong>Pages</strong> (the user can specify a range of pages in the <strong>Page From</strong> and <strong>Page To</strong> arguments) in the <strong>Print Range</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="bd424-114">Die Standardeinstellung ist <strong>Alle</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd424-114">The default is <strong>All</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd424-115"><strong>Von</strong></span><span class="sxs-lookup"><span data-stu-id="bd424-115"><strong>Page From</strong></span></span></p></td>
<td><p><span data-ttu-id="bd424-p103">Die erste zu druckende Seite. Der Druckvorgang wird am Anfang dieser Seite gestartet. Dieses Argument ist erforderlich, wenn Sie im Feld <strong>Druckbereich</strong> die Option <strong>Seiten</strong> auswählen.</span><span class="sxs-lookup"><span data-stu-id="bd424-p103">The first page to print. Printing starts at the top of this page. This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd424-119"><strong>Bis</strong></span><span class="sxs-lookup"><span data-stu-id="bd424-119"><strong>Page To</strong></span></span></p></td>
<td><p><span data-ttu-id="bd424-p104">Die letzte zu druckende Seite. Der Druckvorgang wird unten auf dieser Seite beendet. Dieses Argument ist erforderlich, wenn Sie im Feld <strong>Druckbereich</strong> die Option <strong>Seiten</strong> auswählen.</span><span class="sxs-lookup"><span data-stu-id="bd424-p104">The last page to print. Printing stops at the bottom of this page. This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd424-123"><strong>Druckqualität</strong></span><span class="sxs-lookup"><span data-stu-id="bd424-123"><strong>Print Quality</strong></span></span></p></td>
<td><p><span data-ttu-id="bd424-124">Die Qualität des Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="bd424-124">The print quality.</span></span> <span data-ttu-id="bd424-125">Klicken Sie auf <strong>Hoch</strong>, <strong>Mittel</strong>, <strong>Niedrig</strong> oder <strong>Entwurf</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd424-125">Click <strong>High</strong>, <strong>Medium</strong>, <strong>Low</strong>, or <strong>Draft</strong>.</span></span> <span data-ttu-id="bd424-126">Je niedriger die Qualität, desto schneller wird das Objekt gedruckt.</span><span class="sxs-lookup"><span data-stu-id="bd424-126">The lower the quality, the faster the object prints.</span></span> <span data-ttu-id="bd424-127">Die Standardeinstellung ist <strong>Hoch</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd424-127">The default is <strong>High</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd424-128"><strong>Copies</strong></span><span class="sxs-lookup"><span data-stu-id="bd424-128"><strong>Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="bd424-129">Die Anzahl der zu druckenden Exemplare.</span><span class="sxs-lookup"><span data-stu-id="bd424-129">The number of copies to print.</span></span> <span data-ttu-id="bd424-130">Die Standardeinstellung ist 1.</span><span class="sxs-lookup"><span data-stu-id="bd424-130">The default is 1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd424-131"><strong>Exemplare sortieren</strong></span><span class="sxs-lookup"><span data-stu-id="bd424-131"><strong>Collate Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="bd424-p107">Klicken Sie auf <strong>Ja</strong> (gedruckte Exemplare sortieren) oder <strong>Nein</strong> (Exemplare nicht sortieren). Das Objekt wird möglicherweise schneller gedruckt, wenn dieses Argument auf <strong>Nein</strong> festgelegt wird. Die Standardeinstellung ist <strong>Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd424-p107">Click <strong>Yes</strong> (collate the printed copies) or <strong>No</strong> (do not collate copies). The object may print faster if this argument is set to <strong>No</strong>. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="bd424-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd424-135">Remarks</span></span>

<span data-ttu-id="bd424-p108">Diese Aktion ist mit dem Auswählen eines Objekts, dem Klicken auf die Registerkarte **Datei** und dann dem Klicken auf **Drucken** vergleichbar. Mit dieser Aktion wird jedoch kein Dialogfeld **Drucken** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bd424-p108">This action is similar to selecting an object, clicking the **File** tab and then clicking **Print**. With this action, however, no **Print** dialog box appears.</span></span>

> [!TIP]
> <span data-ttu-id="bd424-138">[!TIPP] Erstellen Sie ein Makro mit einer **Drucken** -Aktion mit diesen Einstellungen in den Argumenten, wenn Sie bestimmte Druckeinstellungen häufig verwenden.</span><span class="sxs-lookup"><span data-stu-id="bd424-138">If you have particular print settings you use frequently, create a macro containing a **PrintOut** action with these settings in its arguments.</span></span>

<span data-ttu-id="bd424-p109">Die Argumente für diese Aktion entsprechen den Optionen im Dialogfeld **Drucken**. Im Gegensatz zur **SuchenDatensatz** -Aktion und dem Dialogfeld **Suchen und Ersetzen** werden die Argumenteinstellungen nicht mit den Optionen des Dialogfelds **Drucken** gemeinsam verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd424-p109">The arguments for this action correspond to options in the **Print** dialog box. However, unlike the **FindRecord** action and **Find and Replace** dialog box, the argument settings aren't shared with the **Print** dialog box options.</span></span>

<span data-ttu-id="bd424-141">Verwenden Sie die **PrintOut** -Methode des **DoCmd** -Objekts, um die **Drucken** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="bd424-141">To run the **PrintOut** action in a Visual Basic for Applications (VBA) module, use the **PrintOut** method of the **DoCmd** object.</span></span>

