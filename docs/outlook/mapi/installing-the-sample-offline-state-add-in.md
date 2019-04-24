---
title: Installieren des Offline Status-Beispiel-Add-ins
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Zuletzt geändert: 06 Juli, 2012'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317213"
---
# <a name="installing-the-sample-offline-state-add-in"></a><span data-ttu-id="8ab3e-103">Installieren des Offline Status-Beispiel-Add-ins</span><span class="sxs-lookup"><span data-stu-id="8ab3e-103">Installing the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="8ab3e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ab3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ab3e-105">In diesem Thema werden die Schritte zum herunterladen und Installieren des Offline Status-Add-in-Beispiels erläutert.</span><span class="sxs-lookup"><span data-stu-id="8ab3e-105">This topic takes you through the steps to download and install the Sample Offline State Add-in.</span></span> <span data-ttu-id="8ab3e-106">Das Beispiel für Offlinestatus-Add-in ist ein COM-Add-in, das ein **Offlinestatus** Menü zu Outlook hinzufügt und die OFFLINESTATUS-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ab3e-106">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="8ab3e-107">Über das Offline Status Menü können Sie die Statusüberwachung aktivieren oder deaktivieren, den aktuellen Status überprüfen und den aktuellen Status ändern.</span><span class="sxs-lookup"><span data-stu-id="8ab3e-107">Through the Offline State menu you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="8ab3e-108">Weitere Informationen dazu, wie das Offlinestatus-Add-in implementiert wird, finden Sie unter [Einrichten eines Offlinestatus-Add-ins](setting-up-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="8ab3e-108">For more information about how the Offline State Add-in is implemented, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
## <a name="install-the-sample-offline-state-add-in"></a><span data-ttu-id="8ab3e-109">Installieren des Offline Status-Beispiel-Add-ins</span><span class="sxs-lookup"><span data-stu-id="8ab3e-109">Install the Sample Offline State Add-in</span></span>

1. <span data-ttu-id="8ab3e-110">Laden Sie sich das Beispiel für das Offline Status-Add-in hier herunter: [Outlook 2007 Auxiliary Reference Code Samples und redistributAble Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span><span class="sxs-lookup"><span data-stu-id="8ab3e-110">Download the Sample Offline State Add-in here: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="8ab3e-111">Führen Sie Visual Studio 2005 als Administrator aus.</span><span class="sxs-lookup"><span data-stu-id="8ab3e-111">Run Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="8ab3e-112">Wenn auf Ihrem Computer Windows XP läuft, müssen Sie als Administrator angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="8ab3e-112">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="8ab3e-113">Wenn auf Ihrem Computer Windows Vista installiert ist, müssen Sie als Administrator angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="8ab3e-113">If your computer is running Windows Vista, you must be logged in as an Administrator.</span></span> <span data-ttu-id="8ab3e-114">Klicken Sie mit der rechten Maustaste auf das Visual Studio 2005-Symbol, und klicken Sie auf **als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="8ab3e-114">Right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
3. <span data-ttu-id="8ab3e-115">Klicken Sie in Visual Studio 2005 auf **Datei**, wählen Sie **Öffnen**aus, und klicken Sie dann auf **Projekt/Lösung**.</span><span class="sxs-lookup"><span data-stu-id="8ab3e-115">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
4. <span data-ttu-id="8ab3e-116">Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, klicken Sie auf **ConnectionStateAddin**, und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="8ab3e-116">Browse to the location where you saved the sample, click **ConnectionStateAddin**, and then click **Open**.</span></span>
    
5. <span data-ttu-id="8ab3e-117">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="8ab3e-117">On the **Build** menu, click **Build Solution**.</span></span>
    
6. <span data-ttu-id="8ab3e-118">Klicken Sie im Dialogfeld **Datei speichern** unter auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="8ab3e-118">In the **Save File As** dialog box, click **Save**.</span></span>
    
7. <span data-ttu-id="8ab3e-119">Klicken Sie im **Startmenü** auf **Alle Programme**, klicken Sie auf **Zubehör**, klicken Sie mit der rechten Maustaste auf **Eingabeaufforderungen**, und klicken Sie dann auf **als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="8ab3e-119">Click the **Start** menu, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="8ab3e-120">Wenn Sie Windows XP betreiben, müssen Sie als Administrator angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="8ab3e-120">If you are running Windows XP, you must be logged in as an Administrator.</span></span> 
  
8. <span data-ttu-id="8ab3e-121">Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8ab3e-121">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
9. <span data-ttu-id="8ab3e-122">Ändern Sie im **Eingabe Aufforderungs** Fenster die Verzeichnisse in den Debug-Ordner, in dem Sie das Beispiel gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="8ab3e-122">In the **Command Prompt** window, change directories to the Debug folder where you saved the sample.</span></span> <span data-ttu-id="8ab3e-123">Wenn Sie beispielsweise das Beispiel in der Datei "c:" gespeichert haben, **"C:\ConnectionStateAddin\Debug"** , und drücken Sie dann die **Eingabe**Taste.</span><span class="sxs-lookup"><span data-stu-id="8ab3e-123">For example, if you saved the sample on your C:\ drive, you would type **cd "C:\ConnectionStateAddin\Debug"** and then press **ENTER**.</span></span> 
    
10. <span data-ttu-id="8ab3e-124">Geben Sie **regsvr32 OfflineStateAddin. dll** ein, und drücken **Sie die Eingabe**Taste.</span><span class="sxs-lookup"><span data-stu-id="8ab3e-124">Type **regsvr32 OfflineStateAddin.dll** and press **ENTER**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="8ab3e-125">Zum Deinstallieren des Beispiel-Offline Status-Add-ins geben Sie **regsvr32-u OfflineStateAddin. dll ein.**</span><span class="sxs-lookup"><span data-stu-id="8ab3e-125">To uninstall the Sample Offline State Add-in, type **regsvr32 -u OfflineStateAddin.dll**</span></span>
  
11. <span data-ttu-id="8ab3e-126">Klicken Sie im Dialogfeld **RegSrv32** auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ab3e-126">In the **RegSrv32** dialog box, click **OK**.</span></span>
    
12. <span data-ttu-id="8ab3e-127">Starten Sie Outlook neu, um das **Offline Status** Menü anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8ab3e-127">Restart Outlook to see the **Offline State** menu.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8ab3e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ab3e-128">See also</span></span>



[<span data-ttu-id="8ab3e-129">Informationen zur Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="8ab3e-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="8ab3e-130">Installieren des Offlinestatus-Add-In-Beispiels</span><span class="sxs-lookup"><span data-stu-id="8ab3e-130">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="8ab3e-131">Informationen zum Offlinestatus-Add-In-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8ab3e-131">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="8ab3e-132">Einrichten eines Offlinestatus-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="8ab3e-132">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
  
[<span data-ttu-id="8ab3e-133">Überwachen von Verbindungsstatusänderungen mit einem Offlinestatus-Add-In</span><span class="sxs-lookup"><span data-stu-id="8ab3e-133">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[<span data-ttu-id="8ab3e-134">Trennen eines Offline Status-Add-ins</span><span class="sxs-lookup"><span data-stu-id="8ab3e-134">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

