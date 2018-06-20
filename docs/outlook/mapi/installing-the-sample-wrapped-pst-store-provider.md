---
title: Installieren des Beispiels umfließendem PST-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: 'Letzte �nderung: Donnerstag, 5. Juli 2012'
ms.openlocfilehash: 29aabc7a2e8513bf24bd3b56ff3e4a126e3d7437
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792696"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="6545f-103">Installieren des Beispiels umfließendem PST-Anbieter</span><span class="sxs-lookup"><span data-stu-id="6545f-103">Installing the Sample Wrapped PST Store Provider</span></span>

  
  
<span data-ttu-id="6545f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6545f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6545f-105">In diesem Thema führt Sie durch die Schritte zum Herunterladen und Installieren der umbrochen PST Store Beispielanbieter.</span><span class="sxs-lookup"><span data-stu-id="6545f-105">This topic takes you through the steps to download and install the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="6545f-106">Die umfließendem PST-Datei speichern Beispielanbieter, WrapPST, implementiert einen gepackten PST-Anbieter, der in Verbindung mit der API für die Replikation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6545f-106">The Sample Wrapped PST Store Provider, WrapPST, implements a wrapped PST store provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="6545f-107">Weitere Informationen zur Replikation-API finden Sie unter [Über die Replikation-API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="6545f-107">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="6545f-108">Installieren des Beispielanbieters gepackten PST-Speichers</span><span class="sxs-lookup"><span data-stu-id="6545f-108">Install the Sample Wrapped PST Store Provider</span></span>

1. <span data-ttu-id="6545f-109">Um die umfließendem PST Store Beispielanbieter herunterladen möchten, finden Sie unter [Outlook 2007: zusätzliche Referenzcodebeispiele und verteilbares Installationsprogramm](http://www.microsoft.com/en-us/download/details.aspx?id=24102).</span><span class="sxs-lookup"><span data-stu-id="6545f-109">To download the Sample Wrapped PST Store Provider, see [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](http://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="6545f-110">Öffnen Sie den Ordner **SampleWrappedPSTStoreProvider** , und klicken Sie auf **Allerdateien extrahieren**.</span><span class="sxs-lookup"><span data-stu-id="6545f-110">Open the **SampleWrappedPSTStoreProvider** folder and click **Extract All Files**.</span></span>
    
3. <span data-ttu-id="6545f-111">Klicken Sie auf **Durchsuchen**, markieren Sie den Speicherort, in dem Sie das Beispiel zu speichern möchten, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="6545f-111">Click **Browse**, select the location where you want to save the sample, and click **OK**.</span></span>
    
4. <span data-ttu-id="6545f-112">Klicken Sie auf **extrahieren**.</span><span class="sxs-lookup"><span data-stu-id="6545f-112">Click **Extract**.</span></span> <span data-ttu-id="6545f-113">Der Ordner gewählte angezeigt wird und die extrahierten Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="6545f-113">The folder you selected appears and contains the extracted files.</span></span>
    
5. <span data-ttu-id="6545f-114">Öffnen Sie Visual Studio 2005 als Administrator an.</span><span class="sxs-lookup"><span data-stu-id="6545f-114">Open Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="6545f-115">Wenn Ihr Computer unter Windows XP ausgeführt wird, müssen Sie als Administrator angemeldet sein,.</span><span class="sxs-lookup"><span data-stu-id="6545f-115">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="6545f-116">Wenn Ihr Computer Windows Vista ausgeführt wird, müssen Sie als Administrator, und Sie müssen mit der rechten Maustaste in des Visual Studio 2005-Symbols und klicken Sie auf **als Administrator ausführen**angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="6545f-116">If your computer is running Windows Vista, you must be logged in as an Administrator and you must right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
6. <span data-ttu-id="6545f-117">Klicken Sie in Visual Studio 2005 auf **Datei**, klicken Sie auf **Öffnen**, und klicken Sie dann auf **Projekt/Projektmappe**.</span><span class="sxs-lookup"><span data-stu-id="6545f-117">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
7. <span data-ttu-id="6545f-118">Navigieren Sie zum Speicherort, in dem Sie das Beispiel gespeichert haben, klicken Sie auf **WrapPST**und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="6545f-118">Browse to the location where you saved the sample, click **WrapPST**, and then click **Open**.</span></span>
    
8. <span data-ttu-id="6545f-119">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="6545f-119">On the **Build** menu, click **Build Solution**.</span></span>
    
9. <span data-ttu-id="6545f-120">Klicken Sie im Dialogfeld **Datei speichern unter** auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="6545f-120">In the **Save File As** dialog box, click **Save**.</span></span>
    
10. <span data-ttu-id="6545f-121">In den Ordner, in dem Sie das Beispiel gespeichert haben, mit der rechten Maustaste in der Datei **Install.bat aus** , und klicken Sie auf **als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="6545f-121">In the folder where you saved the sample, right-click the **Install.bat** file and click **Run as administrator**.</span></span>
    
11. <span data-ttu-id="6545f-122">Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="6545f-122">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6545f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6545f-123">See also</span></span>



[<span data-ttu-id="6545f-124">Zum Beispiel umgebrochen PST-Anbieter</span><span class="sxs-lookup"><span data-stu-id="6545f-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="6545f-125">Initialisieren einen Anbieter für umbrochenen PST anmelden</span><span class="sxs-lookup"><span data-stu-id="6545f-125">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="6545f-126">Anmelden bei einem Anbieter gepackten PST-Datei</span><span class="sxs-lookup"><span data-stu-id="6545f-126">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="6545f-127">Verwenden eines Anbieters gepackten PST-Speichers</span><span class="sxs-lookup"><span data-stu-id="6545f-127">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="6545f-128">Herunterfahren von einem Anbieter gepackten PST-Datei</span><span class="sxs-lookup"><span data-stu-id="6545f-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
