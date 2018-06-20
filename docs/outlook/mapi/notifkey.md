---
title: NOTIFKEY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFKEY
api_type:
- COM
ms.assetid: 031b7e18-59b2-445c-a747-348fda92f458
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3c480c420753b2da6c57b3961589d5c2e2e8022a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793298"
---
# <a name="notifkey"></a>NOTIFKEY

  
  
**Betrifft**: Outlook 
  
Identifiziert eindeutig eine Verbindung zwischen einer Advise-Empfänger, eine Advise-Quelle und MAPI.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a>Members

 **cb**
  
> Die Anzahl von Bytes in das Element **Ab** . 
    
 **ab**
  
> Array von Bytes, beschreibt die Benachrichtigung-Taste.
    
## <a name="remarks"></a>Hinweise

Die Methoden [Abonnieren](imapisupport-subscribe.md) und [Benachrichtigen](imapisupport-notify.md) der [IMAPISupport](imapisupportiunknown.md) verwenden Sie die Struktur **NOTIFKEY** zum Generieren von Benachrichtigungen an den entsprechenden Advise-Empfänger über die entsprechenden Advise-Quelle. 
  
Dienstanbieter generieren Benachrichtigung Schlüssel, wenn ihre **Advise** -Methode aufgerufen wird und sie **Abonnieren** , um die benachrichtigungsregistrierung und das nachfolgende Senden von Benachrichtigungen zu behandeln anrufen möchten. Eine Taste Benachrichtigung kann die Eintrags-ID der Advise-Quelle oder andere identifizierende Elemente wie etwa eine Konstante sein. Beispielsweise kann Anbieter eine Nachricht den Pfad eines Ordners als dessen Benachrichtigung Schlüssel verwenden. 
  
Der Schlüssel Benachrichtigung sollte für mehrere Prozesse funktionieren. 
  
Die bereichsanforderungen für eine Benachrichtigung Schlüssel ähneln jenen für langfristige Eintrags-ID. Im Gegensatz zu einer Eintrags-ID, muss eine Benachrichtigung Taste jedoch binär-vergleichbar sein. In der Regel enthält ein Benachrichtigung Schlüssel einen **GUID** -Wert, der vom Dienstanbieter gefolgt von anderen eindeutigen anbieterspezifische Informationen auf das Objekt definiert. 
  
Eine Erläuterung der Verwendung der Struktur **NOTIFKEY** zum Verwalten von Verbindungen zwischen der Advise-senken und die Objekte, die die Benachrichtigungen generieren finden Sie unter [Ereignisbenachrichtigung unterstützen](supporting-event-notification.md). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Strukturen](mapi-structures.md)

