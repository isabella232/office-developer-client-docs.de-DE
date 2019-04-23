---
title: MinimizeWindow-Makroaktion
TOCTitle: MinimizeWindow macro action
ms:assetid: 3a92b654-15ce-1ed1-63e0-eed927dbe26c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192648(v=office.15)
ms:contentKeyID: 48544265
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm174420
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9f7c4ab535010dc0329673fd04721615f6eb3cd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288883"
---
# <a name="minimizewindow-macro-action"></a><span data-ttu-id="eb4cb-102">MinimizeWindow-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="eb4cb-102">MinimizeWindow macro action</span></span>

<span data-ttu-id="eb4cb-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb4cb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eb4cb-104">Wenn der Zugriff auf überlappende Fenster anstelle von Dokumenten im Registerkartenformat konfiguriert ist, können Sie die **minimierenfenster** -Aktion verwenden, um das aktive Fenster auf eine kleine Titelleiste am unteren Rand des Access-Fensters zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="eb4cb-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MinimizeWindow** action to reduce the active window to a small title bar at the bottom of the Access window.</span></span>

> [!NOTE]
> <span data-ttu-id="eb4cb-p101">Diese Aktion kann auf Codefenster des Visual Basic-Editors nicht angewendet werden. Informationen zu den Auswirkungen auf Codefenster finden Sie im Thema zur **WindowState**-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="eb4cb-p101">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the **WindowState** property topic.</span></span>

## <a name="setting"></a><span data-ttu-id="eb4cb-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="eb4cb-107">Setting</span></span>

<span data-ttu-id="eb4cb-108">Die **MinimierenFenster**-Aktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="eb4cb-108">The **MinimizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb4cb-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb4cb-109">Remarks</span></span>

<span data-ttu-id="eb4cb-p102">Sie können diese Aktion verwenden, um ein Fenster vom Bildschirm zu entfernen, während das Objekt geöffnet bleibt. Sie können diese Aktion auch verwenden, um ein Objekt zu öffnen, ohne sein Fenster anzuzeigen. Zum Anzeigen des Objekts verwenden Sie die **AuswählenObjekt** -Aktion mit der Aktion **MaximierenFenster** oder **WiederherstellenFenster**. Durch die **WiederherstellenFenster** -Aktion wird ein minimiertes Fenster in seiner vorherigen Größe wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="eb4cb-p102">You can use this action to remove a window from the screen while leaving the object open. You can also use this action to open an object without displaying its window. To display the object, use the **SelectObject** action with either the **MaximizeWindow** or **RestoreWindow** action. The **RestoreWindow** action restores a minimized window to its previous size.</span></span>

<span data-ttu-id="eb4cb-114">The **MinimizeWindow** action has the same effect as clicking the **Minimize** button in the window's upper-right corner or clicking **Minimize** on the window's **Control** menu.</span><span class="sxs-lookup"><span data-stu-id="eb4cb-114">The **MinimizeWindow** action has the same effect as clicking the **Minimize** button in the window's upper-right corner or clicking **Minimize** on the window's **Control** menu.</span></span>

<span data-ttu-id="eb4cb-115">**Tipps**</span><span class="sxs-lookup"><span data-stu-id="eb4cb-115">**Tips**</span></span>

- <span data-ttu-id="eb4cb-116">Wenn das Fenster, das Sie minimieren möchten, nicht das aktive Fenster ist, müssen Sie zuerst die **AuswählenObjekt** -Aktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="eb4cb-116">You may first need to use the **SelectObject** action if the window you want to minimize isn't the active window.</span></span>

- <span data-ttu-id="eb4cb-p103">To hide the Navigation Pane, use the **SelectObject** action with the In Navigation Pane argument set to **Yes** and then use the **MinimizeWindow** action. The object you select in the **SelectObject** action can be any object in the database.</span><span class="sxs-lookup"><span data-stu-id="eb4cb-p103">To hide the Navigation Pane, use the **SelectObject** action with the In Navigation Pane argument set to **Yes** and then use the **MinimizeWindow** action. The object you select in the **SelectObject** action can be any object in the database.</span></span>

- <span data-ttu-id="eb4cb-p104">Sie können das aktive Fenster ausblenden, indem Sie auf im Menü **Ansicht** auf **Dieses Fenster verwalten**und dann auf **Ausblenden** klicken. Anstatt auf die Größe eines Symbols verkleinert zu werden, wird das Fenster in diesem Fall unsichtbar. Verwenden Sie den Befehl **Einblenden** im gleichen Menü, damit das Fenster wieder angezeigt wird. Mithilfe der **AusführenMenübefehl** -Aktion können Sie jeden dieser Befehle auch in einem Makro ausführen.</span><span class="sxs-lookup"><span data-stu-id="eb4cb-p104">You can hide the active window by clicking **Manage This Window** on the **View** menu, and then clicking **Hide**. Instead of being reduced to an icon, the window becomes invisible. Use the **Unhide** command on the same menu to make the window reappear. You can use the **RunMenuCommand** action to carry out either of these commands from a macro.</span></span>

- <span data-ttu-id="eb4cb-123">Sie können auch die **SetzenWert** -Aktion verwenden, um die **Sichtbar**-Eigenschaft eines Formulars so festzulegen, dass das Fenster des Formulars ausgeblendet oder angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="eb4cb-123">You can also use the **SetValue** action to set a form's **Visible** property to hide or show the form's window.</span></span>

<span data-ttu-id="eb4cb-124">Verwenden Sie die **Minimize** -Methode des **DoCmd** -Objekts, um die **MinimierenFenster** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="eb4cb-124">To run the **MinimizeWindow** action in a Visual Basic for Applications (VBA) module, use the **Minimize** method of the **DoCmd** object.</span></span>

