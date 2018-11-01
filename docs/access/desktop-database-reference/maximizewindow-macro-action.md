---
title: MaximierenFenster-Makroaktion
TOCTitle: MaximizeWindow Macro Action
ms:assetid: 79c9e430-07a7-02b2-ff5a-c6b9ec32c5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196171(v=office.15)
ms:contentKeyID: 48545778
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm196948
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 110262c9aee48fc24858150714194953136fa835
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867272"
---
# <a name="maximizewindow-macro-action"></a><span data-ttu-id="30702-102">MaximierenFenster-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="30702-102">MaximizeWindow Macro Action</span></span>


<span data-ttu-id="30702-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="30702-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="30702-104">Wenn überlappende Fenster anstelle von Dokumente im Registerkartenformat verwenden Zugriff konfiguriert ist, können Sie die **Maximierenfenster** -Aktion verwenden, um das aktive Fenster zu vergrößern, damit es das Access-Fenster ausfüllt.</span><span class="sxs-lookup"><span data-stu-id="30702-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MaximizeWindow** action to enlarge the active window so that it fills the Access window.</span></span> <span data-ttu-id="30702-105">Diese Aktion ermöglicht es Ihnen, so viel wie möglich vom Objekt im aktiven Fenster anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="30702-105">This action will allow you to see as much of the object in the active window as possible.</span></span>


> [!NOTE]
> <P><span data-ttu-id="30702-p102">[!HINWEIS] Diese Aktion kann auf Codefenster des Visual Basic-Editors nicht angewendet werden. Informationen zu den Auswirkungen auf Codefenster finden Sie im Thema zur <STRONG>WindowState</STRONG> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="30702-p102">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the <STRONG>WindowState</STRONG> property topic.</span></span></P>



## <a name="setting"></a><span data-ttu-id="30702-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="30702-108">Setting</span></span>

<span data-ttu-id="30702-109">Die **MaximierenFenster** -Aktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="30702-109">The **MaximizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="30702-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="30702-110">Remarks</span></span>

<span data-ttu-id="30702-111">Diese Aktion hat dieselbe Wirkung wie das Klicken auf die Schaltfläche **Maximieren** in der oberen rechten Fensterecke oder klicken auf **Maximieren** im **Systemmenü des Fensters** .</span><span class="sxs-lookup"><span data-stu-id="30702-111">This action has the same effect as clicking the **Maximize** button in the window's upper-right corner or clicking **Maximize** on the window's **Control** menu.</span></span>

<span data-ttu-id="30702-112">Sie können die **WiederherstellenFenster** -Aktion verwenden, um ein maximiertes Fenster in seiner vorherigen Größe wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="30702-112">You can use the **RestoreWindow** action to restore a maximized window to its previous size.</span></span>

<span data-ttu-id="30702-113">**Tipps**</span><span class="sxs-lookup"><span data-stu-id="30702-113">**Tips**</span></span>

  - <span data-ttu-id="30702-114">Wenn das Fenster, das Sie maximieren möchten, nicht das aktive Fenster ist, müssen Sie die **AuswählenObjekt** -Aktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="30702-114">You may need to use the **SelectObject** action if the window you want to maximize isn't the active window.</span></span>

  - <span data-ttu-id="30702-p103">Wenn Sie ein Fenster in Access maximieren, werden alle anderen Fenster ebenfalls maximiert, wenn Sie sie öffnen oder zu diesen wechseln. Popupformulare werden jedoch nicht maximiert. Falls ein Formular seine Größe beibehalten soll, wenn andere Fenster maximiert werden, müssen Sie seine **PopUp** -Eigenschaft auf **Ja** festlegen.</span><span class="sxs-lookup"><span data-stu-id="30702-p103">When you maximize a window in Access, all other windows are also maximized when you open them or switch to them. However, pop-up forms aren't maximized. If you want a form to maintain its size when other windows are maximized, set its **PopUp** property to **Yes**.</span></span>

<span data-ttu-id="30702-118">Verwenden Sie die **Maximize** -Methode des **DoCmd** -Objekts, um die **MaximierenFenster** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="30702-118">To run the **MaximizeWindow** action in a Visual Basic for Applications module, use the **Maximize** method of the **DoCmd** object.</span></span>

