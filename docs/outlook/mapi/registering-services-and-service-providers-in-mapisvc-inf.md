---
title: Registrieren von Diensten und Dienstanbietern in MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Letzte Änderung: 18. Juli 2013'
ms.openlocfilehash: adc6318ab36818b4c423bb6b1dc1b083b3fb54eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328371"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a><span data-ttu-id="49dc3-103">Registrieren von Diensten und Dienstanbietern in MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="49dc3-103">Registering Services and Service Providers in MapiSvc.inf</span></span>

 
  
<span data-ttu-id="49dc3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49dc3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49dc3-105">Für die Installation eines neuen Anbieters auf einem System muss die Datei MapiSvc.inf so aktualisiert werden, dass sie auf den neuen Anbieter zeigt.</span><span class="sxs-lookup"><span data-stu-id="49dc3-105">Installing a new provider on a system requires updating the MapiSvc.inf file to point to the new provider.</span></span> <span data-ttu-id="49dc3-106">Standardeigenschaften, die während der Konfiguration festgelegt werden, z. B. die folgenden, informieren MAPI darüber, wo die Dynamic-Link-Bibliothek des Anbieters (.dll):</span><span class="sxs-lookup"><span data-stu-id="49dc3-106">Standard properties set during configuration, which include the following, inform MAPI where to find the provider's dynamic-link library (.dll):</span></span>
  
- <span data-ttu-id="49dc3-107">Die **PR_SERVICE_DLL_NAME** wird im **Abschnitt [Nachrichtendienst]** angegeben.</span><span class="sxs-lookup"><span data-stu-id="49dc3-107">The **PR_SERVICE_DLL_NAME** is specified in the **[Message Service]** section.</span></span> 
    
- <span data-ttu-id="49dc3-108">Die **PR_PROVIDER_DLL_NAME** wird im **Abschnitt [Dienstanbieter]** angegeben.</span><span class="sxs-lookup"><span data-stu-id="49dc3-108">The **PR_PROVIDER_DLL_NAME** is specified in the **[Service Provider]** section.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="49dc3-109">Es wird erwartet, dass Sie den Namen des Anbieternamens .dll (ohne das Suffix "32") festlegen.</span><span class="sxs-lookup"><span data-stu-id="49dc3-109">The expectation is that you set the name of your provider's .dll (without the suffix "32").</span></span> <span data-ttu-id="49dc3-110">MAPI lädt dann Ihren Anbieter, indem Sie ihn auf dem Pfad suchen.</span><span class="sxs-lookup"><span data-stu-id="49dc3-110">MAPI then loads your provider by looking for it on the path.</span></span> 
  
## <a name="putting-a-path-in-mapisvcinf"></a><span data-ttu-id="49dc3-111">Pfad in MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="49dc3-111">Putting a Path in MapiSvc.inf</span></span>

<span data-ttu-id="49dc3-112">Die meisten Anwendungen werden unter Programmdateien installiert und erfordern ein Update der Pfadvariablen, damit MAPI-Anbieter funktionieren können.</span><span class="sxs-lookup"><span data-stu-id="49dc3-112">Most applications install under Program Files, requiring an update to the path variable to allow MAPI providers to work.</span></span> <span data-ttu-id="49dc3-113">Mit einigen Einschränkungen können Microsoft Outlook 2010 und Outlook 2013 vollständige Pfade zu MAPI-Anbietern aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="49dc3-113">With a few restrictions Microsoft Outlook 2010 and Outlook 2013 can accommodate full paths to MAPI providers.</span></span>
  
<span data-ttu-id="49dc3-114">Beim Registrieren Ihres Anbieters in MapiSvc.inf können Sie den vollständigen Pfad zum Anbieter in den MAPI-Eigenschaften **PR_SERVICE_DLL_NAME** und **PR_PROVIDER_DLL_NAME**.</span><span class="sxs-lookup"><span data-stu-id="49dc3-114">When registering your provider in MapiSvc.inf, you could put the full path to the provider in the MAPI properties **PR_SERVICE_DLL_NAME** and **PR_PROVIDER_DLL_NAME**.</span></span>
  
