---
title: StopAllMacros-Makroaktion
TOCTitle: StopAllMacros macro action
ms:assetid: 6afbf906-03b8-6e68-bbc9-7a4b141cf1c5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195440(v=office.15)
ms:contentKeyID: 48545442
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm104968
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4e44182dd4290b05a2cfc8fabdf9240819f4b7aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314476"
---
# <a name="stopallmacros-macro-action"></a><span data-ttu-id="83ba5-102">StopAllMacros-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="83ba5-102">StopAllMacros macro action</span></span>


<span data-ttu-id="83ba5-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="83ba5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="83ba5-104">Verwenden Sie die **StoppAlleMakros**-Aktion, um alle laufenden Makros zu beenden.</span><span class="sxs-lookup"><span data-stu-id="83ba5-104">You can use the **StopAllMacros** action to stop all macros that are currently running.</span></span>

## <a name="setting"></a><span data-ttu-id="83ba5-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="83ba5-105">Setting</span></span>

<span data-ttu-id="83ba5-106">Die **StoppAlleMakros**-Aktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="83ba5-106">The **StopAllMacros** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="83ba5-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83ba5-107">Remarks</span></span>

<span data-ttu-id="83ba5-p101">Normalerweise verwenden Sie diese Aktion, wenn eine Fehlersituation das Beenden aller Makros erfordert. Sie können einen bedingten Ausdruck in der Aktionszeile des Makros verwenden, die diese Aktion enthält. Wenn der Ausdruck als **Wahr** (–1) ausgewertet wird, beendet Microsoft Access alle Makros.</span><span class="sxs-lookup"><span data-stu-id="83ba5-p101">You typically use this action when an error condition makes it necessary to stop all macros. You can use a conditional expression in the macro's action row that contains this action. When the expression evaluates to **True** (–1), Microsoft Access stops all macros.</span></span>

<span data-ttu-id="83ba5-p102">Angenommen, ein Makro zeigt im Rahmen einer Reihe komplexer Aktionen, einschließlich der Ausführung weiterer Makros, ein Meldungsfeld an. Wenn der Benutzer in diesem Meldungsfeld auf **Abbrechen** klickt, kann die **StoppAlleMakros** -Aktion alle laufenden Makros beenden.</span><span class="sxs-lookup"><span data-stu-id="83ba5-p102">For example, you might have a macro that displays a message box as one of a number of complex actions, including running other macros. If the user clicks **Cancel** in this message box, the **StopAllMacros** action can stop all the macros that are running.</span></span>

<span data-ttu-id="83ba5-113">Wenn ein Makro die Aktionen **Echo** oder **Warnmeldungen** zum Ausschalten von Echo oder der Anzeige von Systemmeldungen verwendet hat, werden sie mit der **StoppAlleMakros** -Aktion wieder eingeschaltet.</span><span class="sxs-lookup"><span data-stu-id="83ba5-113">If a macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopAllMacros** action automatically turns them back on.</span></span>

<span data-ttu-id="83ba5-114">Diese Aktion ist in einem VBA-Modul (Visual Basic für Applikationen) nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="83ba5-114">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

