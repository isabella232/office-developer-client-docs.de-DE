---
title: MaximizeWindow-Makroaktion
TOCTitle: MaximizeWindow macro action
ms:assetid: 79c9e430-07a7-02b2-ff5a-c6b9ec32c5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196171(v=office.15)
ms:contentKeyID: 48545778
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm196948
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 452e676d3becb7f5f76587a970b71a42e4ec8ab2
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928649"
---
# <a name="maximizewindow-macro-action"></a><span data-ttu-id="1a5fc-102">MaximizeWindow-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="1a5fc-102">MaximizeWindow macro action</span></span>


<span data-ttu-id="1a5fc-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a5fc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1a5fc-104">Wenn überlappende Fenster anstelle von Dokumente im Registerkartenformat verwenden Zugriff konfiguriert ist, können Sie die **Maximierenfenster** -Aktion verwenden, um das aktive Fenster zu vergrößern, damit es das Access-Fenster ausfüllt.</span><span class="sxs-lookup"><span data-stu-id="1a5fc-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MaximizeWindow** action to enlarge the active window so that it fills the Access window.</span></span> <span data-ttu-id="1a5fc-105">Diese Aktion ermöglicht es Ihnen, so viel wie möglich vom Objekt im aktiven Fenster anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1a5fc-105">This action will allow you to see as much of the object in the active window as possible.</span></span>


> [!NOTE]
> <P><span data-ttu-id="1a5fc-p102">[!HINWEIS] Diese Aktion kann auf Codefenster des Visual Basic-Editors nicht angewendet werden. Informationen zu den Auswirkungen auf Codefenster finden Sie im Thema zur <STRONG>WindowState</STRONG> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1a5fc-p102">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the <STRONG>WindowState</STRONG> property topic.</span></span></P>



## <a name="setting"></a><span data-ttu-id="1a5fc-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="1a5fc-108">Setting</span></span>

<span data-ttu-id="1a5fc-109">Die **MaximierenFenster** -Aktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="1a5fc-109">The **MaximizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a5fc-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1a5fc-110">Remarks</span></span>

<span data-ttu-id="1a5fc-111">Diese Aktion hat dieselbe Wirkung wie das Klicken auf die Schaltfläche **Maximieren** in der oberen rechten Fensterecke oder klicken auf **Maximieren** im **Systemmenü des Fensters** .</span><span class="sxs-lookup"><span data-stu-id="1a5fc-111">This action has the same effect as clicking the **Maximize** button in the window's upper-right corner or clicking **Maximize** on the window's **Control** menu.</span></span>

<span data-ttu-id="1a5fc-112">Sie können die **WiederherstellenFenster** -Aktion verwenden, um ein maximiertes Fenster in seiner vorherigen Größe wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="1a5fc-112">You can use the **RestoreWindow** action to restore a maximized window to its previous size.</span></span>

<span data-ttu-id="1a5fc-113">**Tipps**</span><span class="sxs-lookup"><span data-stu-id="1a5fc-113">**Tips**</span></span>

  - <span data-ttu-id="1a5fc-114">Wenn das Fenster, das Sie maximieren möchten, nicht das aktive Fenster ist, müssen Sie die **AuswählenObjekt** -Aktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="1a5fc-114">You may need to use the **SelectObject** action if the window you want to maximize isn't the active window.</span></span>

  - <span data-ttu-id="1a5fc-p103">Wenn Sie ein Fenster in Access maximieren, werden alle anderen Fenster ebenfalls maximiert, wenn Sie sie öffnen oder zu diesen wechseln. Popupformulare werden jedoch nicht maximiert. Falls ein Formular seine Größe beibehalten soll, wenn andere Fenster maximiert werden, müssen Sie seine **PopUp** -Eigenschaft auf **Ja** festlegen.</span><span class="sxs-lookup"><span data-stu-id="1a5fc-p103">When you maximize a window in Access, all other windows are also maximized when you open them or switch to them. However, pop-up forms aren't maximized. If you want a form to maintain its size when other windows are maximized, set its **PopUp** property to **Yes**.</span></span>

<span data-ttu-id="1a5fc-118">Verwenden Sie die **Maximize** -Methode des **DoCmd** -Objekts, um die **MaximierenFenster** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1a5fc-118">To run the **MaximizeWindow** action in a Visual Basic for Applications module, use the **Maximize** method of the **DoCmd** object.</span></span>

