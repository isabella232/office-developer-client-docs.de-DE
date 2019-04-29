---
title: Verwenden von Thread sicheren Objekten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 611e0a49f0fd8df8fe40205a33ed5501055c3d45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425169"
---
# <a name="using-thread-safe-objects"></a><span data-ttu-id="c96a1-103">Verwenden von Thread sicheren Objekten</span><span class="sxs-lookup"><span data-stu-id="c96a1-103">Using Thread-Safe Objects</span></span>

  
  
<span data-ttu-id="c96a1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c96a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c96a1-105">Client Anwendungen können davon ausgehen, dass Objekte, die direkt oder als Rückrufe verwendet werden, nur in den folgenden Fällen threadsicher sind:</span><span class="sxs-lookup"><span data-stu-id="c96a1-105">Client applications can assume that objects used directly or as callbacks are always thread-safe except in the following cases:</span></span>
  
- <span data-ttu-id="c96a1-106">Das Statusobjekt eines Transportanbieters, das über einen Clientaufruf von [IMAPISession:: OpenEntry](imapisession-openentry.md) mit einer Eintrags-ID aus der Statustabellen Zeile des Anbieters abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c96a1-106">A transport provider's status object obtained through a client call to [IMAPISession::OpenEntry](imapisession-openentry.md) with an entry identifier from the provider's status table row.</span></span> 
    
- <span data-ttu-id="c96a1-107">Alle MAPI-Formularobjekte, die über einen Clientaufruf an [MAPIOpenFormMgr](mapiopenformmgr.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c96a1-107">All MAPI form objects obtained through a client call to [MAPIOpenFormMgr](mapiopenformmgr.md).</span></span> <span data-ttu-id="c96a1-108">Formularobjekte gehorchen Apartmentmodell Regeln, und Clients müssen diese und alle darin enthaltenen Objekte nur für den Thread verwenden, der Sie erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="c96a1-108">Form objects obey apartment model rules and clients must use them and all objects contained by them only on the thread that created them.</span></span>
    
<span data-ttu-id="c96a1-109">Wenn ein Client in der Statustabelle, die die Eintrags-ID des zugeordneten Status Objekts enthält, auf die Zeile eines Transportanbieters zugreift \*\*\*\* , kann der Client OpenEntry mit dieser Eintrags-ID aufrufen, um das Status-Objekt zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c96a1-109">When a client accesses a transport provider's row in the status table that includes the entry identifier of the associated status object, the client can call **OpenEntry** with that entry identifier to open the status object.</span></span> <span data-ttu-id="c96a1-110">Dieses Statusobjekt ist nicht threadsicher, da Transportanbieter im Kontext des MAPI-Spoolers ausgeführt werden und keinen separaten Kontext für Ihr Status-Objekt beibehalten.</span><span class="sxs-lookup"><span data-stu-id="c96a1-110">This status object is not thread-safe because transport providers run in the context of the MAPI spooler and do not maintain a separate context for their status object.</span></span> <span data-ttu-id="c96a1-111">Das Status-Objekt befolgt Apartmentmodell Regeln, und Clients müssen es nur für den Thread verwenden, der es erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="c96a1-111">The status object obeys apartment model rules and clients must use it only on the thread that created it.</span></span> 
  
<span data-ttu-id="c96a1-112">Ein Client muss [MAPIInitialize](mapiinitialize.md) auch für jeden Thread aufrufen, bevor MAPI-Objekte und [MAPIUninitialize](mapiuninitialize.md) verwendet werden, wenn die Verwendung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c96a1-112">A client must also invoke [MAPIInitialize](mapiinitialize.md) on every thread before using any MAPI objects and [MAPIUninitialize](mapiuninitialize.md) when that use is complete.</span></span> <span data-ttu-id="c96a1-113">Diese Aufrufe sollten auch dann vorgenommen werden, wenn die zu verwendenden Objekte aus einer externen Quelle an den Thread übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="c96a1-113">These calls should be made even if the objects to be used are passed to the thread from an external source.</span></span> <span data-ttu-id="c96a1-114">**MAPIInitialize** und **MAPIUninitialize** können von überall aus aufgerufen werden, außer innerhalb einer Win32- **DllMain** -Funktion, eine Funktion, die vom System aufgerufen wird, wenn Prozesse und Threads initialisiert und beendet werden, oder bei Aufrufen der \*\* LoadLibrary\*\* -und **FreeLibrary** -Funktionen.</span><span class="sxs-lookup"><span data-stu-id="c96a1-114">**MAPIInitialize** and **MAPIUninitialize** can be called from anywhere except from within a Win32 **DllMain** function, a function that is invoked by the system when processes and threads are initialized and terminated, or upon calls to the **LoadLibrary** and **FreeLibrary** functions.</span></span> 
  
<span data-ttu-id="c96a1-115">InDirekte use-Objekte sollten nie als threadsicher angenommen werden.</span><span class="sxs-lookup"><span data-stu-id="c96a1-115">Indirect use objects should never be assumed to be thread-safe.</span></span> <span data-ttu-id="c96a1-116">InDirekte use-Objekte werden von Methoden zurückgegeben, die Ziel Schnittstellenzeiger als Eingabeparameter erfordern.</span><span class="sxs-lookup"><span data-stu-id="c96a1-116">Indirect use objects are returned by methods that require destination interface pointers as input parameters.</span></span> <span data-ttu-id="c96a1-117">Beispiele für solche Methoden sind **IMAPIProp:: CopyTo** und **CopyProps**, **IMAPIFolder:: CopyFolder** und **CopyMessage**und **IMsgServiceAdmin:: CopyMsgService**.</span><span class="sxs-lookup"><span data-stu-id="c96a1-117">Examples of such methods are **IMAPIProp::CopyTo** and **CopyProps**, **IMAPIFolder::CopyFolder** and **CopyMessage**, and **IMsgServiceAdmin::CopyMsgService**.</span></span> <span data-ttu-id="c96a1-118">Wenn ein Dienstanbieter ein solches Objekt aus einem anderen Thread als dem, an dem es übergeben wurde, aufrufen möchte, ist er dafür verantwortlich, das Objekt explizit zu marshallen.</span><span class="sxs-lookup"><span data-stu-id="c96a1-118">If a service provider wants to call such an object from a thread other than the one on which it was passed, the provider is responsible for explicitly marshaling the object.</span></span>
  

