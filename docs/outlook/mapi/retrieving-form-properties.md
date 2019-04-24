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
# <a name="retrieving-form-properties"></a>Abrufen von Formulareigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zum Ausgeben einer Abfrage, die für einen benutzerdefinierten Nachrichtentyp sinnvoll ist, muss eine Anwendung die Eigenschaften kennen, die in dieser Nachricht erwartet werden. Eine Clientanwendung fragt den MAPI-Formular-Manager ab, um eine Liste der Eigenschaften abzurufen, die von einer benutzerdefinierten Nachrichtenklasse verwendet werden. Der Formular-Manager ruft diese Informationen aus der entsprechenden Formular Konfigurationsdatei ab, sodass Clientanwendungen diese Informationen ohne den Aufwand der Aktivierung des Formular Servers selbst verwenden können. Zu diesem Zweck Ruft die Clientanwendung die [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) -Methode wie folgt auf: 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

Beachten Sie, dass das dritte Argument für **ResolveMessageClass** der Ordner ist, in dem die Tabelle mit den zugeordneten Inhalten enthalten ist, die von der Abfrage nach Formular Servern durchsucht wird. NULL gibt an, dass der Formular-Manager alle verfügbaren Formular Container durchsuchen soll. Wenn die Abfrage für einen bestimmten Ordner ausgeführt werden soll, empfiehlt es sich, stattdessen den entsprechenden [IMAPIFolder](imapifolderimapicontainer.md) -Zeiger einzufügen. 
  
## <a name="see-also"></a>Siehe auch



[Formular Server interAktionen](form-server-interactions.md)

