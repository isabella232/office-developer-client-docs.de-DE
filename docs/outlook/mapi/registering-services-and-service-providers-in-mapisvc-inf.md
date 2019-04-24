---
title: Registrieren von Diensten und Dienstanbietern in MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Zuletzt geändert: 18, 2013'
ms.openlocfilehash: adc6318ab36818b4c423bb6b1dc1b083b3fb54eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328371"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a><span data-ttu-id="01d86-103">Registrieren von Diensten und Dienstanbietern in MapiSvc. inf</span><span class="sxs-lookup"><span data-stu-id="01d86-103">Registering Services and Service Providers in MapiSvc.inf</span></span>

 
  
<span data-ttu-id="01d86-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01d86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01d86-105">Für die Installation eines neuen Anbieters auf einem System muss die Datei MapiSvc. inf aktualisiert werden, damit auf den neuen Anbieter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="01d86-105">Installing a new provider on a system requires updating the MapiSvc.inf file to point to the new provider.</span></span> <span data-ttu-id="01d86-106">Standard Eigenschaften, die während der Konfiguration festgelegt werden, einschließlich der folgenden, informieren Sie MAPI, wo die Dynamic-Link-Bibliothek des Anbieters (dll) zu finden ist:</span><span class="sxs-lookup"><span data-stu-id="01d86-106">Standard properties set during configuration, which include the following, inform MAPI where to find the provider's dynamic-link library (.dll):</span></span>
  
- <span data-ttu-id="01d86-107">Die **PR_SERVICE_DLL_NAME** wird im Abschnitt **[Message Service]** angegeben.</span><span class="sxs-lookup"><span data-stu-id="01d86-107">The **PR_SERVICE_DLL_NAME** is specified in the **[Message Service]** section.</span></span> 
    
- <span data-ttu-id="01d86-108">Die **PR_PROVIDER_DLL_NAME** wird im Abschnitt **[Service Provider]** angegeben.</span><span class="sxs-lookup"><span data-stu-id="01d86-108">The **PR_PROVIDER_DLL_NAME** is specified in the **[Service Provider]** section.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="01d86-109">Es wird davon ausgegangen, dass Sie den Namen der dll Ihres Anbieters (ohne Suffix "32") festlegen.</span><span class="sxs-lookup"><span data-stu-id="01d86-109">The expectation is that you set the name of your provider's .dll (without the suffix "32").</span></span> <span data-ttu-id="01d86-110">MAPI lädt dann Ihren Anbieter, indem er nach dem Pfad sucht.</span><span class="sxs-lookup"><span data-stu-id="01d86-110">MAPI then loads your provider by looking for it on the path.</span></span> 
  
## <a name="putting-a-path-in-mapisvcinf"></a><span data-ttu-id="01d86-111">Einfügen eines Pfads in MapiSvc. inf</span><span class="sxs-lookup"><span data-stu-id="01d86-111">Putting a Path in MapiSvc.inf</span></span>

<span data-ttu-id="01d86-112">Die meisten Anwendungen werden Unterprogramm Dateien installiert, wobei eine Aktualisierung der PATH-Variablen erforderlich ist, damit MAPI-Anbieter arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="01d86-112">Most applications install under Program Files, requiring an update to the path variable to allow MAPI providers to work.</span></span> <span data-ttu-id="01d86-113">Mit einigen Einschränkungen können Microsoft Outlook 2010 und Outlook 2013 vollständige Pfade zu MAPI-Anbietern aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="01d86-113">With a few restrictions Microsoft Outlook 2010 and Outlook 2013 can accommodate full paths to MAPI providers.</span></span>
  
<span data-ttu-id="01d86-114">Wenn Sie Ihren Anbieter in MapiSvc. inf registrieren, können Sie den vollständigen Pfad zum Anbieter in den MAPI-Eigenschaften **PR_SERVICE_DLL_NAME** und **PR_PROVIDER_DLL_NAME**.</span><span class="sxs-lookup"><span data-stu-id="01d86-114">When registering your provider in MapiSvc.inf, you could put the full path to the provider in the MAPI properties **PR_SERVICE_DLL_NAME** and **PR_PROVIDER_DLL_NAME**.</span></span>
  
