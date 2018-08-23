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
ms.openlocfilehash: d5cb43bfa3acd912e397644657223c177d6afb30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589322"
---
# <a name="hrallocadvisesink"></a>HrAllocAdviseSink

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Erstellt eine Advise-Empfängerobjekt, wenn ein Kontext die aufrufende Implementierung und eine Rückruffunktion, die ausgelöst werden, indem eine Benachrichtigung angegeben wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Parameter

 _lpfnCallback_
  
> [in] Zeiger auf eine Rückruffunktion, die basierend auf den [NOTIFCALLBACK](notifcallback.md) Prototyp, die MAPI angerufen, wenn eine Benachrichtigungsereignis tritt ein, für die neu erstellte advise-Empfänger. 
    
 _lpvContext_
  
> [in] Zeiger auf Daten des Anrufers an der Callback-Funktion beim Aufrufen von MAPI übergeben. Die Anrufer Daten können eine Adresse Vielfache an den Client oder Anbieter von darstellen. In der Regel stellt der _LpvContext_ -Parameter für C++-Code einen Zeiger auf die Adresse eines Objekts. 
    
 _lppAdviseSink_
  
> [out] Zeiger auf einen Zeiger auf eine Advise-Empfängerobjekt.
    
## <a name="return-value"></a>Rückgabewert

None.
  
## <a name="remarks"></a>HinwBemerkungeneise

Um die **HrAllocAdviseSink** -Funktion verwenden, können Sie eine Clientanwendung oder Dienstanbieter erstellt ein Objekt Erhalt von Benachrichtigungen, erstellt eine Benachrichtigung Callback-Funktion basierend auf den [NOTIFCALLBACK](notifcallback.md) Funktionsprototyp, der mit diesem Objekt wechselt, auf und übergibt einen Zeiger auf das Objekt in der **HrAllocAdviseSink** -Funktion als _LpvContext_ Wert. Auf diese Weise führt eine Benachrichtigung. und als Teil der Benachrichtigung, MAPI-Aufrufen die Callback-Funktion mit dem Mauszeiger Objekt als Kontext aus. 
  
MAPI implementierte eine Benachrichtigung Engine asynchron an. In C++ kann die Benachrichtigung Callback-Methode eines Objekts sein. Wenn das Objekt, das die Benachrichtigung generiert nicht vorhanden, wird des Clients oder Anbieter Anfordern einer Benachrichtigung muss eine separate Referenzzähler für dieses Objekt für des Objekts behalten advise-Empfänger. 
  
> [!CAUTION]
> **HrAllocAdviseSink** sollte nur selten verwendet werden. Es ist sicherer für Clients zum Erstellen ihrer eigenen Advise-senken. 
  

