---
title: SendKeys-Makroaktion
TOCTitle: SendKeys macro action
ms:assetid: 3b06fcfc-ea64-c780-b5fc-6fc72853f524
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192656(v=office.15)
ms:contentKeyID: 48544275
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm183441
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f8c45cdf0d9cf588f61d1b51b728a8a15f6d7e12
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308750"
---
# <a name="sendkeys-macro-action"></a><span data-ttu-id="dca3e-102">SendKeys-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="dca3e-102">SendKeys macro action</span></span>

<span data-ttu-id="dca3e-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dca3e-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Sicherheitshinweis" alt="Security note" /><span data-ttu-id="dca3e-105"><strong>Sicherheitshinweis</strong></span><span class="sxs-lookup"><span data-stu-id="dca3e-105"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dca3e-p101">Vermeiden Sie die <strong>SendKeys</strong>-Anweisung oder ein AutoKeys-Makro mit sensiblen oder vertraulichen Informationen. Ein böswilliger Benutzer kann die Tastatureingaben abfangen und die Sicherheit von Computer und Daten gefährden.</span><span class="sxs-lookup"><span data-stu-id="dca3e-p101">Avoid using the <strong>SendKeys</strong> statement or an AutoKeys macro with sensitive or confidential information. A malicious user could intercept the keystrokes and compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dca3e-108">Sie können die **Tastaturbefehle** -Aktion zum direkten Senden von Tastaturbefehlen an Microsoft Access oder an eine aktive Windows-basierte Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="dca3e-108">You can use the **SendKeys** action to send keystrokes directly to Microsoft Access or to an active Windows-based application.</span></span>

> [!NOTE]
> <span data-ttu-id="dca3e-109">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="dca3e-109">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="dca3e-110">Einstellung</span><span class="sxs-lookup"><span data-stu-id="dca3e-110">Setting</span></span>

<span data-ttu-id="dca3e-111">Die **Tastaturbefehle**-Aktion verwendet die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="dca3e-111">The **SendKeys** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dca3e-112">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="dca3e-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="dca3e-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dca3e-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dca3e-114"><strong>Anschläge</strong></span><span class="sxs-lookup"><span data-stu-id="dca3e-114"><strong>Keystrokes</strong></span></span></p></td>
<td><p><span data-ttu-id="dca3e-115">Die Tastenkombinationen, die der Zugriff oder die Anwendung verarbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="dca3e-115">The keystrokes you want Access or the application to process.</span></span> <span data-ttu-id="dca3e-116">Geben Sie die Tastenkombinationen im Feld <strong>Tastenkombinationen</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs Makro-Generator ein.</span><span class="sxs-lookup"><span data-stu-id="dca3e-116">Enter the keystrokes in the <strong>Keystrokes</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="dca3e-117">Sie können bis zu 255 Zeichen eingeben.</span><span class="sxs-lookup"><span data-stu-id="dca3e-117">You can type up to 255 characters.</span></span> <span data-ttu-id="dca3e-118">Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="dca3e-118">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dca3e-119"><strong>Wait</strong></span><span class="sxs-lookup"><span data-stu-id="dca3e-119"><strong>Wait</strong></span></span></p></td>
<td><p><span data-ttu-id="dca3e-p103">Gibt an, ob das Makro angehalten werden soll, bis die Tastaturbefehle verarbeitet worden sind. Klicken Sie auf <strong>Ja</strong> (werden angehalten) oder <strong>Nein</strong> (werden nicht angehalten). Die Standardeinstellung ist <strong>Nein</strong>.</span><span class="sxs-lookup"><span data-stu-id="dca3e-p103">Specifies whether the macro should pause until the keystrokes have been processed. Click <strong>Yes</strong> (to pause) or <strong>No</strong> (to not pause). The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="dca3e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dca3e-123">Remarks</span></span>

<span data-ttu-id="dca3e-124">Access verarbeitet die Tastaturbefehle, die von der **Tastaturbefehle**-Aktion empfangen werden, als ob Sie diese direkt in einem Access-Fenster eingegeben hätten.</span><span class="sxs-lookup"><span data-stu-id="dca3e-124">Access processes the keystrokes it receives through the **SendKeys** action exactly as if you had typed them directly in an Access window.</span></span>

