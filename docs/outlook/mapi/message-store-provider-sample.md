---
title: Beispiel für einen Nachrichtenspeicher
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b3c907b0a53a41a52516b23ffb1cf7400d887d89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793260"
---
# <a name="message-store-provider-sample"></a><span data-ttu-id="58010-103">Beispiel für einen Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="58010-103">Message Store Provider Sample</span></span>

  
  
<span data-ttu-id="58010-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="58010-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="58010-105">Der umbrochen PST Store Beispielanbieter verwendet einen Anbieter für Persönliche Ordner-Datei (PST) als Back-End zum Speichern von Daten.</span><span class="sxs-lookup"><span data-stu-id="58010-105">The Sample Wrapped PST Store Provider uses a Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="58010-106">Der gepackten PST-Speicheranbieter sollten zusammen mit der API für die Replikation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58010-106">The wrapped PST store provider should be used together with the Replication API.</span></span> 
  
<span data-ttu-id="58010-107">Replikation der API können Sie Elemente in einem Microsoft Outlook-PST-Speicher aus einem Back-End-Daten-Repository repliziert werden.</span><span class="sxs-lookup"><span data-stu-id="58010-107">The Replication API enables you to replicate items from a back-end data repository into a Microsoft Outlook PST store.</span></span> <span data-ttu-id="58010-108">Sie verwenden die Replikation-API zum Replizieren von Daten in einer dedizierten PST-Speicher und verfolgen an den Synchronisierungsstatus.</span><span class="sxs-lookup"><span data-stu-id="58010-108">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="58010-109">Weitere Informationen finden Sie unter [Informationen zu Replikation API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="58010-109">For more information, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="58010-110">Die meisten Funktionen in der umbrochen PST Store Beispielanbieter übergeben ihre Argumente direkt an dem zugrunde liegenden PST-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="58010-110">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="58010-111">Bestimmte Funktionen erfordern besondere Implementierung und werden in den folgenden Themen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="58010-111">Certain functions require special implementation and are described in the following topics.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="58010-112">Ausführbare Datei:</span><span class="sxs-lookup"><span data-stu-id="58010-112">Executable:</span></span>  <br/> |<span data-ttu-id="58010-113">WrpPST32.dll</span><span class="sxs-lookup"><span data-stu-id="58010-113">WrpPST32.dll</span></span>  <br/> |
|<span data-ttu-id="58010-114">Code Quellverzeichnis:</span><span class="sxs-lookup"><span data-stu-id="58010-114">Source code directory:</span></span>  <br/> |<span data-ttu-id="58010-115">SampleWrappedPSTStoreProvider\WrapPST</span><span class="sxs-lookup"><span data-stu-id="58010-115">SampleWrappedPSTStoreProvider\WrapPST</span></span>  <br/> |
|<span data-ttu-id="58010-116">Sprache:</span><span class="sxs-lookup"><span data-stu-id="58010-116">Language:</span></span>  <br/> |<span data-ttu-id="58010-117">C++</span><span class="sxs-lookup"><span data-stu-id="58010-117">C++</span></span>  <br/> |
|<span data-ttu-id="58010-118">Plattformen:</span><span class="sxs-lookup"><span data-stu-id="58010-118">Platforms:</span></span>  <br/> |<span data-ttu-id="58010-119">Microsoft Visual Studio 2008 zum Kompilieren für Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="58010-119">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="58010-120">Unterstützte Features</span><span class="sxs-lookup"><span data-stu-id="58010-120">Supported Features</span></span>

<span data-ttu-id="58010-121">In diesem Beispiel unterstützt Microsoft Outlook 2010 64-Bit- und wurde für Outlook 2013 jetzt überarbeitet.</span><span class="sxs-lookup"><span data-stu-id="58010-121">This sample supports Microsoft Outlook 2010 64-bit and has now been revised for Outlook 2013.</span></span> <span data-ttu-id="58010-122">Finden Sie unter den folgenden Themen Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="58010-122">See the following topics for additional information:</span></span>
  
- [<span data-ttu-id="58010-123">Über die API-Replikation</span><span class="sxs-lookup"><span data-stu-id="58010-123">About the Replication API</span></span>](about-the-replication-api.md)
    
- [<span data-ttu-id="58010-124">Initialisieren einen Anbieter für umbrochenen PST anmelden</span><span class="sxs-lookup"><span data-stu-id="58010-124">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="58010-125">Anmelden bei einem Anbieter gepackten PST-Datei</span><span class="sxs-lookup"><span data-stu-id="58010-125">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="58010-126">Verwenden eines Anbieters gepackten PST-Speichers</span><span class="sxs-lookup"><span data-stu-id="58010-126">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="58010-127">Herunterfahren von einem Anbieter gepackten PST-Datei</span><span class="sxs-lookup"><span data-stu-id="58010-127">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
 <span data-ttu-id="58010-128">**So installieren Sie die umfließendem PST Store Beispielanbieter**</span><span class="sxs-lookup"><span data-stu-id="58010-128">**To install the Sample Wrapped PST Store Provider**</span></span>
  
1. <span data-ttu-id="58010-129">Zum Beispiel umgebrochen PST-Anbieter finden Sie unter [Herunterladen der MAPI-Beispiele für Outlook](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="58010-129">To download the Sample Wrapped PST Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="58010-130">Suchen Sie den Ordner, in dem Sie die MAPI-Beispiele für Outlook gespeichert.</span><span class="sxs-lookup"><span data-stu-id="58010-130">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="58010-131">Mit der rechten Maustaste die **OutlookMAPISamples -\<Versionsnummer\> ** zip-Ordner, und klicken Sie dann auf **Alle extrahieren**.</span><span class="sxs-lookup"><span data-stu-id="58010-131">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and then click **Extract All**.</span></span>
    
3. <span data-ttu-id="58010-132">Klicken Sie auf **Durchsuchen**, markieren Sie den Speicherort, in dem Sie das Beispiel zu speichern möchten, und klicken Sie dann auf **extrahieren**.</span><span class="sxs-lookup"><span data-stu-id="58010-132">Click **Browse**, select the location where you want to save the sample, and then click **Extract**.</span></span>
    
4. <span data-ttu-id="58010-133">Führen Sie Microsoft Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="58010-133">Run Microsoft Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="58010-134">Klicken Sie in Microsoft Visual Studio 2008 auf **Datei**, klicken Sie auf **Öffnen**, und klicken Sie dann auf **Projekt/Projektmappe**.</span><span class="sxs-lookup"><span data-stu-id="58010-134">In Microsoft Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="58010-135">Navigieren Sie zum Speicherort, in dem Sie das Beispiel gespeichert haben, klicken Sie auf **WrapPST.vcproj**und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="58010-135">Browse to the location where you saved the sample, click **WrapPST.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="58010-136">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="58010-136">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="58010-137">Klicken Sie im Dialogfeld **Datei speichern unter** auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="58010-137">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="58010-138">In den Ordner, in dem Sie das Beispiel gespeichert haben, mit der rechten Maustaste in der Datei **Install.bat aus** , und klicken Sie dann auf **als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="58010-138">In the folder where you saved the sample, right-click the **install.bat** file and then click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="58010-139">Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="58010-139">In the **User Account Control** dialog box, click **Continue**.</span></span>
    

