---
title: Verknüpfen mit MAPI-DLL-Dateien
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19fd4678-21d3-47a6-a439-1d4959cac407
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 428e92dd783368374fa07c8df9629d60e83dd217
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582028"
---
# <a name="linking-to-the-mapi-dlls"></a><span data-ttu-id="21148-103">Verknüpfen mit MAPI-DLL-Dateien</span><span class="sxs-lookup"><span data-stu-id="21148-103">Linking to the MAPI DLLs</span></span>

  
  
<span data-ttu-id="21148-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21148-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21148-105">MAPI-Clients können mit der MAPI-DLLs implizit oder explizit verknüpfen mithilfe der Windows-Funktionen **LoadLibrary** und **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="21148-105">MAPI clients can link to the MAPI DLLs implicitly, or explicitly by using the Windows functions **LoadLibrary** and **GetProcAddress**.</span></span> <span data-ttu-id="21148-106">Informationen zum Verknüpfen explizit MAPI-DLLs finden Sie unter [Link zu MAPI-Funktionen](how-to-link-to-mapi-functions.md).</span><span class="sxs-lookup"><span data-stu-id="21148-106">For information on explicitly linking MAPI DLLs, see [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
  
<span data-ttu-id="21148-107">MAPI bietet Typ-Definition-Anweisungen in der MAPIX. H-Headerdatei für jede der folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="21148-107">MAPI provides type definition statements in the MAPIX.H header file for each of the following functions:</span></span>
  
[<span data-ttu-id="21148-108">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="21148-108">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="21148-109">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="21148-109">MAPIUninitialize</span></span>](mapiuninitialize.md)
  
[<span data-ttu-id="21148-110">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="21148-110">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="21148-111">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="21148-111">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="21148-112">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="21148-112">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="21148-113">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="21148-113">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="21148-114">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="21148-114">MAPIAdminProfiles</span></span>](mapiadminprofiles.md)
  
<span data-ttu-id="21148-115">Verwenden Sie diese Typdefinitionen ordnungsgemäß die entsprechenden Einstiegspunkte aufrufen, wenn Sie explizit MAPI-DLLs verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="21148-115">Use these type definitions to correctly call the corresponding entry points if you link explicitly to the MAPI DLLs.</span></span>
  
<span data-ttu-id="21148-116">Dienstanbieter können nicht-MAPI-Funktionalität enthalten – Features, die nicht vollständig im Zusammenhang mit MAPI sind – in ihre DLL-Datei.</span><span class="sxs-lookup"><span data-stu-id="21148-116">Service providers can contain non-MAPI functionality — features that are completely unrelated to MAPI — in their DLL.</span></span> <span data-ttu-id="21148-117">Wenn Sie diese Features verwenden müssen, rufen Sie **LoadLibrary** , bevor Sie mit der DLL und **FreeLibrary** nach dessen Verwendung die DLL aus dem Speicher entfernt.</span><span class="sxs-lookup"><span data-stu-id="21148-117">If you need to use these features, call **LoadLibrary** before using the DLL and **FreeLibrary** to remove the DLL from memory after its use.</span></span> <span data-ttu-id="21148-118">Da MAPI-MAPI-Verwendungsmöglichkeiten von einem Dienstanbieter DLL nicht bekannt ist, besteht keine Garantie, dass die DLL bei Bedarf zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="21148-118">Because MAPI is unaware of non-MAPI uses of a service provider DLL, there is no guarantee that the DLL will be available when needed.</span></span> <span data-ttu-id="21148-119">MAPI wieder einem Dienstanbieter DLL aufgehoben werden nicht mehr von Clients mit aktiver Sitzungen, die die Dienste erfordern.</span><span class="sxs-lookup"><span data-stu-id="21148-119">MAPI releases a service provider DLL when there are no longer any clients with active sessions that require its services.</span></span> 
  

