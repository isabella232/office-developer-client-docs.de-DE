---
title: NOTIFKEY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.NOTIFKEY
api_type:
- COM
ms.assetid: 031b7e18-59b2-445c-a747-348fda92f458
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6665569b157a874aec248312b30e0528f48c0bcb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625189"
---
# <a name="notifkey"></a>NOTIFKEY

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Identifiziert eindeutig eine Verbindung zwischen einer Empfehlungssenke, einer Empfehlungsquelle und mapi.
  
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
  
> Anzahl der Bytes  im Ab-Element. 
    
 **ab**
  
> Bytearray, das den Benachrichtigungsschlüssel beschreibt.
    
## <a name="remarks"></a>Bemerkungen

The [Subscribe](imapisupport-subscribe.md) and [Notify](imapisupport-notify.md) methods of [IMAPISupport](imapisupportiunknown.md) use the **NOTIFKEY** structure to generate notifications to the appropriate advise sink about the appropriate advise source. 
  
Dienstanbieter generieren Benachrichtigungsschlüssel, wenn ihre **Advise-Methode** aufgerufen wird, und sie möchten **Subscribe** aufrufen, um die Benachrichtigungsregistrierung und das anschließende Senden von Benachrichtigungen zu verarbeiten. Ein Benachrichtigungsschlüssel kann der Eintragsbezeichner der Empfehlungsquelle oder ein anderes identifizierende Element wie eine Konstante sein. Beispielsweise kann ein Nachrichtenspeicheranbieter den Pfad eines Ordners als Benachrichtigungsschlüssel verwenden. 
  
Der Benachrichtigungsschlüssel sollte über mehrere Prozesse hinweg funktionieren. 
  
Die Bereichsanforderungen für einen Benachrichtigungsschlüssel ähneln denen für einen langfristigen Eintragsbezeichner. Im Gegensatz zu einem Eintragsbezeichner muss ein Benachrichtigungsschlüssel jedoch binär vergleichbar sein. In der Regel enthält ein Benachrichtigungsschlüssel einen **GUID-Wert,** der vom Dienstanbieter definiert wird, gefolgt von anderen anbieterspezifischen Informationen, die für das Objekt eindeutig sind. 
  
Eine Erläuterung der Verwendung der **NOTIFKEY-Struktur** zum Verwalten der Verbindungen zwischen den Empfehlungssenken und den Objekten, die die Benachrichtigungen generieren, finden Sie unter ["Unterstützende Ereignisbenachrichtigung".](supporting-event-notification.md) 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Strukturen](mapi-structures.md)

