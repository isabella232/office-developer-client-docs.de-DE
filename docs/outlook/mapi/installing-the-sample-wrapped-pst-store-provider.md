---
title: Installieren des Umschlossenen Store -Beispielanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: 'Letzte �nderung: Donnerstag, 5. Juli 2012'
ms.openlocfilehash: a1574de555eb74d06c4dbe721e7e013ac59d3071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309632"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="5d82f-103">Installieren des Umschlossenen Store -Beispielanbieters</span><span class="sxs-lookup"><span data-stu-id="5d82f-103">Installing the Sample Wrapped PST Store Provider</span></span>

  
  
<span data-ttu-id="5d82f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d82f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d82f-105">In diesem Thema werden Die Schritte zum Herunterladen und Installieren des Beispielanbieters für umschlossene PST Store beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5d82f-105">This topic takes you through the steps to download and install the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="5d82f-106">Der Beispielanbieter für umbrochene PST Store WrapPST implementiert einen umschlossenen PST-Speicheranbieter, der in Verbindung mit der Replikations-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d82f-106">The Sample Wrapped PST Store Provider, WrapPST, implements a wrapped PST store provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="5d82f-107">Weitere Informationen zur Replikations-API finden Sie unter [Informationen zur Replikations-API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="5d82f-107">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="5d82f-108">Installieren des Beispielanbieters für Store PST</span><span class="sxs-lookup"><span data-stu-id="5d82f-108">Install the Sample Wrapped PST Store Provider</span></span>

1. <span data-ttu-id="5d82f-109">Informationen zum Herunterladen des Beispielanbieters für umschlossene PST Store finden Sie [unter Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span><span class="sxs-lookup"><span data-stu-id="5d82f-109">To download the Sample Wrapped PST Store Provider, see [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="5d82f-110">Öffnen Sie **den Ordner SampleWrappedPSTStoreProvider,** und klicken Sie auf **Alle Dateien extrahieren.**</span><span class="sxs-lookup"><span data-stu-id="5d82f-110">Open the **SampleWrappedPSTStoreProvider** folder and click **Extract All Files**.</span></span>
    
3. <span data-ttu-id="5d82f-111">Klicken **Sie auf Durchsuchen,** wählen Sie den Speicherort aus, an dem Sie das Beispiel speichern möchten, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d82f-111">Click **Browse**, select the location where you want to save the sample, and click **OK**.</span></span>
    
4. <span data-ttu-id="5d82f-112">Klicken Sie auf **Extrahieren**.</span><span class="sxs-lookup"><span data-stu-id="5d82f-112">Click **Extract**.</span></span> <span data-ttu-id="5d82f-113">Der ausgewählte Ordner wird angezeigt und enthält die extrahierten Dateien.</span><span class="sxs-lookup"><span data-stu-id="5d82f-113">The folder you selected appears and contains the extracted files.</span></span>
    
5. <span data-ttu-id="5d82f-114">Öffnen Visual Studio 2005 als Administrator.</span><span class="sxs-lookup"><span data-stu-id="5d82f-114">Open Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="5d82f-115">Wenn Ihr Computer mit Windows XP ausgeführt wird, müssen Sie als Administrator angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="5d82f-115">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="5d82f-116">Wenn Ihr Computer Windows Vista ausgeführt wird, müssen Sie als Administrator angemeldet sein, und Sie müssen mit der rechten Maustaste auf das Visual Studio 2005-Symbol klicken und auf Als Administrator **ausführen klicken.**</span><span class="sxs-lookup"><span data-stu-id="5d82f-116">If your computer is running Windows Vista, you must be logged in as an Administrator and you must right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
6. <span data-ttu-id="5d82f-117">Klicken Visual Studio 2005 auf **Datei,** wählen Sie **Öffnen** aus, und klicken Sie **dann auf Project/Lösung**.</span><span class="sxs-lookup"><span data-stu-id="5d82f-117">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
7. <span data-ttu-id="5d82f-118">Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, klicken Sie auf **WrapPST,** und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="5d82f-118">Browse to the location where you saved the sample, click **WrapPST**, and then click **Open**.</span></span>
    
8. <span data-ttu-id="5d82f-119">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="5d82f-119">On the **Build** menu, click **Build Solution**.</span></span>
    
9. <span data-ttu-id="5d82f-120">Klicken Sie im Dialogfeld Datei speichern **unter** auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="5d82f-120">In the **Save File As** dialog box, click **Save**.</span></span>
    
10. <span data-ttu-id="5d82f-121">Klicken Sie im Ordner, in dem Sie das Beispiel gespeichert haben, mit der rechten Maustaste **aufInstall.bat** und klicken Sie auf Als **Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="5d82f-121">In the folder where you saved the sample, right-click the **Install.bat** file and click **Run as administrator**.</span></span>
    
11. <span data-ttu-id="5d82f-122">Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5d82f-122">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5d82f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d82f-123">See also</span></span>



[<span data-ttu-id="5d82f-124">Informationen zum Beispiel umschlossenen STORE Anbieter</span><span class="sxs-lookup"><span data-stu-id="5d82f-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="5d82f-125">Initialisieren eines umschlossenen STORE Anbieters</span><span class="sxs-lookup"><span data-stu-id="5d82f-125">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="5d82f-126">Anmelden bei einem umschlossenen STORE Anbieter</span><span class="sxs-lookup"><span data-stu-id="5d82f-126">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="5d82f-127">Verwenden eines umschlossenen STORE Anbieters</span><span class="sxs-lookup"><span data-stu-id="5d82f-127">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="5d82f-128">Herunterfahren eines umschlossenen STORE Anbieters</span><span class="sxs-lookup"><span data-stu-id="5d82f-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

