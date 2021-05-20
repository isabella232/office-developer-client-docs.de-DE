---
title: HrAllocAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrAllocAdviseSink
api_type:
- HeaderDef
ms.assetid: 1dd460e6-ce95-4fef-bb5e-8d778c9716d5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7f9873fe8e1825c68d4540cc1d093171e9f95727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428900"
---
# <a name="hrallocadvisesink"></a>HrAllocAdviseSink

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt ein Advise-Sink-Objekt, das einen durch die aufrufende Implementierung angegebenen Kontext und eine Rückruffunktion, die durch eine Ereignisbenachrichtigung ausgelöst werden soll, angegeben wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Parameter

 _lpfnCallback_
  
> [in] Zeiger auf eine Rückruffunktion basierend auf dem [NOTIFCALLBACK-Prototyp,](notifcallback.md) den MAPI aufrufen soll, wenn ein Benachrichtigungsereignis für die neu erstellte Hinweissenke auftritt. 
    
 _lpvContext_
  
> [in] Zeiger auf Aufruferdaten, die an die Rückruffunktion übergeben werden, wenn MAPI sie aufruft. Die Anruferdaten können eine Adresse darstellen, die für den Client oder Anbieter von Bedeutung ist. In der Regel stellt der  _lpvContext-Parameter_ für C++-Code einen Zeiger auf die Adresse eines Objekts dar. 
    
 _lppAdviseSink_
  
> [out] Zeiger auf einen Zeiger auf ein Advise Sink-Objekt.
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Hinweise

Um die **HrAllocAdviseSink-Funktion** zu verwenden, erstellt eine Clientanwendung oder ein Dienstanbieter ein Objekt zum Empfangen von Benachrichtigungen, erstellt eine Benachrichtigungsrückruffunktion basierend auf dem [NOTIFCALLBACK-Funktionsprototyp,](notifcallback.md) der mit diesem Objekt verwendet wird, und übergibt einen Zeiger auf das Objekt in der **HrAllocAdviseSink-Funktion** als _lpvContext-Wert._ Dies führt eine Benachrichtigung aus. und im Rahmen des Benachrichtigungsprozesses ruft MAPI die Rückruffunktion mit dem Objektzeiger als Kontext auf. 
  
MAPI implementiert sein Benachrichtigungsmodul asynchron. In C++ kann der Benachrichtigungsrückruf eine Objektmethode sein. Wenn das Objekt, das die Benachrichtigung generiert, nicht vorhanden ist, muss der Client oder Anbieter, der eine Benachrichtigung anfordert, eine separate Referenzanzahl für dieses Objekt für die Hinweissenke des Objekts behalten. 
  
> [!CAUTION]
> **HrAllocAdviseSink** sollte sparsam verwendet werden. Es ist sicherer für Kunden, eigene Ratensenken zu erstellen. 
  

