---
title: Abrufen von Formulareigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 023d2cf312438b1e4b6a90c57e1ead7d606d7727
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328651"
---
# <a name="retrieving-form-properties"></a><span data-ttu-id="9ebf2-103">Abrufen von Formulareigenschaften</span><span class="sxs-lookup"><span data-stu-id="9ebf2-103">Retrieving Form Properties</span></span>

  
  
<span data-ttu-id="9ebf2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ebf2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ebf2-105">Zum Ausgeben einer Abfrage, die für einen benutzerdefinierten Nachrichtentyp sinnvoll ist, muss eine Anwendung die Eigenschaften kennen, die in dieser Nachricht erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="9ebf2-105">To issue a query that is meaningful to a custom message type, an application needs to know the properties that are expected on that message.</span></span> <span data-ttu-id="9ebf2-106">Eine Clientanwendung fragt den MAPI-Formular-Manager ab, um eine Liste der Eigenschaften abzurufen, die von einer benutzerdefinierten Nachrichtenklasse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ebf2-106">To get a list of properties that a custom message class uses, a client application queries the MAPI form manager.</span></span> <span data-ttu-id="9ebf2-107">Der Formular-Manager ruft diese Informationen aus der entsprechenden Formular Konfigurationsdatei ab, sodass Clientanwendungen diese Informationen ohne den Aufwand der Aktivierung des Formular Servers selbst verwenden können.</span><span class="sxs-lookup"><span data-stu-id="9ebf2-107">The form manager gets this information from the appropriate form configuration file so that client applications can use this information without the overhead of activating the form server itself.</span></span> <span data-ttu-id="9ebf2-108">Zu diesem Zweck Ruft die Clientanwendung die [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) -Methode wie folgt auf:</span><span class="sxs-lookup"><span data-stu-id="9ebf2-108">To do this, the client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method as follows:</span></span> 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

<span data-ttu-id="9ebf2-109">Beachten Sie, dass das dritte Argument für **ResolveMessageClass** der Ordner ist, in dem die Tabelle mit den zugeordneten Inhalten enthalten ist, die von der Abfrage nach Formular Servern durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="9ebf2-109">Note that the third argument to **ResolveMessageClass** is the folder that contains the associated contents table that the query will search for form servers.</span></span> <span data-ttu-id="9ebf2-110">NULL gibt an, dass der Formular-Manager alle verfügbaren Formular Container durchsuchen soll.</span><span class="sxs-lookup"><span data-stu-id="9ebf2-110">NULL indicates that the form manager should search all available form containers.</span></span> <span data-ttu-id="9ebf2-111">Wenn die Abfrage für einen bestimmten Ordner ausgeführt werden soll, empfiehlt es sich, stattdessen den entsprechenden [IMAPIFolder](imapifolderimapicontainer.md) -Zeiger einzufügen.</span><span class="sxs-lookup"><span data-stu-id="9ebf2-111">If the query is to run against a particular folder, it is better to include the appropriate [IMAPIFolder](imapifolderimapicontainer.md) pointer instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9ebf2-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ebf2-112">See also</span></span>



[<span data-ttu-id="9ebf2-113">Formular Server interAktionen</span><span class="sxs-lookup"><span data-stu-id="9ebf2-113">Form Server Interactions</span></span>](form-server-interactions.md)

