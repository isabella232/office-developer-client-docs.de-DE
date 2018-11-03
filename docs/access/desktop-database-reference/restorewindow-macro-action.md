---
title: RestoreWindow-Makroaktion
TOCTitle: RestoreWindow macro action
ms:assetid: 507a6452-2be0-a523-1201-0108d2b9d23c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193815(v=office.15)
ms:contentKeyID: 48544796
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11103
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fb857e7eda7860150feb7af07babcc2574c3972f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929048"
---
# <a name="restorewindow-macro-action"></a><span data-ttu-id="ad1ce-102">RestoreWindow-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="ad1ce-102">RestoreWindow macro action</span></span>


<span data-ttu-id="ad1ce-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad1ce-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ad1ce-104">Um die vorherige Größe eines maximierten oder minimierten Fensters wiederherzustellen, können Sie die **WiederherstellenFenster** -Aktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-104">You can use the **RestoreWindow** action to restore a maximized or minimized window to its previous size.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ad1ce-p101">[!HINWEIS] Diese Aktion kann auf Codefenster des Visual Basic-Editors nicht angewendet werden. Informationen zu den Auswirkungen auf Codefenster finden Sie im Thema zur <STRONG>WindowState</STRONG> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-p101">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the <STRONG>WindowState</STRONG> property topic.</span></span></P>



## <a name="setting"></a><span data-ttu-id="ad1ce-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="ad1ce-107">Setting</span></span>

<span data-ttu-id="ad1ce-108">Die **WiederherstellenFenster** -Aktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-108">The **RestoreWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad1ce-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ad1ce-109">Remarks</span></span>

<span data-ttu-id="ad1ce-p102">Diese Aktion funktioniert für das ausgewählte Objekt. Wenn ein Objekt minimiert worden ist, können Sie es auswählen, indem Sie die **AuswählenObjekt** -Aktion verwenden, und dann seine vorherige Größe wiederherstellen, indem Sie die **WiederherstellenFenster** -Aktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-p102">This action works on the selected object. If an object has been minimized, you can first select it by using the **SelectObject** action and then restore it to its previous size by using the **RestoreWindow** action.</span></span>

<span data-ttu-id="ad1ce-112">Sie können die **VerschiebenUndGrößeÄndernFenster** -Aktion verwenden, um ein Fenster, das wiederhergestellt wurde, zu verschieben oder in der Größe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-112">You can use the **MoveAndSizeWindow** action to move or size a window that you have restored.</span></span>

<span data-ttu-id="ad1ce-113">Die **WiederherstellenFenster** -Aktion hat dieselbe Wirkung wie ein Klicken auf die Schaltfläche **Wiederherstellen** in der rechten oberen Ecke des Fensters oder ein Klicken auf den Befehl **Wiederherstellen** im Fenstermenü **System**.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-113">The **RestoreWindow** action has the same effect as clicking the **Restore** button in the window's upper-right corner or clicking the **Restore** command on the window's **Control** menu.</span></span>

<span data-ttu-id="ad1ce-114">Verwenden Sie die **Restore** -Methode des **DoCmd** -Objekts, um die **WiederherstellenFenster** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-114">To run the **RestoreWindow** action in a Visual Basic for Applications (VBA) module, use the **Restore** method of the **DoCmd** object.</span></span>

