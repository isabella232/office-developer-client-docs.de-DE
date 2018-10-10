---
title: WiederherstellenFenster-Makroaktion
TOCTitle: RestoreWindow Macro Action
ms:assetid: 507a6452-2be0-a523-1201-0108d2b9d23c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193815(v=office.15)
ms:contentKeyID: 48544796
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11103
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1dc6776310b0544b8bb807327612637a5fbcff67
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475607"
---
# <a name="restorewindow-macro-action"></a><span data-ttu-id="c6dc4-102">WiederherstellenFenster-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="c6dc4-102">RestoreWindow Macro Action</span></span>


<span data-ttu-id="c6dc4-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6dc4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c6dc4-104">Um die vorherige Größe eines maximierten oder minimierten Fensters wiederherzustellen, können Sie die **WiederherstellenFenster** -Aktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="c6dc4-104">You can use the **RestoreWindow** action to restore a maximized or minimized window to its previous size.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c6dc4-p101">[!HINWEIS] Diese Aktion kann auf Codefenster des Visual Basic-Editors nicht angewendet werden. Informationen zu den Auswirkungen auf Codefenster finden Sie im Thema zur <STRONG>WindowState</STRONG> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c6dc4-p101">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the <STRONG>WindowState</STRONG> property topic.</span></span></P>



## <a name="setting"></a><span data-ttu-id="c6dc4-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="c6dc4-107">Setting</span></span>

<span data-ttu-id="c6dc4-108">Die **WiederherstellenFenster** -Aktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="c6dc4-108">The **RestoreWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6dc4-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c6dc4-109">Remarks</span></span>

<span data-ttu-id="c6dc4-p102">Diese Aktion funktioniert für das ausgewählte Objekt. Wenn ein Objekt minimiert worden ist, können Sie es auswählen, indem Sie die **AuswählenObjekt** -Aktion verwenden, und dann seine vorherige Größe wiederherstellen, indem Sie die **WiederherstellenFenster** -Aktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="c6dc4-p102">This action works on the selected object. If an object has been minimized, you can first select it by using the **SelectObject** action and then restore it to its previous size by using the **RestoreWindow** action.</span></span>

<span data-ttu-id="c6dc4-112">Sie können die **VerschiebenUndGrößeÄndernFenster** -Aktion verwenden, um ein Fenster, das wiederhergestellt wurde, zu verschieben oder in der Größe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c6dc4-112">You can use the **MoveAndSizeWindow** action to move or size a window that you have restored.</span></span>

<span data-ttu-id="c6dc4-113">Die **WiederherstellenFenster** -Aktion hat dieselbe Wirkung wie ein Klicken auf die Schaltfläche **Wiederherstellen** in der rechten oberen Ecke des Fensters oder ein Klicken auf den Befehl **Wiederherstellen** im Fenstermenü **System**.</span><span class="sxs-lookup"><span data-stu-id="c6dc4-113">The **RestoreWindow** action has the same effect as clicking the **Restore** button in the window's upper-right corner or clicking the **Restore** command on the window's **Control** menu.</span></span>

<span data-ttu-id="c6dc4-114">Verwenden Sie die **Restore** -Methode des **DoCmd** -Objekts, um die **WiederherstellenFenster** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c6dc4-114">To run the **RestoreWindow** action in a Visual Basic for Applications (VBA) module, use the **Restore** method of the **DoCmd** object.</span></span>

