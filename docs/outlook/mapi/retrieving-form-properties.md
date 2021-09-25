---
title: Abrufen von Formulareigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6fb1c828803063fbc77d1732ca18b527c08fd0f3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586831"
---
# <a name="retrieving-form-properties"></a>Abrufen von Formulareigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um eine Abfrage auszustellen, die für einen benutzerdefinierten Nachrichtentyp von Bedeutung ist, muss eine Anwendung die Eigenschaften kennen, die für diese Nachricht erwartet werden. Um eine Liste der Eigenschaften abzurufen, die von einer benutzerdefinierten Nachrichtenklasse verwendet werden, fragt eine Clientanwendung den MAPI-Formular-Manager ab. Der Formular-Manager ruft diese Informationen aus der entsprechenden Formularkonfigurationsdatei ab, sodass Clientanwendungen diese Informationen verwenden können, ohne den Aufwand für die Aktivierung des Formularservers selbst zu verursachen. Hierzu ruft die Clientanwendung die [IMAPIFormMgr::ResolveMessageClass-Methode](imapiformmgr-resolvemessageclass.md) wie folgt auf: 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

Beachten Sie, dass das dritte Argument für **ResolveMessageClass** der Ordner ist, der das zugeordnete Inhaltsverzeichnis enthält, nach dem die Abfrage nach Formularservern sucht. NULL gibt an, dass der Formular-Manager alle verfügbaren Formularcontainer durchsuchen soll. Wenn die Abfrage für einen bestimmten Ordner ausgeführt werden soll, ist es besser, stattdessen den entsprechenden [IMAPIFolder-Zeiger](imapifolderimapicontainer.md) einzuschließen. 
  
## <a name="see-also"></a>Siehe auch



[Formularserverinteraktionen](form-server-interactions.md)

