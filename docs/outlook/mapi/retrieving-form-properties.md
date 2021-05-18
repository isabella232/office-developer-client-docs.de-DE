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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412919"
---
# <a name="retrieving-form-properties"></a>Abrufen von Formulareigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zum Ausführen einer Abfrage, die für einen benutzerdefinierten Nachrichtentyp von Bedeutung ist, muss eine Anwendung die Eigenschaften kennen, die für diese Nachricht erwartet werden. Um eine Liste der Eigenschaften zu erhalten, die von einer benutzerdefinierten Nachrichtenklasse verwendet werden, fragt eine Clientanwendung den MAPI-Formular-Manager ab. Der Formular-Manager ruft diese Informationen aus der entsprechenden Formularkonfigurationsdatei ab, damit Clientanwendungen diese Informationen verwenden können, ohne den Formularserver selbst zu aktivieren. Dazu ruft die Clientanwendung die [IMAPIFormMgr::ResolveMessageClass-Methode](imapiformmgr-resolvemessageclass.md) wie folgt auf: 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

Beachten Sie, dass das dritte Argument für **ResolveMessageClass** der Ordner ist, der die zugeordnete Inhaltstabelle enthält, nach der die Abfrage nach Formularservern sucht. NULL gibt an, dass der Formular-Manager alle verfügbaren Formularcontainer durchsuchen soll. Wenn die Abfrage für einen bestimmten Ordner ausgeführt werden soll, ist es besser, stattdessen den entsprechenden [IMAPIFolder-Zeiger](imapifolderimapicontainer.md) zu verwenden. 
  
## <a name="see-also"></a>Siehe auch



[Formularserverinteraktionen](form-server-interactions.md)