<span data-ttu-id="49dc3-115">In beiden Eigenschaften muss der vollständige Pfad ohne das Suffix "32" sein, da MAPI dies weiterhin an den Dateinamen anfügen muss, bevor sie nach Ihrer Datei sucht.</span><span class="sxs-lookup"><span data-stu-id="49dc3-115">In either property, the full path must be without the suffix "32", because MAPI continues to append that to the filename before looking for your file.</span></span> <span data-ttu-id="49dc3-116">Dies bedeutet, dass MAPI beim Registrieren des Pfads "c:\mypath\myprovider.dll" versucht, "c:\mypath\myprovider32.dll".</span><span class="sxs-lookup"><span data-stu-id="49dc3-116">This means that if you register the path "c:\mypath\myprovider.dll", MAPI will attempt to load "c:\mypath\myprovider32.dll".</span></span>
  
<span data-ttu-id="49dc3-117">Da die MAPI von Outlook ursprünglich nicht für vollständige Pfade vorgesehen war, wird das Suffix "32" eingefügt, indem nach dem ersten Zeitraum in der Zeichenfolge gesucht wird, was bedeutet, dass Pfade, die andere Zeiträume enthalten, nicht funktionieren können, sodass Pfade wie "c:\my.path\myprovider.dll" oder "c:\mypath\my.provider.dll" nicht verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="49dc3-117">Because Outlook's MAPI was not originally designed to accommodate full paths, it accomplishes this insertion of the "32" suffix by looking for the first period in the string, which means that paths that contain other periods cannot work, so you cannot use paths such as "c:\my.path\myprovider.dll" or "c:\mypath\my.provider.dll".</span></span>
  
<span data-ttu-id="49dc3-118">Manchmal generieren Sie in einem Speicheranbieter Eintragsbezeichner mit der **WrapStoreEntryID-Funktion,** die als Parameter den Namen Ihres Anbieters annimmt.</span><span class="sxs-lookup"><span data-stu-id="49dc3-118">Sometimes in a store provider you will generate entry identifiers using the **WrapStoreEntryID** function, which takes as a parameter the name of your provider.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="49dc3-119">Wenn Sie vollständige Pfade in MapiSvc.inf verwenden, müssen Sie bei Aufrufen von **WrapStoreEntryID denselben Pfad verwenden.**</span><span class="sxs-lookup"><span data-stu-id="49dc3-119">If you are using full paths in MapiSvc.inf, you must use the same path in any calls to **WrapStoreEntryID**.</span></span> 
  
<span data-ttu-id="49dc3-120">Darüber hinaus kann der von Ihnen verwendete Pfad mithilfe der Codeseite, die von der [GetACP-Funktion](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) bereitgestellt wird, in Unicode und von Unicode konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="49dc3-120">Additionally, the path you use may be converted to and from Unicode using the code page provided by the [GetACP](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) function.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="49dc3-121">Wenn Sie einen Pfad auswählen, der Zeichen enthält, die einen solchen Roundtrip durch die [Funktionen MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) und [WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) nicht überstehen können, wird ein Fehler gemacht.</span><span class="sxs-lookup"><span data-stu-id="49dc3-121">You will experience failure if you choose a path that contains characters that cannot survive such a roundtrip through the [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) and [WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) functions.</span></span> 
  
<span data-ttu-id="49dc3-122">Für eine Demonstration dieser Funktionalität wurde das Umbrochene [PST-Beispiel](https://github.com/stephenegriffin/Outlook2010CodeSamples) auf GitHub überarbeitet – die entsprechenden Funktionen finden Sie in **MergeWithMapiSvc** und **GenerateProviderPath**.</span><span class="sxs-lookup"><span data-stu-id="49dc3-122">For a demonstration of this functionality, the [Wrapped PST sample](https://github.com/stephenegriffin/Outlook2010CodeSamples) on GitHub has been revised - the pertinent functionality is in **MergeWithMapiSvc** and **GenerateProviderPath**.</span></span>
  

