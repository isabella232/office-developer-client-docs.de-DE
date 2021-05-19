---
title: Verwenden Thread-Safe Objekten
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
# <a name="using-thread-safe-objects"></a><span data-ttu-id="c35a5-103">Verwenden Thread-Safe Objekten</span><span class="sxs-lookup"><span data-stu-id="c35a5-103">Using Thread-Safe Objects</span></span>

  
  
<span data-ttu-id="c35a5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c35a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c35a5-105">Clientanwendungen können davon ausgehen, dass objekte, die direkt oder als Rückrufe verwendet werden, immer threadsicher sind, außer in den folgenden Fällen:</span><span class="sxs-lookup"><span data-stu-id="c35a5-105">Client applications can assume that objects used directly or as callbacks are always thread-safe except in the following cases:</span></span>
  
- <span data-ttu-id="c35a5-106">Das Statusobjekt eines Transportanbieters, das über einen Clientaufruf von [IMAPISession::OpenEntry](imapisession-openentry.md) mit einem Eintragsbezeichner aus der Statustabelle des Anbieters erhalten wurde.</span><span class="sxs-lookup"><span data-stu-id="c35a5-106">A transport provider's status object obtained through a client call to [IMAPISession::OpenEntry](imapisession-openentry.md) with an entry identifier from the provider's status table row.</span></span> 
    
- <span data-ttu-id="c35a5-107">Alle MAPI-Formularobjekte, die über einen Clientaufruf von [MAPIOpenFormMgr erhalten wurden.](mapiopenformmgr.md)</span><span class="sxs-lookup"><span data-stu-id="c35a5-107">All MAPI form objects obtained through a client call to [MAPIOpenFormMgr](mapiopenformmgr.md).</span></span> <span data-ttu-id="c35a5-108">Formularobjekte befolgen Apartmentmodellregeln, und Clients müssen sie und alle darin enthaltenen Objekte nur im Thread verwenden, von dem sie erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="c35a5-108">Form objects obey apartment model rules and clients must use them and all objects contained by them only on the thread that created them.</span></span>
    
<span data-ttu-id="c35a5-109">Wenn ein Client auf die Zeile eines Transportanbieters in der Statustabelle zutritt, die die Eintrags-ID des zugeordneten Statusobjekts enthält, kann der Client **OpenEntry** mit diesem Eintragsbezeichner aufrufen, um das Statusobjekt zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c35a5-109">When a client accesses a transport provider's row in the status table that includes the entry identifier of the associated status object, the client can call **OpenEntry** with that entry identifier to open the status object.</span></span> <span data-ttu-id="c35a5-110">Dieses Statusobjekt ist nicht threadsicher, da Transportanbieter im Kontext des MAPI-Spoolers ausgeführt werden und keinen separaten Kontext für ihr Statusobjekt beibehalten.</span><span class="sxs-lookup"><span data-stu-id="c35a5-110">This status object is not thread-safe because transport providers run in the context of the MAPI spooler and do not maintain a separate context for their status object.</span></span> <span data-ttu-id="c35a5-111">Das status-Objekt befolgt Apartmentmodellregeln, und Clients dürfen es nur für den Thread verwenden, von dem es erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c35a5-111">The status object obeys apartment model rules and clients must use it only on the thread that created it.</span></span> 
  
<span data-ttu-id="c35a5-112">Ein Client muss [mapIInitialize](mapiinitialize.md) auch in jedem Thread aufrufen, bevor mapI-Objekte verwendet werden und [MAPIUninitialize,](mapiuninitialize.md) wenn diese Verwendung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c35a5-112">A client must also invoke [MAPIInitialize](mapiinitialize.md) on every thread before using any MAPI objects and [MAPIUninitialize](mapiuninitialize.md) when that use is complete.</span></span> <span data-ttu-id="c35a5-113">Diese Aufrufe sollten auch dann ausgeführt werden, wenn die zu verwendenden Objekte von einer externen Quelle an den Thread übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="c35a5-113">These calls should be made even if the objects to be used are passed to the thread from an external source.</span></span> <span data-ttu-id="c35a5-114">**MAPIInitialize** und **MAPIUninitialize** können von überall aufgerufen werden, mit Ausnahme einer Win32 **DllMain-Funktion,** einer Funktion, die vom System aufgerufen wird, wenn Prozesse und Threads initialisiert und beendet werden, oder bei Aufrufen der **LoadLibrary-** und **FreeLibrary-Funktionen.**</span><span class="sxs-lookup"><span data-stu-id="c35a5-114">**MAPIInitialize** and **MAPIUninitialize** can be called from anywhere except from within a Win32 **DllMain** function, a function that is invoked by the system when processes and threads are initialized and terminated, or upon calls to the **LoadLibrary** and **FreeLibrary** functions.</span></span> 
  
<span data-ttu-id="c35a5-115">Indirekte Verwendungsobjekte sollten niemals als threadsicher angenommen werden.</span><span class="sxs-lookup"><span data-stu-id="c35a5-115">Indirect use objects should never be assumed to be thread-safe.</span></span> <span data-ttu-id="c35a5-116">Indirekte Verwendungsobjekte werden von Methoden zurückgegeben, für die Zielschnittstellenzeiger als Eingabeparameter erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c35a5-116">Indirect use objects are returned by methods that require destination interface pointers as input parameters.</span></span> <span data-ttu-id="c35a5-117">Beispiele für solche Methoden sind **IMAPIProp::CopyTo** und **CopyProps**, **IMAPIFolder::CopyFolder** und **CopyMessage** und **IMsgServiceAdmin::CopyMsgService**.</span><span class="sxs-lookup"><span data-stu-id="c35a5-117">Examples of such methods are **IMAPIProp::CopyTo** and **CopyProps**, **IMAPIFolder::CopyFolder** and **CopyMessage**, and **IMsgServiceAdmin::CopyMsgService**.</span></span> <span data-ttu-id="c35a5-118">Wenn ein Dienstanbieter ein solches Objekt von einem anderen Thread als dem Thread aufrufen möchte, an den es übergeben wurde, ist der Anbieter für das explizite Marshalling des Objekts verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="c35a5-118">If a service provider wants to call such an object from a thread other than the one on which it was passed, the provider is responsible for explicitly marshaling the object.</span></span>
  

