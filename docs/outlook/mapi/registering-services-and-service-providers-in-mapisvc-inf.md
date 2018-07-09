---
title: Registrieren von Diensten und Dienstanbieter in MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Zuletzt geändert: 18 Juli 2013'
ms.openlocfilehash: 2eb7f1b496e0732b157ea4f9105a0e067329c52f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795359"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a><span data-ttu-id="35f51-103">Registrieren von Diensten und Dienstanbieter in MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="35f51-103">Registering Services and Service Providers in MapiSvc.inf</span></span>

 
  
<span data-ttu-id="35f51-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="35f51-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="35f51-105">Installieren einen neuen Anbieter auf einem System erfordert die Aktualisierung der Datei "MapiSvc.inf" So zeigen Sie auf den neuen Anbieter.</span><span class="sxs-lookup"><span data-stu-id="35f51-105">Installing a new provider on a system requires updating the MapiSvc.inf file to point to the new provider.</span></span> <span data-ttu-id="35f51-106">Standardeigenschaften festlegen während der Konfiguration, die Folgendes enthalten, MAPI zu informieren, wo der Anbieter Dynamic Link Library (DLL) zu finden:</span><span class="sxs-lookup"><span data-stu-id="35f51-106">Standard properties set during configuration, which include the following, inform MAPI where to find the provider's dynamic-link library (.dll):</span></span>
  
- <span data-ttu-id="35f51-107">Die **PR_SERVICE_DLL_NAME** wird im Abschnitt **[Messagingdiensts]** angegeben.</span><span class="sxs-lookup"><span data-stu-id="35f51-107">The **PR_SERVICE_DLL_NAME** is specified in the **[Message Service]** section.</span></span> 
    
- <span data-ttu-id="35f51-108">Die **PR_PROVIDER_DLL_NAME** wird im Abschnitt **[Service Provider]** angegeben.</span><span class="sxs-lookup"><span data-stu-id="35f51-108">The **PR_PROVIDER_DLL_NAME** is specified in the **[Service Provider]** section.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="35f51-109">Es wird erwartet, dass Sie den Namen des Anbieters DLL (ohne das Suffix "32") festgelegt.</span><span class="sxs-lookup"><span data-stu-id="35f51-109">The expectation is that you set the name of your provider's .dll (without the suffix "32").</span></span> <span data-ttu-id="35f51-110">MAPI lädt Ihres Anbieters klicken Sie dann auf den Pfad gesucht.</span><span class="sxs-lookup"><span data-stu-id="35f51-110">MAPI then loads your provider by looking for it on the path.</span></span> 
  
## <a name="putting-a-path-in-mapisvcinf"></a><span data-ttu-id="35f51-111">Einen Pfad Websitemigration MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="35f51-111">Putting a Path in MapiSvc.inf</span></span>

<span data-ttu-id="35f51-112">Die meisten installieren unter Programmdateien, erfordern ein Update zur Path-Variablen um MAPI-Anbieter arbeiten zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="35f51-112">Most applications install under Program Files, requiring an update to the path variable to allow MAPI providers to work.</span></span> <span data-ttu-id="35f51-113">Mit einigen Einschränkungen unterstützen Microsoft Outlook 2010 und Outlook 2013 vollständige Pfade zu MAPI-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="35f51-113">With a few restrictions Microsoft Outlook 2010 and Outlook 2013 can accommodate full paths to MAPI providers.</span></span>
  
<span data-ttu-id="35f51-114">Beim Registrieren des Anbieters in MapiSvc.inf, könnten Sie den vollständigen Pfad des Anbieters in der MAPI-Eigenschaften **PR_SERVICE_DLL_NAME** und **PR_PROVIDER_DLL_NAME**einfügen.</span><span class="sxs-lookup"><span data-stu-id="35f51-114">When registering your provider in MapiSvc.inf, you could put the full path to the provider in the MAPI properties **PR_SERVICE_DLL_NAME** and **PR_PROVIDER_DLL_NAME**.</span></span>
  
