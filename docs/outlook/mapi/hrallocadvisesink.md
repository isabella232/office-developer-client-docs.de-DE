---
title: HrAllocAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- HrAllocAdviseSink
api_type:
- HeaderDef
ms.assetid: 1dd460e6-ce95-4fef-bb5e-8d778c9716d5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0bbd881b194ed3b2b94758f9e8a25eaf1e869c3d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614059"
---
# <a name="hrallocadvisesink"></a>HrAllocAdviseSink

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt ein Empfehlungssenkenobjekt, das durch die aufrufende Implementierung angegeben wird, und eine Rückruffunktion, die durch eine Ereignisbenachrichtigung ausgelöst wird. 
  
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
  
> [in] Zeiger auf eine Rückruffunktion basierend auf dem [NOTIFCALLBACK-Prototyp,](notifcallback.md) den mapi aufrufen soll, wenn ein Benachrichtigungsereignis für die neu erstellte Empfehlungssenke auftritt. 
    
 _lpvContext_
  
> [in] Zeiger auf Aufruferdaten, die an die Rückruffunktion übergeben werden, wenn mapi sie aufruft. Die Aufruferdaten können eine Adresse darstellen, die für den Client oder Anbieter von Bedeutung ist. In der Regel stellt der  _lpvContext-Parameter_ für C++-Code einen Zeiger auf die Adresse eines Objekts dar. 
    
 _lppAdviseSink_
  
> [out] Zeiger auf einen Zeiger auf ein Empfehlungssenkenobjekt.
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Bemerkungen

Um die **HrAllocAdviseSink-Funktion** zu verwenden, erstellt eine Clientanwendung oder ein Dienstanbieter ein Objekt zum Empfangen von Benachrichtigungen, erstellt eine Benachrichtigungsrückruffunktion basierend auf dem [NOTIFCALLBACK-Funktionsprototyp,](notifcallback.md) der mit diesem Objekt verknüpft ist, und übergibt einen Zeiger an das Objekt in der **HrAllocAdviseSink-Funktion** als _lpvContext-Wert._ Dadurch wird eine Benachrichtigung ausgeführt. und als Teil des Benachrichtigungsprozesses ruft MAPI die Rückruffunktion mit dem Objektzeiger als Kontext auf. 
  
MAPI implementiert das Benachrichtigungsmodul asynchron. In C++ kann der Benachrichtigungsrückruf eine Objektmethode sein. Wenn das Objekt, das die Benachrichtigung generiert, nicht vorhanden ist, muss der Client oder Anbieter, der die Benachrichtigung anfordert, eine separate Verweisanzahl für dieses Objekt für die Empfehlungssenke des Objekts behalten. 
  
> [!CAUTION]
> **HrAllocAdviseSink** sollte sparsam verwendet werden; Es ist sicherer für Clients, eigene Empfehlungssenken zu erstellen. 
  

