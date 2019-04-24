---
title: Beispiel für Nachrichtenspeicher Anbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: eb51881aac6e1953a21686857944ba2a15d0dca2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356938"
---
# <a name="message-store-provider-sample"></a><span data-ttu-id="593e4-103">Beispiel für Nachrichtenspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="593e4-103">Message Store Provider Sample</span></span>

  
  
<span data-ttu-id="593e4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="593e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="593e4-105">Der Beispiel-Wrapped-PST-Speicheranbieter verwendet einen PST-Anbieter als Back-End zum Speichern von Daten.</span><span class="sxs-lookup"><span data-stu-id="593e4-105">The Sample Wrapped PST Store Provider uses a Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="593e4-106">Der eingebundene PST-Speicheranbieter sollte zusammen mit der Replikations-API verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="593e4-106">The wrapped PST store provider should be used together with the Replication API.</span></span> 
  
<span data-ttu-id="593e4-107">Mit der Replikations-API können Sie Elemente aus einem Back-End-Daten-Repository in einen Microsoft Outlook-PST-Speicher replizieren.</span><span class="sxs-lookup"><span data-stu-id="593e4-107">The Replication API enables you to replicate items from a back-end data repository into a Microsoft Outlook PST store.</span></span> <span data-ttu-id="593e4-108">Sie verwenden die Replikations-API, um die Daten in einem dedizierten PST-Speicher zu replizieren und den Synchronisierungsstatus nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="593e4-108">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="593e4-109">Weitere Informationen finden Sie unter [Informationen zur Replikations-API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="593e4-109">For more information, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="593e4-110">Die meisten Funktionen im beispielhaften PST-Speicheranbieter übergeben ihre Argumente direkt an den zugrunde liegenden PST-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="593e4-110">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="593e4-111">Bestimmte Funktionen erfordern eine spezielle Implementierung und werden in den folgenden Themen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="593e4-111">Certain functions require special implementation and are described in the following topics.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="593e4-112">Executable</span><span class="sxs-lookup"><span data-stu-id="593e4-112">Executable:</span></span>  <br/> |<span data-ttu-id="593e4-113">WrpPST32. dll</span><span class="sxs-lookup"><span data-stu-id="593e4-113">WrpPST32.dll</span></span>  <br/> |
|<span data-ttu-id="593e4-114">Quellcodeverzeichnis:</span><span class="sxs-lookup"><span data-stu-id="593e4-114">Source code directory:</span></span>  <br/> |<span data-ttu-id="593e4-115">SampleWrappedPSTStoreProvider\WrapPST</span><span class="sxs-lookup"><span data-stu-id="593e4-115">SampleWrappedPSTStoreProvider\WrapPST</span></span>  <br/> |
|<span data-ttu-id="593e4-116">Sprache</span><span class="sxs-lookup"><span data-stu-id="593e4-116">Language:</span></span>  <br/> |<span data-ttu-id="593e4-117">C++</span><span class="sxs-lookup"><span data-stu-id="593e4-117">C++</span></span>  <br/> |
|<span data-ttu-id="593e4-118">Plattformen</span><span class="sxs-lookup"><span data-stu-id="593e4-118">Platforms:</span></span>  <br/> |<span data-ttu-id="593e4-119">Microsoft Visual Studio 2008 für die Kompilierung für Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="593e4-119">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="593e4-120">Unterstützte Features</span><span class="sxs-lookup"><span data-stu-id="593e4-120">Supported Features</span></span>

<span data-ttu-id="593e4-121">In diesem Beispiel wird Microsoft Outlook 2010 64-Bit unterstützt und nun für Outlook 2013 überarbeitet.</span><span class="sxs-lookup"><span data-stu-id="593e4-121">This sample supports Microsoft Outlook 2010 64-bit and has now been revised for Outlook 2013.</span></span> <span data-ttu-id="593e4-122">Weitere Informationen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="593e4-122">See the following topics for additional information:</span></span>
  
- [<span data-ttu-id="593e4-123">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="593e4-123">About the Replication API</span></span>](about-the-replication-api.md)
    
- [<span data-ttu-id="593e4-124">Initialisieren eines einGebundenen PST-Speicheranbieters</span><span class="sxs-lookup"><span data-stu-id="593e4-124">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="593e4-125">Anmelden bei einem einGebundenen PST-Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="593e4-125">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="593e4-126">Verwenden eines einGebundenen PST-Speicheranbieters</span><span class="sxs-lookup"><span data-stu-id="593e4-126">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="593e4-127">Herunterfahren eines einGebundenen PST-Speicheranbieters</span><span class="sxs-lookup"><span data-stu-id="593e4-127">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
 <span data-ttu-id="593e4-128">**So installieren Sie den beispielhaften PST-Speicheranbieter**</span><span class="sxs-lookup"><span data-stu-id="593e4-128">**To install the Sample Wrapped PST Store Provider**</span></span>
  
1. <span data-ttu-id="593e4-129">Informationen zum Herunterladen des Beispiel-Wrapper-PST-Anbieters finden Sie unter [herunterladen der Outlook-MAPI-Beispiele](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="593e4-129">To download the Sample Wrapped PST Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="593e4-130">Suchen Sie den Ordner, in dem Sie die Outlook-MAPI-Beispiele gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="593e4-130">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="593e4-131">Klicken Sie mit der rechten Maustaste auf den Zip **-Ordner OutlookMAPISamples-\<Versions\> Nummer** , und klicken Sie dann auf **Alle extrahieren**.</span><span class="sxs-lookup"><span data-stu-id="593e4-131">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and then click **Extract All**.</span></span>
    
3. <span data-ttu-id="593e4-132">Klicken Sie auf **Durchsuchen**, wählen Sie den Speicherort aus, an dem Sie das Beispiel speichern möchten, und klicken Sie dann auf **extrahieren**.</span><span class="sxs-lookup"><span data-stu-id="593e4-132">Click **Browse**, select the location where you want to save the sample, and then click **Extract**.</span></span>
    
4. <span data-ttu-id="593e4-133">Führen Sie Microsoft Visual Studio 2008 aus.</span><span class="sxs-lookup"><span data-stu-id="593e4-133">Run Microsoft Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="593e4-134">Klicken Sie in Microsoft Visual Studio 2008 auf **Datei**, wählen Sie **Öffnen**aus, und klicken Sie dann auf **Projekt/Lösung**.</span><span class="sxs-lookup"><span data-stu-id="593e4-134">In Microsoft Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="593e4-135">Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, klicken Sie auf **WrapPST. vcproj**, und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="593e4-135">Browse to the location where you saved the sample, click **WrapPST.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="593e4-136">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="593e4-136">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="593e4-137">Klicken Sie im Dialogfeld **Datei speichern** unter auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="593e4-137">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="593e4-138">Klicken Sie in dem Ordner, in dem Sie das Beispiel gespeichert haben, mit der rechten Maustaste auf die Datei **install. bat** , und klicken Sie dann auf **als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="593e4-138">In the folder where you saved the sample, right-click the **install.bat** file and then click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="593e4-139">Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="593e4-139">In the **User Account Control** dialog box, click **Continue**.</span></span>
    

