---
title: Verwenden von threadsicheren Objekten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4a66f892043b9a90893a60f3fa6ba69ea6457f5a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795846"
---
# <a name="using-thread-safe-objects"></a><span data-ttu-id="2e37f-103">Verwenden von threadsicheren Objekten</span><span class="sxs-lookup"><span data-stu-id="2e37f-103">Using Thread-Safe Objects</span></span>

  
  
<span data-ttu-id="2e37f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2e37f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2e37f-105">Clientanwendungen können davon ausgehen, dass Objekte direkt verwendet oder als Rückrufe immer threadsicheren außer in den folgenden Fällen sind:</span><span class="sxs-lookup"><span data-stu-id="2e37f-105">Client applications can assume that objects used directly or as callbacks are always thread-safe except in the following cases:</span></span>
  
- <span data-ttu-id="2e37f-106">Eines Transportdienstes-Objekt, der durch einen Clientaufruf von [IMAPISession::OpenEntry](imapisession-openentry.md) mit einem Eintrag Bezeichner aus der Anbieter Status Tabellenzeile abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2e37f-106">A transport provider's status object obtained through a client call to [IMAPISession::OpenEntry](imapisession-openentry.md) with an entry identifier from the provider's status table row.</span></span> 
    
- <span data-ttu-id="2e37f-107">Alle MAPI-Formular-Objekten, die durch einen Clientaufruf [MAPIOpenFormMgr](mapiopenformmgr.md).</span><span class="sxs-lookup"><span data-stu-id="2e37f-107">All MAPI form objects obtained through a client call to [MAPIOpenFormMgr](mapiopenformmgr.md).</span></span> <span data-ttu-id="2e37f-108">Formular-Objekte gelten des Apartmentthreading Model Regeln und Clients müssen sie und alle Objekte, die von ihnen enthalten sind, nur in dem Thread, die sie erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="2e37f-108">Form objects obey apartment model rules and clients must use them and all objects contained by them only on the thread that created them.</span></span>
    
<span data-ttu-id="2e37f-109">Wenn ein Client eines Transportdienstes Zeile in der Tabelle "Status", die die Eintrags-ID des zugeordneten Status-Objekts enthält zugreift, kann der Client **OpenEntry** mit dieses Eintrags-ID zum Öffnen des Status-Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2e37f-109">When a client accesses a transport provider's row in the status table that includes the entry identifier of the associated status object, the client can call **OpenEntry** with that entry identifier to open the status object.</span></span> <span data-ttu-id="2e37f-110">In diesem Statusobjekt ist nicht threadsicheren, da Transportanbieter im Zusammenhang mit der MAPI-Warteschlange ausführen und einen separaten Kontext für ihren Statusobjekt nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="2e37f-110">This status object is not thread-safe because transport providers run in the context of the MAPI spooler and do not maintain a separate context for their status object.</span></span> <span data-ttu-id="2e37f-111">Das Statusobjekt des Apartmentthreading Model Regeln erfüllt und Clients müssen nur auf Threads, der es erstellt.</span><span class="sxs-lookup"><span data-stu-id="2e37f-111">The status object obeys apartment model rules and clients must use it only on the thread that created it.</span></span> 
  
<span data-ttu-id="2e37f-112">Ein Client muss auch ["MAPIInitialize"](mapiinitialize.md) auf jedem Thread aufrufen, um vor der Nutzung jeglicher MAPI-Objekten und [MAPIUninitialize](mapiuninitialize.md) nach Abschluss der, die verwenden.</span><span class="sxs-lookup"><span data-stu-id="2e37f-112">A client must also invoke [MAPIInitialize](mapiinitialize.md) on every thread before using any MAPI objects and [MAPIUninitialize](mapiuninitialize.md) when that use is complete.</span></span> <span data-ttu-id="2e37f-113">Diese Aufrufe erfolgen soll, auch wenn die Objekte, die verwendet werden, an der Thread aus einer externen Quelle übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="2e37f-113">These calls should be made even if the objects to be used are passed to the thread from an external source.</span></span> <span data-ttu-id="2e37f-114">**"MAPIInitialize"** und **MAPIUninitialize** kann aus an einer beliebigen Stelle mit Ausnahme von innerhalb einer Win32 **DllMain** -Funktion eine Funktion aufgerufen werden, die vom System beim Prozesse und Threads initialisiert und beendet sind oder beim Aufrufen der **aufgerufen wird LoadLibrary** und **FreeLibrary** Funktionen.</span><span class="sxs-lookup"><span data-stu-id="2e37f-114">**MAPIInitialize** and **MAPIUninitialize** can be called from anywhere except from within a Win32 **DllMain** function, a function that is invoked by the system when processes and threads are initialized and terminated, or upon calls to the **LoadLibrary** and **FreeLibrary** functions.</span></span> 
  
<span data-ttu-id="2e37f-115">Indirekte Verwenden von Objekten sollte niemals Threadsicherheit vorgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2e37f-115">Indirect use objects should never be assumed to be thread-safe.</span></span> <span data-ttu-id="2e37f-116">Indirekte Verwenden von Objekten werden von Methoden zurückgegeben, die Ziel-Schnittstellenzeiger als Eingabeparameter benötigen.</span><span class="sxs-lookup"><span data-stu-id="2e37f-116">Indirect use objects are returned by methods that require destination interface pointers as input parameters.</span></span> <span data-ttu-id="2e37f-117">Beispiele für solche Methoden sind **IMAPIProp::CopyTo** und **CopyProps**, **IMAPIFolder::CopyFolder** und **CopyMessage**und **IMsgServiceAdmin::CopyMsgService**.</span><span class="sxs-lookup"><span data-stu-id="2e37f-117">Examples of such methods are **IMAPIProp::CopyTo** and **CopyProps**, **IMAPIFolder::CopyFolder** and **CopyMessage**, and **IMsgServiceAdmin::CopyMsgService**.</span></span> <span data-ttu-id="2e37f-118">Wenn ein Dienstanbieter solches Objekt von einem Thread aufrufen als den, auf dem es übergeben wurde möchte, ist der Anbieter für das Objekt explizit Marshallen verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="2e37f-118">If a service provider wants to call such an object from a thread other than the one on which it was passed, the provider is responsible for explicitly marshaling the object.</span></span>
  

