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
ms.openlocfilehash: aa029e3a81670746cdc467ddf7578c5900b58b29
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929034"
---
# <a name="sendkeys-macro-action"></a><span data-ttu-id="7a3fd-102">SendKeys-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="7a3fd-102">SendKeys macro action</span></span>


<span data-ttu-id="7a3fd-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7a3fd-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Sicherheitshinweis" alt="Security note" /><span data-ttu-id="7a3fd-105"><strong>Sicherheitshinweis</strong></span><span class="sxs-lookup"><span data-stu-id="7a3fd-105"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7a3fd-p101">
      Vermeiden Sie bei sensiblen oder vertraulichen Informationen die Verwendung der <strong>SendKeys</strong>-Anweisung oder eines AutoKeys-Makros. Ein bösartiger Benutzer könnte die Tastenfolgen abfangen und die Sicherheit Ihres Computers und Ihrer Daten gefährden.
</span><span class="sxs-lookup"><span data-stu-id="7a3fd-p101">Avoid using the <strong>SendKeys</strong> statement or an AutoKeys macro with sensitive or confidential information. A malicious user could intercept the keystrokes and compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7a3fd-108">Sie können die **Tastaturbefehle** -Aktion zum direkten Senden von Tastaturbefehlen an Microsoft Access oder an eine aktive Windows-basierte Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a3fd-108">You can use the **SendKeys** action to send keystrokes directly to Microsoft Access or to an active Windows-based application.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7a3fd-p102">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="7a3fd-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="7a3fd-111">Einstellung</span><span class="sxs-lookup"><span data-stu-id="7a3fd-111">Setting</span></span>

<span data-ttu-id="7a3fd-112">Die **Tastaturbefehle** -Aktion verwendet die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="7a3fd-112">The **SendKeys** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7a3fd-113">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="7a3fd-113">Action argument</span></span></p></th>
<th><p><span data-ttu-id="7a3fd-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a3fd-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a3fd-115"><strong>Tastaturbefehle</strong></span><span class="sxs-lookup"><span data-stu-id="7a3fd-115"><strong>Keystrokes</strong></span></span></p></td>
<td><p><span data-ttu-id="7a3fd-p103">Die Tastaturbefehle, die Access oder die Anwendung verarbeiten soll. Geben Sie die Tastaturbefehle im Feld Tastaturbefehle im Abschnitt Aktionsargumente im Bereichs Makro-Generator ein. Sie können bis zu 255 Zeichen eingeben. Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="7a3fd-p103">The keystrokes you want Access or the application to process. Enter the keystrokes in the <strong>Keystrokes</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can type up to 255 characters. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a3fd-120"><strong>Wait</strong></span><span class="sxs-lookup"><span data-stu-id="7a3fd-120"><strong>Wait</strong></span></span></p></td>
<td><p><span data-ttu-id="7a3fd-p104">Gibt an, ob das Makro angehalten werden soll, bis die Tastaturbefehle verarbeitet worden sind. Klicken Sie auf <strong>Ja</strong> (werden angehalten) oder <strong>Nein</strong> (werden nicht angehalten). Die Standardeinstellung ist <strong>Nein</strong>.</span><span class="sxs-lookup"><span data-stu-id="7a3fd-p104">Specifies whether the macro should pause until the keystrokes have been processed. Click <strong>Yes</strong> (to pause) or <strong>No</strong> (to not pause). The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7a3fd-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7a3fd-124">Remarks</span></span>

<span data-ttu-id="7a3fd-125">Access verarbeitet die Tastaturbefehle, die von der **Tastaturbefehle** -Aktion empfangen werden, als ob Sie diese direkt in einem Access-Fenster eingegeben hätten.</span><span class="sxs-lookup"><span data-stu-id="7a3fd-125">Access processes the keystrokes it receives through the **SendKeys** action exactly as if you had typed them directly in an Access window.</span></span>

<span data-ttu-id="7a3fd-126">Um die Tastaturbefehle anzugeben, verwenden Sie dieselbe Syntax wie für die Anweisung **Tastaturbefehle**.</span><span class="sxs-lookup"><span data-stu-id="7a3fd-126">To specify the keystrokes, use the same syntax as you would for the **SendKeys** statement.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7a3fd-127">[!HINWEIS] Ein Fehler kann auftreten, wenn das Argument <STRONG>Tastaturbefehle</STRONG> falsche Syntax, falsch geschriebenen Text oder andere Werte enthält, die für das Fenster nicht geeignet sind, an die die Tastaturbefehle gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a3fd-127">An error can occur if the <STRONG>Keystrokes</STRONG> argument contains incorrect syntax, misspelled text, or other values that aren't appropriate for the window the keystrokes are sent to.</span></span></P>



