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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ab1586696a4b72aa9e88545c2069c3f8b5d22d72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429628"
---
# <a name="notifkey"></a>NOTIFKEY

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Identifiziert eindeutig eine Verbindung zwischen einer Ratensenke, einer Ratenquelle und MAPI.
  
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

## <a name="members"></a>Elemente

 **cb**
  
> Anzahl der Bytes im **ab-Element.** 
    
 **ab**
  
> Array von Bytes, die den Benachrichtigungsschlüssel beschreiben.
    
## <a name="remarks"></a>Hinweise

Die [Subscribe-](imapisupport-subscribe.md) und [Notify-Methoden](imapisupport-notify.md) von [IMAPISupport](imapisupportiunknown.md) verwenden die **NOTIFKEY-Struktur,** um Benachrichtigungen an die entsprechende Ratensenke über die entsprechende Informationsquelle zu generieren. 
  
Dienstanbieter generieren Benachrichtigungsschlüssel, wenn ihre **Advise-Methode** aufgerufen wird, und sie möchten **Subscribe** aufrufen, um die Benachrichtigungsregistrierung und das nachfolgende Senden von Benachrichtigungen zu verarbeiten. Ein Benachrichtigungsschlüssel kann der Eintragsbezeichner der Beratenden Quelle oder ein anderes identifizierendes Element wie eine Konstante sein. Beispielsweise kann ein Nachrichtenspeicheranbieter den Pfad eines Ordners als Benachrichtigungsschlüssel verwenden. 
  
Der Benachrichtigungsschlüssel sollte über mehrere Prozesse hinweg funktionieren. 
  
Die Bereichsanforderungen für einen Benachrichtigungsschlüssel ähneln denen für eine langfristige Eintrags-ID. Im Gegensatz zu einem Eintragsbezeichner muss ein Benachrichtigungsschlüssel jedoch binär vergleichbar sein. In der Regel enthält ein Benachrichtigungsschlüssel einen vom Dienstanbieter definierten **GUID-Wert,** gefolgt von anderen anbieterspezifischen Informationen, die für das Objekt eindeutig sind. 
  
Eine Diskussion über die Verwendung der **NOTIFKEY-Struktur** zum Verwalten der Verbindungen zwischen den Ratensenken und den Objekten, die die Benachrichtigungen generieren, finden Sie unter [Supporting Event Notification](supporting-event-notification.md). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Strukturen](mapi-structures.md)