<span data-ttu-id="01d86-115">In beiden Eigenschaften muss der vollständige Pfad ohne das Suffix "32" sein, da MAPI die Datei weiterhin an den Dateinamen anhängt, bevor Sie nach Ihrer Daten sucht.</span><span class="sxs-lookup"><span data-stu-id="01d86-115">In either property, the full path must be without the suffix "32", because MAPI continues to append that to the filename before looking for your file.</span></span> <span data-ttu-id="01d86-116">Wenn Sie also den Pfad "c:\mypath\myprovider.dll" registrieren, versucht MAPI, "c:\mypath\myprovider32.dll" zu laden.</span><span class="sxs-lookup"><span data-stu-id="01d86-116">This means that if you register the path "c:\mypath\myprovider.dll", MAPI will attempt to load "c:\mypath\myprovider32.dll".</span></span>
  
<span data-ttu-id="01d86-117">Da die MAPI von Outlook ursprünglich nicht für vollständige Pfade konzipiert wurde, führt Sie diese Einfügung des Suffixes "32" durch, indem Sie nach dem ersten Punkt in der Zeichenfolge sucht, was heißt, dass Pfade, die andere Punkte enthalten, nicht funktionieren können, sodass Sie keine Pfade wie "c:\My.path\myprovider.dll" oder "c:\mypath\my.Provider.dll".</span><span class="sxs-lookup"><span data-stu-id="01d86-117">Because Outlook's MAPI was not originally designed to accommodate full paths, it accomplishes this insertion of the "32" suffix by looking for the first period in the string, which means that paths that contain other periods cannot work, so you cannot use paths such as "c:\my.path\myprovider.dll" or "c:\mypath\my.provider.dll".</span></span>
  
<span data-ttu-id="01d86-118">Manchmal werden Sie in einem Informationsspeicher Anbieter Eingabe-IDs mithilfe der **WrapStoreEntryID** -Funktion generieren, die als Parameter den Namen Ihres Anbieters verwendet.</span><span class="sxs-lookup"><span data-stu-id="01d86-118">Sometimes in a store provider you will generate entry identifiers using the **WrapStoreEntryID** function, which takes as a parameter the name of your provider.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="01d86-119">Wenn Sie in MapiSvc. inf vollständige Pfade verwenden, müssen Sie den gleichen Pfad in allen Aufrufen von **WrapStoreEntryID**verwenden.</span><span class="sxs-lookup"><span data-stu-id="01d86-119">If you are using full paths in MapiSvc.inf, you must use the same path in any calls to **WrapStoreEntryID**.</span></span> 
  
<span data-ttu-id="01d86-120">Darüber hinaus kann der verwendete Pfad mithilfe der Codeseite, die von der [GetACP](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) -Funktion bereitgestellt wird, in und aus Unicode konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="01d86-120">Additionally, the path you use may be converted to and from Unicode using the code page provided by the [GetACP](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) function.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="01d86-121">Wenn Sie einen Pfad auswählen, der Zeichen enthält, die einen solchen Roundtrip über die [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) -und [WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) -Funktionen nicht überstehen können, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="01d86-121">You will experience failure if you choose a path that contains characters that cannot survive such a roundtrip through the [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) and [WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) functions.</span></span> 
  
<span data-ttu-id="01d86-122">Für eine Demonstration dieser Funktionalität wurde das [Wrapped PST-Beispiel](https://github.com/stephenegriffin/Outlook2010CodeSamples) auf GitHub überarbeitet – die entsprechende Funktionalität befindet sich in **MergeWithMapiSvc** und **GenerateProviderPath**.</span><span class="sxs-lookup"><span data-stu-id="01d86-122">For a demonstration of this functionality, the [Wrapped PST sample](https://github.com/stephenegriffin/Outlook2010CodeSamples) on GitHub has been revised - the pertinent functionality is in **MergeWithMapiSvc** and **GenerateProviderPath**.</span></span>
  

