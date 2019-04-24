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
localization_priority: Normal
ms.openlocfilehash: 35637781035b7a449ba574cf5f6c84f2cb5223db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306587"
---
# <a name="restorewindow-macro-action"></a><span data-ttu-id="43ef8-102">RestoreWindow-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="43ef8-102">RestoreWindow macro action</span></span>

<span data-ttu-id="43ef8-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="43ef8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="43ef8-104">Um die vorherige Größe eines maximierten oder minimierten Fensters wiederherzustellen, können Sie die **WiederherstellenFenster**-Aktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="43ef8-104">You can use the **RestoreWindow** action to restore a maximized or minimized window to its previous size.</span></span>

> [!NOTE]
> <span data-ttu-id="43ef8-p101">Diese Aktion kann auf Codefenster des Visual Basic-Editors nicht angewendet werden. Informationen zu den Auswirkungen auf Codefenster finden Sie im Thema zur **WindowState**-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="43ef8-p101">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the **WindowState** property topic.</span></span>

## <a name="setting"></a><span data-ttu-id="43ef8-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="43ef8-107">Setting</span></span>

<span data-ttu-id="43ef8-108">Die **WiederherstellenFenster**-Aktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="43ef8-108">The **RestoreWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="43ef8-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43ef8-109">Remarks</span></span>

<span data-ttu-id="43ef8-p102">Diese Aktion funktioniert für das ausgewählte Objekt. Wenn ein Objekt minimiert worden ist, können Sie es auswählen, indem Sie die **AuswählenObjekt**-Aktion verwenden, und dann seine vorherige Größe wiederherstellen, indem Sie die **WiederherstellenFenster**-Aktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="43ef8-p102">This action works on the selected object. If an object has been minimized, you can first select it by using the **SelectObject** action and then restore it to its previous size by using the **RestoreWindow** action.</span></span>

<span data-ttu-id="43ef8-112">Sie können die **VerschiebenUndGrößeÄndernFenster** -Aktion verwenden, um ein Fenster, das wiederhergestellt wurde, zu verschieben oder in der Größe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="43ef8-112">You can use the **MoveAndSizeWindow** action to move or size a window that you have restored.</span></span>

<span data-ttu-id="43ef8-113">Die **WiederherstellenFenster**-Aktion hat dieselbe Wirkung wie ein Klicken auf die Schaltfläche **Wiederherstellen** in der rechten oberen Ecke des Fensters oder ein Klicken auf den Befehl **Wiederherstellen** im Fenstermenü **System**.</span><span class="sxs-lookup"><span data-stu-id="43ef8-113">The **RestoreWindow** action has the same effect as clicking the **Restore** button in the window's upper-right corner or clicking the **Restore** command on the window's **Control** menu.</span></span>

<span data-ttu-id="43ef8-114">Verwenden Sie die **Restore**-Methode des **DoCmd**-Objekts, um die **WiederherstellenFenster**-Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="43ef8-114">To run the **RestoreWindow** action in a Visual Basic for Applications (VBA) module, use the **Restore** method of the **DoCmd** object.</span></span>