<span data-ttu-id="dca3e-125">Um die Tastaturbefehle anzugeben, verwenden Sie dieselbe Syntax wie für die Anweisung **Tastaturbefehle**.</span><span class="sxs-lookup"><span data-stu-id="dca3e-125">To specify the keystrokes, use the same syntax as you would for the **SendKeys** statement.</span></span>

> [!NOTE]
> <span data-ttu-id="dca3e-126">[!HINWEIS] Ein Fehler kann auftreten, wenn das Argument **Tastaturbefehle** falsche Syntax, falsch geschriebenen Text oder andere Werte enthält, die für das Fenster nicht geeignet sind, an die die Tastaturbefehle gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="dca3e-126">An error can occur if the **Keystrokes** argument contains incorrect syntax, misspelled text, or other values that aren't appropriate for the window the keystrokes are sent to.</span></span>

<span data-ttu-id="dca3e-p104">Wenn Sie das Makro nicht unterbrechen möchten, um manuell auf das Dialogfeld zu reagieren, können Sie diese Aktion verwenden, um Informationen in einem Dialogfeld einzugeben. In bestimmten, häufig verwendeten Dialogfeldern werden die Optionen durch einige Access-Aktionen, wie **Drucken** und **SuchenDatensatz**, ausgewählt. Um die Optionen auch in weniger häufiger verwendeten Dialogfeldern auszuwählen, können Sie die **Tastaturbefehle** -Aktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="dca3e-p104">You can use this action to enter information in a dialog box, particularly if you don't want to interrupt the macro to respond manually to the dialog box. Some Access actions, such as **PrintOut** and **FindRecord**, automatically select the options in certain frequently used dialog boxes. You can use the **SendKeys** action to select the options in less commonly used dialog boxes.</span></span>

> [!NOTE]
> - <span data-ttu-id="dca3e-130">Da das Dialogfeld das Makro unterbricht, müssen Sie die **Tastaturbefehle** -Aktion vor die Aktion stellen, die das Dialogfeld öffnet, und das Argument **Warten** auf **Nein** festlegen.</span><span class="sxs-lookup"><span data-stu-id="dca3e-130">Because the dialog box suspends the macro, you must put the **SendKeys** action before the action that causes the dialog box to open and set the **Wait** argument to **No**.</span></span>
> - <span data-ttu-id="dca3e-p105">Der Zeitpunkt für die Tastaturbefehle, die Access oder eine andere Anwendung erreichen, kann ein Problem darstellen. Daher wird empfohlen, in den Fällen, in denen es eine andere Methode (wie die **SuchenDatensatz** -Aktion) zum Erzielen einer gewünschten Aufgabe gibt, diese statt der **Tastaturbefehle** -Aktion zur Auswahl der Optionen in einem Dialogfeld zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="dca3e-p105">The timing of the keystrokes reaching Access or another application can be tricky. As a result, it's recommended that if there's some other method (such as the **FindRecord** action) you can use to achieve a desired task, use that method rather than using the **SendKeys** action to fill in the options in a dialog box.</span></span>

<span data-ttu-id="dca3e-133">Wenn Sie mehr als 255 Zeichen an Access oder eine andere Windows-basierte Anwendung senden möchten, können Sie mehrere **Tastaturbefehle** -Aktionen in Folge in einem Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="dca3e-133">If you want to send more than 255 characters to Access or another Windows-based application, you can use several **SendKeys** actions in succession in a macro.</span></span>

<span data-ttu-id="dca3e-p106">Wenn die **Tastaturbefehle** -Aktion zum Senden von Tastaturbefehlen verwendet wird, wird das entsprechende Ereignis **KeyDown**, **KeyUp** und **KeyPress** ausgelöst. Wenn Nicht-ANSI-Tastaturbefehle gesendet werden (wie eine Funktionstaste), wird das **KeyPress** -Ereignis nicht ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="dca3e-p106">Using the **SendKeys** action to send keystrokes triggers the appropriate **KeyDown**, **KeyUp**, and **KeyPress** events. Sending non-ANSI keystrokes (such as a function key) doesn't trigger the **KeyPress** event.</span></span>

<span data-ttu-id="dca3e-p107">Diese Aktion ist in einem Modul für Visual Basic für Applikationen (VBA) nicht verfügbar. Verwenden Sie stattdessen die Anweisung **Tastaturbefehle**.</span><span class="sxs-lookup"><span data-stu-id="dca3e-p107">This action isn't available from a Visual Basic for Applications (VBA) module. Use the **SendKeys** statement instead.</span></span>

