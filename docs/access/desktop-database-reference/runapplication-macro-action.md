---
title: RunApplication-Makroaktion
TOCTitle: RunApplication macro action
ms:assetid: 29967e6e-c441-b115-3ee6-2299b8a3bc25
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192038(v=office.15)
ms:contentKeyID: 48543885
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm93359
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2fcc3cc7bac9bcc4ab1f87c6e3da791eab06fc94
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919276"
---
# <a name="runapplication-macro-action"></a><span data-ttu-id="292d5-102">RunApplication-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="292d5-102">RunApplication macro action</span></span>


<span data-ttu-id="292d5-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="292d5-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Sicherheitshinweis" alt="Security note" /><span data-ttu-id="292d5-105"><strong>Sicherheitshinweis</strong></span><span class="sxs-lookup"><span data-stu-id="292d5-105"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="292d5-p101">Seien Sie mit der Ausführung von ausführbaren Dateien oder ausführbarem Code in Makros oder Anwendungen vorsichtig. Ausführbare Dateien oder ausführbarer Code können verwendet werden, um Aktionen auszuführen, welche die Sicherheit Ihres Computers und Ihrer Daten gefährden können.</span><span class="sxs-lookup"><span data-stu-id="292d5-p101">Use caution when running executable files or code in macros or applications. Executable files or code can be used to carry out actions that might compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="292d5-p102">Sie können die **AusführenAnwendung** -Aktion verwenden, um eine Microsoft Windows-basierte oder MS-DOS-basierte Anwendung, wie Microsoft Excel, Microsoft Word oder Microsoft PowerPoint, in Microsoft Access auszuführen. Sie können z. B. Excel-Tabellenkalkulationsdaten in Ihre Access-Datenbank einfügen.</span><span class="sxs-lookup"><span data-stu-id="292d5-p102">You can use the **RunApplication** action to run a Microsoft Windows-based or MS-DOS-based application, such as Microsoft Excel, Microsoft Word, or Microsoft PowerPoint, from within Microsoft Access. For example, you may want to paste Excel spreadsheet data into your Access database.</span></span>


> [!NOTE]
> <P><span data-ttu-id="292d5-p103">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="292d5-p103">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="292d5-112">Einstellung</span><span class="sxs-lookup"><span data-stu-id="292d5-112">Setting</span></span>

<span data-ttu-id="292d5-113">Die **AusführenAnwendung** -Aktion hat das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="292d5-113">The **RunApplication** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="292d5-114">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="292d5-114">Action argument</span></span></p></th>
<th><p><span data-ttu-id="292d5-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="292d5-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="292d5-116"><strong>Befehlszeile</strong></span><span class="sxs-lookup"><span data-stu-id="292d5-116"><strong>Command Line</strong></span></span></p></td>
<td><p><span data-ttu-id="292d5-p104">Die Befehlszeile, die zum Starten der Anwendung verwendet wird (einschließlich des Pfads und aller anderen erforderlichen Parameter wie Switches, mit denen die Anwendung in einem bestimmten Modus ausgeführt wird). Geben Sie die Befehlszeile im Feld Befehlszeile im Abschnitt Aktionsargumente des Bereichs Makro-Generator ein. Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="292d5-p104">The command line used to start the application (including the path and any other necessary parameters, such as switches that run the application in a particular mode). Enter the command line in the <strong>Command Line</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="292d5-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="292d5-120">Remarks</span></span>

<span data-ttu-id="292d5-p105">Die mit dieser Aktion ausgewählte Anwendung wird im Vordergrund ausgeführt. Das Makro, das diese Aktion enthält, wird nach dem Starten der Anwendung weiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="292d5-p105">The application selected with this action loads and runs in the foreground. The macro containing this action continues to run after starting the application.</span></span>

<span data-ttu-id="292d5-p106">Sie können Daten zwischen der anderen Anwendung und Access übertragen, indem Sie die Microsoft Windows-Funktion Dynamischer Datenaustausch (Dynamic Data Exchange, DDE) oder die Zwischenablage verwenden. Um Tastaturbefehle an eine andere Anwendung zu senden (obwohl DDE eine effizientere Methode für das Übertragen von Daten ist), können Sie die **Tastaturbefehle** -Aktion verwenden. Sie können Daten auch zwischen Anwendungen freigeben, indem Sie die Automatisierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="292d5-p106">You can transfer data between the other application and Access by using the Microsoft Windows dynamic data exchange (DDE) facility or the Clipboard. You can use the **SendKeys** action to send keystrokes to the other application (although DDE is a more efficient method for transferring data). You can also share data among applications by using automation.</span></span>

<span data-ttu-id="292d5-126">MS-DOS-basierte Anwendungen werden in einem MS-DOS-Fenster innerhalb der Windows-Umgebung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="292d5-126">MS-DOS-based applications run in an MS-DOS window within the Windows environment.</span></span>

<span data-ttu-id="292d5-127">In Windows-Betriebssystemen gibt es eine Reihe von Möglichkeiten, eine Anwendung auszuführen, u. a. Starten des Programms in Windows-Explorer, Verwenden des Befehls **Ausführen** im Menü **Start** und Doppelklicken auf ein Programmsymbol auf dem Windows- Desktop.</span><span class="sxs-lookup"><span data-stu-id="292d5-127">In Windows operating systems, there are a number of ways to run an application, including starting the program from the Windows Explorer, using the **Run** command on the **Start** menu, and double-clicking a program icon on the Windows Desktop.</span></span>

<span data-ttu-id="292d5-p107">Sie können die **AusführenAnwendung** -Aktion nicht in einem Modul für Visual Basic für Applikationen (VBA) ausführen. Verwenden Sie stattdessen die **Shell** -Funktion von VBA.</span><span class="sxs-lookup"><span data-stu-id="292d5-p107">You can't run the **RunApplication** action in a Visual Basic for Applications (VBA) module. Use the VBA **Shell** function instead.</span></span>

