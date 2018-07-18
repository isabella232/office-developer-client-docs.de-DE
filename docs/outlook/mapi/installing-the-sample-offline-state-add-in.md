---
title: Installieren des Offlinestatus-Add-In-Beispiels
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Zuletzt geändert: 06 Juli 2012'
ms.openlocfilehash: 00232f290c367c4bab1854bfe3909abc7b03cef8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792715"
---
# <a name="installing-the-sample-offline-state-add-in"></a><span data-ttu-id="5fe98-103">Installieren des Offlinestatus-Add-In-Beispiels</span><span class="sxs-lookup"><span data-stu-id="5fe98-103">Installing the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="5fe98-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5fe98-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5fe98-105">In diesem Thema führt Sie durch die Schritte zum Herunterladen und Offline-Status Beispiel-Add-in installieren.</span><span class="sxs-lookup"><span data-stu-id="5fe98-105">This topic takes you through the steps to download and install the Sample Offline State Add-in.</span></span> <span data-ttu-id="5fe98-106">Das Offline-Status Beispiel-Add-in ist ein COM-add-in, die ein Menü **Status als offline anzeigen** zu Outlook hinzugefügt und State-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fe98-106">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="5fe98-107">Überprüfen Sie über das Menü Offline-Status, das können Sie aktivieren oder deaktivieren, Status der Überwachung den aktuellen Status, und ändern Sie den aktuellen Status.</span><span class="sxs-lookup"><span data-stu-id="5fe98-107">Through the Offline State menu you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="5fe98-108">Weitere Informationen dazu, wie das Offline-Status-Add-in implementiert wird finden Sie unter [Einstellung Up eine Offline-Status-Add-in](setting-up-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="5fe98-108">For more information about how the Offline State Add-in is implemented, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
## <a name="install-the-sample-offline-state-add-in"></a><span data-ttu-id="5fe98-109">Installieren Sie das Beispiel Offline State-Add-in</span><span class="sxs-lookup"><span data-stu-id="5fe98-109">Install the Sample Offline State Add-in</span></span>

1. <span data-ttu-id="5fe98-110">Das Beispiel Offline Zustand Add-in hier herunterladen: [Outlook 2007: zusätzliche Referenzcodebeispiele und verteilbares Installationsprogramm](http://www.microsoft.com/en-us/download/details.aspx?id=24102).</span><span class="sxs-lookup"><span data-stu-id="5fe98-110">Download the Sample Offline State Add-in here: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](http://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="5fe98-111">Visual Studio 2005 als Administrator ausführen.</span><span class="sxs-lookup"><span data-stu-id="5fe98-111">Run Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="5fe98-112">Wenn Ihr Computer unter Windows XP ausgeführt wird, müssen Sie als Administrator angemeldet sein,.</span><span class="sxs-lookup"><span data-stu-id="5fe98-112">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="5fe98-113">Wenn Ihr Computer Windows Vista ausgeführt wird, müssen Sie als Administrator angemeldet sein,.</span><span class="sxs-lookup"><span data-stu-id="5fe98-113">If your computer is running Windows Vista, you must be logged in as an Administrator.</span></span> <span data-ttu-id="5fe98-114">Mit der rechten Maustaste in des Visual Studio 2005-Symbols, und klicken Sie auf **als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="5fe98-114">Right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
3. <span data-ttu-id="5fe98-115">Klicken Sie in Visual Studio 2005 auf **Datei**, klicken Sie auf **Öffnen**, und klicken Sie dann auf **Projekt/Projektmappe**.</span><span class="sxs-lookup"><span data-stu-id="5fe98-115">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
4. <span data-ttu-id="5fe98-116">Navigieren Sie zum Speicherort, in dem Sie das Beispiel gespeichert haben, klicken Sie auf **ConnectionStateAddin**und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="5fe98-116">Browse to the location where you saved the sample, click **ConnectionStateAddin**, and then click **Open**.</span></span>
    
5. <span data-ttu-id="5fe98-117">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="5fe98-117">On the **Build** menu, click **Build Solution**.</span></span>
    
6. <span data-ttu-id="5fe98-118">Klicken Sie im Dialogfeld **Datei speichern unter** auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="5fe98-118">In the **Save File As** dialog box, click **Save**.</span></span>
    
7. <span data-ttu-id="5fe98-119">Klicken Sie auf **das Startmenü** , klicken Sie auf **Alle Programme**, klicken Sie auf **Zubehör**, mit der rechten Maustaste **an der Eingabeaufforderung**, und klicken Sie dann auf **als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="5fe98-119">Click the **Start** menu, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="5fe98-120">Wenn Sie Windows XP ausgeführt werden, müssen Sie als Administrator angemeldet sein,.</span><span class="sxs-lookup"><span data-stu-id="5fe98-120">If you are running Windows XP, you must be logged in as an Administrator.</span></span> 
  
8. <span data-ttu-id="5fe98-121">Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5fe98-121">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
9. <span data-ttu-id="5fe98-122">Wechseln Sie in **das Eingabeaufforderungsfenster** zum Ordner "Debug", in dem Sie das Beispiel gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="5fe98-122">In the **Command Prompt** window, change directories to the Debug folder where you saved the sample.</span></span> <span data-ttu-id="5fe98-123">Wenn Sie das Beispiel auf Laufwerk C:\ gespeichert, würden Sie beispielsweise geben Sie **cd "C:\ConnectionStateAddin\Debug"** und **dann die EINGABETASTE**.</span><span class="sxs-lookup"><span data-stu-id="5fe98-123">For example, if you saved the sample on your C:\ drive, you would type **cd "C:\ConnectionStateAddin\Debug"** and then press **ENTER**.</span></span> 
    
10. <span data-ttu-id="5fe98-124">Geben Sie **regsvr32 OfflineStateAddin.dll** ein, und drücken Sie die **EINGABETASTE**.</span><span class="sxs-lookup"><span data-stu-id="5fe98-124">Type **regsvr32 OfflineStateAddin.dll** and press **ENTER**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="5fe98-125">Um das Beispiel Offline Zustand-Add-in zu deinstallieren, geben Sie **regsvr32 -u OfflineStateAddin.dll**</span><span class="sxs-lookup"><span data-stu-id="5fe98-125">To uninstall the Sample Offline State Add-in, type **regsvr32 -u OfflineStateAddin.dll**</span></span>
  
11. <span data-ttu-id="5fe98-126">Klicken Sie im Dialogfeld **RegSrv32** klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="5fe98-126">In the **RegSrv32** dialog box, click **OK**.</span></span>
    
12. <span data-ttu-id="5fe98-127">Starten Sie Outlook, um das Menü **Status als Offline** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5fe98-127">Restart Outlook to see the **Offline State** menu.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="5fe98-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fe98-128">See also</span></span>



[<span data-ttu-id="5fe98-129">Informationen zu der Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="5fe98-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="5fe98-130">Installieren des Offlinestatus-Add-In-Beispiels</span><span class="sxs-lookup"><span data-stu-id="5fe98-130">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="5fe98-131">Informationen zum Offlinestatus-Add-In-Beispiel</span><span class="sxs-lookup"><span data-stu-id="5fe98-131">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="5fe98-132">Einrichten eines Offlinestatus-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="5fe98-132">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
  
[<span data-ttu-id="5fe98-133">Überwachen von Verbindungsstatusänderungen mit einem Offlinestatus-Add-In</span><span class="sxs-lookup"><span data-stu-id="5fe98-133">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[<span data-ttu-id="5fe98-134">Trennen eines Offlinestatus-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="5fe98-134">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