<span data-ttu-id="7a3fd-p105">Wenn Sie das Makro nicht unterbrechen möchten, um manuell auf das Dialogfeld zu reagieren, können Sie diese Aktion verwenden, um Informationen in einem Dialogfeld einzugeben. In bestimmten, häufig verwendeten Dialogfeldern werden die Optionen durch einige Access-Aktionen, wie **Drucken** und **SuchenDatensatz**, ausgewählt. Um die Optionen auch in weniger häufiger verwendeten Dialogfeldern auszuwählen, können Sie die **Tastaturbefehle** -Aktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a3fd-p105">You can use this action to enter information in a dialog box, particularly if you don't want to interrupt the macro to respond manually to the dialog box. Some Access actions, such as **PrintOut** and **FindRecord**, automatically select the options in certain frequently used dialog boxes. You can use the **SendKeys** action to select the options in less commonly used dialog boxes.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="7a3fd-131">Da das Dialogfeld das Makro unterbricht, müssen Sie die <STRONG>Tastaturbefehle</STRONG> -Aktion vor die Aktion stellen, die das Dialogfeld öffnet, und das Argument <STRONG>Warten</STRONG> auf <STRONG>Nein</STRONG> festlegen.</span><span class="sxs-lookup"><span data-stu-id="7a3fd-131">Because the dialog box suspends the macro, you must put the <STRONG>SendKeys</STRONG> action before the action that causes the dialog box to open and set the <STRONG>Wait</STRONG> argument to <STRONG>No</STRONG>.</span></span></P>
> <LI>
> <P><span data-ttu-id="7a3fd-p106">Der Zeitpunkt für die Tastaturbefehle, die Access oder eine andere Anwendung erreichen, kann ein Problem darstellen. Daher wird empfohlen, in den Fällen, in denen es eine andere Methode (wie die <STRONG>SuchenDatensatz</STRONG> -Aktion) zum Erzielen einer gewünschten Aufgabe gibt, diese statt der <STRONG>Tastaturbefehle</STRONG> -Aktion zur Auswahl der Optionen in einem Dialogfeld zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a3fd-p106">The timing of the keystrokes reaching Access or another application can be tricky. As a result, it's recommended that if there's some other method (such as the <STRONG>FindRecord</STRONG> action) you can use to achieve a desired task, use that method rather than using the <STRONG>SendKeys</STRONG> action to fill in the options in a dialog box.</span></span></P></LI></UL>



<span data-ttu-id="7a3fd-134">Wenn Sie mehr als 255 Zeichen an Access oder eine andere Windows-basierte Anwendung senden möchten, können Sie mehrere **Tastaturbefehle** -Aktionen in Folge in einem Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a3fd-134">If you want to send more than 255 characters to Access or another Windows-based application, you can use several **SendKeys** actions in succession in a macro.</span></span>

<span data-ttu-id="7a3fd-p107">Wenn die **Tastaturbefehle** -Aktion zum Senden von Tastaturbefehlen verwendet wird, wird das entsprechende Ereignis **KeyDown**, **KeyUp** und **KeyPress** ausgelöst. Wenn Nicht-ANSI-Tastaturbefehle gesendet werden (wie eine Funktionstaste), wird das **KeyPress** -Ereignis nicht ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="7a3fd-p107">Using the **SendKeys** action to send keystrokes triggers the appropriate **KeyDown**, **KeyUp**, and **KeyPress** events. Sending non-ANSI keystrokes (such as a function key) doesn't trigger the **KeyPress** event.</span></span>

<span data-ttu-id="7a3fd-p108">Diese Aktion ist in einem Modul für Visual Basic für Applikationen (VBA) nicht verfügbar. Verwenden Sie stattdessen die Anweisung **Tastaturbefehle**.</span><span class="sxs-lookup"><span data-stu-id="7a3fd-p108">This action isn't available from a Visual Basic for Applications (VBA) module. Use the **SendKeys** statement instead.</span></span>

