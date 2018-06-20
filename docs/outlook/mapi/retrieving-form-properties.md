---
title: Abrufen von Formulareigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 334ecaacec88c3730f4cc2f4c80eb35d5a553c4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795401"
---
# <a name="retrieving-form-properties"></a>Abrufen von Formulareigenschaften

  
  
**Betrifft**: Outlook 
  
Zum Ausführen eine Abfrage, die in einem benutzerdefinierten Nachrichtentyp sinnvoll ist, muss eine Anwendung die Eigenschaften kennen, die auf die Nachricht erwartet werden. Um eine Liste der Eigenschaften abzurufen, die eine benutzerdefinierte Meldung-Klasse verwendet wird, fragt eine Clientanwendung MAPI Formular-Manager. Der Formular-Manager ruft diese Informationen aus der Konfigurationsdatei geeigneten Form, sodass Clientanwendungen diese Informationen der Mehraufwand durch das Aktivieren des Formular-Servers selbst verwenden können. Die Clientanwendung ruft die [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) -Methode dazu wie folgt aus: 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

Beachten Sie, dass das dritte Argument für **ResolveMessageClass** den Ordner mit der zugehörigen Inhaltstabelle, die die Abfrage für Formular Server gesucht wird. NULL bedeutet, dass der Formular-Manager auf allen verfügbaren Formular Containern suchen soll. Wenn die Abfrage für einen bestimmten Ordner ausgeführt wird, ist es besser, stattdessen Einbeziehung den entsprechenden [IMAPIFolder](imapifolderimapicontainer.md) Zeiger. 
  
## <a name="see-also"></a>Siehe auch



[Formular Server Interaktionen](form-server-interactions.md)

