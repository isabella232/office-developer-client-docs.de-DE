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
ms.openlocfilehash: 394537a60f4cb9603024115ccea67570291d8ac6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270042"
---
# <a name="linking-to-the-mapi-dlls"></a><span data-ttu-id="d64eb-103">Verknüpfen mit MAPI-DLL-Dateien</span><span class="sxs-lookup"><span data-stu-id="d64eb-103">Linking to the MAPI DLLs</span></span>

  
  
<span data-ttu-id="d64eb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d64eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d64eb-105">MAPI-Clients können implizit oder explizit mithilfe der Windows-Funktionen **LoadLibrary** und **GetProcAddress**eine Verknüpfung zu den MAPI-DLLs herstellen.</span><span class="sxs-lookup"><span data-stu-id="d64eb-105">MAPI clients can link to the MAPI DLLs implicitly, or explicitly by using the Windows functions **LoadLibrary** and **GetProcAddress**.</span></span> <span data-ttu-id="d64eb-106">Informationen zum expliziten Verknüpfen von MAPI-DLLs finden Sie unter [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span><span class="sxs-lookup"><span data-stu-id="d64eb-106">For information on explicitly linking MAPI DLLs, see [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
  
<span data-ttu-id="d64eb-107">MAPI stellt typdefinitions Anweisungen in der MAPIX bereit. H-Headerdatei für jede der folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="d64eb-107">MAPI provides type definition statements in the MAPIX.H header file for each of the following functions:</span></span>
  
[<span data-ttu-id="d64eb-108">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="d64eb-108">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="d64eb-109">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="d64eb-109">MAPIUninitialize</span></span>](mapiuninitialize.md)
  
[<span data-ttu-id="d64eb-110">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="d64eb-110">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="d64eb-111">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="d64eb-111">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="d64eb-112">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="d64eb-112">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="d64eb-113">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d64eb-113">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d64eb-114">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="d64eb-114">MAPIAdminProfiles</span></span>](mapiadminprofiles.md)
  
<span data-ttu-id="d64eb-115">Verwenden Sie diese Typdefinitionen, um die entsprechenden Einstiegspunkte richtig aufzurufen, wenn Sie explizit mit den MAPI-DLLs verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="d64eb-115">Use these type definitions to correctly call the corresponding entry points if you link explicitly to the MAPI DLLs.</span></span>
  
<span data-ttu-id="d64eb-116">Dienstanbieter können nicht-MAPI-Funktionen enthalten, die vollständig mit MAPI in Verbindung stehen (in Ihrer DLL).</span><span class="sxs-lookup"><span data-stu-id="d64eb-116">Service providers can contain non-MAPI functionality — features that are completely unrelated to MAPI — in their DLL.</span></span> <span data-ttu-id="d64eb-117">Wenn Sie diese Funktionen verwenden müssen, rufen Sie **LoadLibrary** vor der Verwendung der dll und **FreeLibrary** , um die dll aus dem Speicher nach ihrer Verwendung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="d64eb-117">If you need to use these features, call **LoadLibrary** before using the DLL and **FreeLibrary** to remove the DLL from memory after its use.</span></span> <span data-ttu-id="d64eb-118">Da MAPI die nicht-MAPI-Verwendung einer Dienstanbieter-DLL nicht kennt, gibt es keine Garantie dafür, dass die DLL bei Bedarf verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d64eb-118">Because MAPI is unaware of non-MAPI uses of a service provider DLL, there is no guarantee that the DLL will be available when needed.</span></span> <span data-ttu-id="d64eb-119">MAPI gibt eine Dienstanbieter-DLL frei, wenn es keine Clients mit aktiven Sitzungen mehr gibt, die deren Dienste erfordern.</span><span class="sxs-lookup"><span data-stu-id="d64eb-119">MAPI releases a service provider DLL when there are no longer any clients with active sessions that require its services.</span></span> 
  