<span data-ttu-id="35f51-115">In beiden-Eigenschaft muss der vollständige Pfad ohne das Suffix "32", sein, da MAPI weiterhin, die an den Dateinamen anfügen, bevor Sie nach der Datei sucht.</span><span class="sxs-lookup"><span data-stu-id="35f51-115">In either property, the full path must be without the suffix "32", because MAPI continues to append that to the filename before looking for your file.</span></span> <span data-ttu-id="35f51-116">Dies bedeutet, dass wenn Sie den Pfad "c:\mypath\myprovider.dll" registrieren, MAPI versucht, "c:\mypath\myprovider32.dll" zu laden.</span><span class="sxs-lookup"><span data-stu-id="35f51-116">This means that if you register the path "c:\mypath\myprovider.dll", MAPI will attempt to load "c:\mypath\myprovider32.dll".</span></span>
  
<span data-ttu-id="35f51-117">Da Outlook MAPI wurde nicht ursprünglich für vollständige Pfade ein entwickelt, sie erreicht diese Einfügung des "32" Suffixes Schlüsseltokens für den ersten Zeitraum in der Zeichenfolge, was bedeutet, dass Pfade mit anderen Perioden arbeiten können, so dass Pfade wie verwendet werden können "c:\my.path\myprovider.dll" oder "c:\mypath\my.provider.dll".</span><span class="sxs-lookup"><span data-stu-id="35f51-117">Because Outlook's MAPI was not originally designed to accommodate full paths, it accomplishes this insertion of the "32" suffix by looking for the first period in the string, which means that paths that contain other periods cannot work, so you cannot use paths such as "c:\my.path\myprovider.dll" or "c:\mypath\my.provider.dll".</span></span>
  
<span data-ttu-id="35f51-118">In einigen Fällen in einem Speicheranbieter generieren Sie mithilfe der **WrapStoreEntryID** -Funktion, die als Parameter den Namen Ihres Anbieters akzeptiert Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="35f51-118">Sometimes in a store provider you will generate entry identifiers using the **WrapStoreEntryID** function, which takes as a parameter the name of your provider.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="35f51-119">Wenn Sie vollständige Pfade in MapiSvc.inf verwenden, müssen Sie denselben Pfad in etwaigen Aufrufen **WrapStoreEntryID**verwenden.</span><span class="sxs-lookup"><span data-stu-id="35f51-119">If you are using full paths in MapiSvc.inf, you must use the same path in any calls to **WrapStoreEntryID**.</span></span> 
  
<span data-ttu-id="35f51-120">Darüber hinaus kann der Pfad, den Sie verwenden in und aus Unicode mithilfe der von der Funktion [GetACP](http://msdn.microsoft.com/de-de/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) bereitgestellte Codepage konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="35f51-120">Additionally, the path you use may be converted to and from Unicode using the code page provided by the [GetACP](http://msdn.microsoft.com/de-de/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) function.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="35f51-121">Sie werden Fehler bemerken, wenn Sie einen Pfad auswählen, der Zeichen enthält, die eine solche eine Schleife durch die Funktionen [MultiByteToWideChar](http://msdn.microsoft.com/de-de/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) und [WideCharToMultiByte](http://msdn.microsoft.com/de-de/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) überstehen kann nicht.</span><span class="sxs-lookup"><span data-stu-id="35f51-121">You will experience failure if you choose a path that contains characters that cannot survive such a roundtrip through the [MultiByteToWideChar](http://msdn.microsoft.com/de-de/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) and [WideCharToMultiByte](http://msdn.microsoft.com/de-de/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) functions.</span></span> 
  
<span data-ttu-id="35f51-122">Für diese Funktionalität veranschaulicht im [Beispiel umgebrochen PST](http://ol2010mapisamples.codeplex.com/) auf CodePlex wurde überarbeitet – die relevante Funktionalität in **MergeWithMapiSvc** und **GenerateProviderPath**ist.</span><span class="sxs-lookup"><span data-stu-id="35f51-122">For a demonstration of this functionality, the [Wrapped PST sample](http://ol2010mapisamples.codeplex.com/) on CodePlex has been revised - the pertinent functionality is in **MergeWithMapiSvc** and **GenerateProviderPath**.</span></span>
  

