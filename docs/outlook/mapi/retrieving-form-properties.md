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
ms.openlocfilehash: 334ecaacec88c3730f4cc2f4c80eb35d5a553c4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795401"
---
# <a name="retrieving-form-properties"></a><span data-ttu-id="84c37-103">Abrufen von Formulareigenschaften</span><span class="sxs-lookup"><span data-stu-id="84c37-103">Retrieving Form Properties</span></span>

  
  
<span data-ttu-id="84c37-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="84c37-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="84c37-105">Zum Ausführen eine Abfrage, die in einem benutzerdefinierten Nachrichtentyp sinnvoll ist, muss eine Anwendung die Eigenschaften kennen, die auf die Nachricht erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="84c37-105">To issue a query that is meaningful to a custom message type, an application needs to know the properties that are expected on that message.</span></span> <span data-ttu-id="84c37-106">Um eine Liste der Eigenschaften abzurufen, die eine benutzerdefinierte Meldung-Klasse verwendet wird, fragt eine Clientanwendung MAPI Formular-Manager.</span><span class="sxs-lookup"><span data-stu-id="84c37-106">To get a list of properties that a custom message class uses, a client application queries the MAPI form manager.</span></span> <span data-ttu-id="84c37-107">Der Formular-Manager ruft diese Informationen aus der Konfigurationsdatei geeigneten Form, sodass Clientanwendungen diese Informationen der Mehraufwand durch das Aktivieren des Formular-Servers selbst verwenden können.</span><span class="sxs-lookup"><span data-stu-id="84c37-107">The form manager gets this information from the appropriate form configuration file so that client applications can use this information without the overhead of activating the form server itself.</span></span> <span data-ttu-id="84c37-108">Die Clientanwendung ruft die [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) -Methode dazu wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="84c37-108">To do this, the client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method as follows:</span></span> 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

<span data-ttu-id="84c37-109">Beachten Sie, dass das dritte Argument für **ResolveMessageClass** den Ordner mit der zugehörigen Inhaltstabelle, die die Abfrage für Formular Server gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="84c37-109">Note that the third argument to **ResolveMessageClass** is the folder that contains the associated contents table that the query will search for form servers.</span></span> <span data-ttu-id="84c37-110">NULL bedeutet, dass der Formular-Manager auf allen verfügbaren Formular Containern suchen soll.</span><span class="sxs-lookup"><span data-stu-id="84c37-110">NULL indicates that the form manager should search all available form containers.</span></span> <span data-ttu-id="84c37-111">Wenn die Abfrage für einen bestimmten Ordner ausgeführt wird, ist es besser, stattdessen Einbeziehung den entsprechenden [IMAPIFolder](imapifolderimapicontainer.md) Zeiger.</span><span class="sxs-lookup"><span data-stu-id="84c37-111">If the query is to run against a particular folder, it is better to include the appropriate [IMAPIFolder](imapifolderimapicontainer.md) pointer instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="84c37-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84c37-112">See also</span></span>



[<span data-ttu-id="84c37-113">Formularserverinteraktionen</span><span class="sxs-lookup"><span data-stu-id="84c37-113">Form Server Interactions</span></span>](form-server-interactions.md)

