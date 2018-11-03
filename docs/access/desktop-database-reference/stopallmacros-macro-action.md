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
ms.openlocfilehash: 34dbfc3504744dd446a018e797ebacfb79066d96
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923350"
---
# <a name="stopallmacros-macro-action"></a><span data-ttu-id="0551c-102">StopAllMacros-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="0551c-102">StopAllMacros macro action</span></span>


<span data-ttu-id="0551c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0551c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0551c-104">Verwenden Sie die **StoppAlleMakros** -Aktion, um alle laufenden Makros zu beenden.</span><span class="sxs-lookup"><span data-stu-id="0551c-104">You can use the **StopAllMacros** action to stop all macros that are currently running.</span></span>

## <a name="setting"></a><span data-ttu-id="0551c-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="0551c-105">Setting</span></span>

<span data-ttu-id="0551c-106">Die **StoppAlleMakros** -Aktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="0551c-106">The **StopAllMacros** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="0551c-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0551c-107">Remarks</span></span>

<span data-ttu-id="0551c-108">Normalerweise verwenden Sie diese Aktion, wenn eine Fehlersituation das Beenden aller Makros erfordert.</span><span class="sxs-lookup"><span data-stu-id="0551c-108">You typically use this action when an error condition makes it necessary to stop all macros.</span></span> <span data-ttu-id="0551c-109">Sie können einen bedingten Ausdruck in der Aktionszeile des Makros verwenden, die diese Aktion enthält.</span><span class="sxs-lookup"><span data-stu-id="0551c-109">You can use a conditional expression in the macro's action row that contains this action.</span></span> <span data-ttu-id="0551c-110">Wenn der Ausdruck auf **True** (– 1) ausgewertet wird, beendet Microsoft Access alle Makros.</span><span class="sxs-lookup"><span data-stu-id="0551c-110">When the expression evaluates to **True** (–1), Microsoft Access stops all macros.</span></span>

<span data-ttu-id="0551c-p102">Angenommen, ein Makro zeigt im Rahmen einer Reihe komplexer Aktionen, einschließlich der Ausführung weiterer Makros, ein Meldungsfeld an. Wenn der Benutzer in diesem Meldungsfeld auf **Abbrechen** klickt, kann die **StoppAlleMakros** -Aktion alle laufenden Makros beenden.</span><span class="sxs-lookup"><span data-stu-id="0551c-p102">For example, you might have a macro that displays a message box as one of a number of complex actions, including running other macros. If the user clicks **Cancel** in this message box, the **StopAllMacros** action can stop all the macros that are running.</span></span>

<span data-ttu-id="0551c-113">Wenn ein Makro die Aktionen **Echo** oder **Warnmeldungen** zum Ausschalten von Echo oder der Anzeige von Systemmeldungen verwendet hat, werden sie mit der **StoppAlleMakros** -Aktion wieder eingeschaltet.</span><span class="sxs-lookup"><span data-stu-id="0551c-113">If a macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopAllMacros** action automatically turns them back on.</span></span>

<span data-ttu-id="0551c-114">Diese Aktion ist in einem VBA-Modul (Visual Basic für Applikationen) nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0551c-114">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

