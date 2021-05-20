---
title: Beispiel für Store-Anbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: eb51881aac6e1953a21686857944ba2a15d0dca2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436867"
---
# <a name="message-store-provider-sample"></a><span data-ttu-id="81499-103">Beispiel für Store-Anbieter</span><span class="sxs-lookup"><span data-stu-id="81499-103">Message Store Provider Sample</span></span>

  
  
<span data-ttu-id="81499-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81499-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81499-105">Der Beispielanbieter für Store PST verwendet einen Anbieter für persönliche Ordner als Back-End zum Speichern von Daten.</span><span class="sxs-lookup"><span data-stu-id="81499-105">The Sample Wrapped PST Store Provider uses a Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="81499-106">Der umschlossene ANBIETER für den PST-Speicher sollte zusammen mit der Replikations-API verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81499-106">The wrapped PST store provider should be used together with the Replication API.</span></span> 
  
<span data-ttu-id="81499-107">Mit der Replikations-API können Sie Elemente aus einem Back-End-Datenrepository in einen Microsoft Outlook PST Store replizieren.</span><span class="sxs-lookup"><span data-stu-id="81499-107">The Replication API enables you to replicate items from a back-end data repository into a Microsoft Outlook PST store.</span></span> <span data-ttu-id="81499-108">Sie verwenden die Replikations-API, um die Daten in einen dedizierten PST-Speicher zu replizieren und den Synchronisierungsstatus zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="81499-108">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="81499-109">Weitere Informationen finden Sie unter [Informationen zur Replikations-API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="81499-109">For more information, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="81499-110">Die meisten Funktionen im Beispielanbieter für umschlossene STORE übergeben ihre Argumente direkt an den zugrunde liegenden PST-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="81499-110">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="81499-111">Bestimmte Funktionen erfordern eine spezielle Implementierung und werden in den folgenden Themen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="81499-111">Certain functions require special implementation and are described in the following topics.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="81499-112">Ausführbare Datei:</span><span class="sxs-lookup"><span data-stu-id="81499-112">Executable:</span></span>  <br/> |<span data-ttu-id="81499-113">WrpPST32.dll</span><span class="sxs-lookup"><span data-stu-id="81499-113">WrpPST32.dll</span></span>  <br/> |
|<span data-ttu-id="81499-114">Quellcodeverzeichnis:</span><span class="sxs-lookup"><span data-stu-id="81499-114">Source code directory:</span></span>  <br/> |<span data-ttu-id="81499-115">SampleWrappedPSTStoreProvider\WrapPST</span><span class="sxs-lookup"><span data-stu-id="81499-115">SampleWrappedPSTStoreProvider\WrapPST</span></span>  <br/> |
|<span data-ttu-id="81499-116">Sprache:</span><span class="sxs-lookup"><span data-stu-id="81499-116">Language:</span></span>  <br/> |<span data-ttu-id="81499-117">C++</span><span class="sxs-lookup"><span data-stu-id="81499-117">C++</span></span>  <br/> |
|<span data-ttu-id="81499-118">Plattformen:</span><span class="sxs-lookup"><span data-stu-id="81499-118">Platforms:</span></span>  <br/> |<span data-ttu-id="81499-119">Microsoft Visual Studio 2008 zum Kompilieren für Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="81499-119">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="81499-120">Unterstützte Features</span><span class="sxs-lookup"><span data-stu-id="81499-120">Supported Features</span></span>

<span data-ttu-id="81499-121">Dieses Beispiel unterstützt Microsoft Outlook 2010 64-Bit und wurde nun für Outlook 2013 überarbeitet.</span><span class="sxs-lookup"><span data-stu-id="81499-121">This sample supports Microsoft Outlook 2010 64-bit and has now been revised for Outlook 2013.</span></span> <span data-ttu-id="81499-122">Weitere Informationen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="81499-122">See the following topics for additional information:</span></span>
  
- [<span data-ttu-id="81499-123">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="81499-123">About the Replication API</span></span>](about-the-replication-api.md)
    
- [<span data-ttu-id="81499-124">Initialisieren eines umschlossenen STORE Anbieters</span><span class="sxs-lookup"><span data-stu-id="81499-124">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="81499-125">Anmelden bei einem umschlossenen STORE Anbieter</span><span class="sxs-lookup"><span data-stu-id="81499-125">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="81499-126">Verwenden eines umschlossenen STORE Anbieters</span><span class="sxs-lookup"><span data-stu-id="81499-126">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="81499-127">Herunterfahren eines umschlossenen STORE Anbieters</span><span class="sxs-lookup"><span data-stu-id="81499-127">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
 <span data-ttu-id="81499-128">**So installieren Sie den Beispielanbieter für Store PST**</span><span class="sxs-lookup"><span data-stu-id="81499-128">**To install the Sample Wrapped PST Store Provider**</span></span>
  
1. <span data-ttu-id="81499-129">Informationen zum Herunterladen des Beispielanbieters für umschlossene PST finden Sie unter [Herunterladen der Outlook MAPI-Beispiele](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="81499-129">To download the Sample Wrapped PST Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="81499-130">Suchen Sie den Ordner, in dem Sie die Outlook gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="81499-130">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="81499-131">Klicken Sie mit der rechten Maustaste auf den **Ordner OutlookMAPISamples- \< version number \>** zip, und klicken Sie dann auf Alle **extrahieren.**</span><span class="sxs-lookup"><span data-stu-id="81499-131">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and then click **Extract All**.</span></span>
    
3. <span data-ttu-id="81499-132">Klicken **Sie auf Durchsuchen,** wählen Sie den Speicherort aus, an dem Sie das Beispiel speichern möchten, und klicken Sie dann auf **Extrahieren**.</span><span class="sxs-lookup"><span data-stu-id="81499-132">Click **Browse**, select the location where you want to save the sample, and then click **Extract**.</span></span>
    
4. <span data-ttu-id="81499-133">Führen Microsoft Visual Studio 2008 aus.</span><span class="sxs-lookup"><span data-stu-id="81499-133">Run Microsoft Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="81499-134">Klicken Microsoft Visual Studio 2008 auf **Datei,** wählen Sie **Öffnen** aus, und klicken Sie **dann auf Project/Lösung**.</span><span class="sxs-lookup"><span data-stu-id="81499-134">In Microsoft Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="81499-135">Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, klicken Sie auf **WrapPST.vcproj,** und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="81499-135">Browse to the location where you saved the sample, click **WrapPST.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="81499-136">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="81499-136">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="81499-137">Klicken Sie im Dialogfeld Datei speichern **unter** auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="81499-137">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="81499-138">Klicken Sie im Ordner, in dem Sie das Beispiel gespeichert **haben,** mit der rechten Maustaste aufinstall.batdatei, und klicken Sie dann **auf Als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="81499-138">In the folder where you saved the sample, right-click the **install.bat** file and then click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="81499-139">Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="81499-139">In the **User Account Control** dialog box, click **Continue**.</span></span>
    

