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
ms.openlocfilehash: ab1586696a4b72aa9e88545c2069c3f8b5d22d72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280047"
---
# <a name="notifkey"></a>NOTIFKEY

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Identifiziert eindeutig eine Verbindung zwischen einer Advise-Senke, einer Advise-Quelle und MAPI.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi. h  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a>Elemente

 **cb**
  
> Die Anzahl der Bytes im **ab** -Element. 
    
 **ab**
  
> Bytearray, das den Benachrichtigungs Schlüssel beschreibt.
    
## <a name="remarks"></a>Bemerkungen

Die [subscribe](imapisupport-subscribe.md) -und [Notify](imapisupport-notify.md) -Methoden von [IMAPISupport](imapisupportiunknown.md) verwenden die **NOTIFKEY** -Struktur, um Benachrichtigungen für die entsprechende Advise-Quelle zu generieren. 
  
Dienstanbieter generieren Benachrichtigungs Schlüssel, wenn Ihre **Advise** -Methode aufgerufen wird, und Sie möchten **abonnieren** aufrufen, um die Benachrichtigungs Registrierung und das anschließende Senden von Benachrichtigungen zu behandeln. Ein Benachrichtigungs Schlüssel kann die Eintrags-ID der Advise-Quelle oder ein beliebiges anderes identifizierendes Element wie eine Konstante sein. Beispielsweise kann ein Nachrichtenspeicher Anbieter den Pfad eines Ordners als Benachrichtigungs Schlüssel verwenden. 
  
Der Benachrichtigungs Schlüssel sollte über mehrere Prozesse hinweg funktionieren. 
  
Die Bereichsanforderungen für einen Benachrichtigungs Schlüssel ähneln denen für eine langfristige Eintrags-ID. Anders als bei einer Eintrags-ID muss ein Benachrichtigungs Schlüssel jedoch Binär-vergleichbar sein. In der Regel enthält ein Benachrichtigungs Schlüssel einen vom Dienstanbieter definierten **GUID** -Wert, gefolgt von anderen anbieterspezifischen Informationen, die für das Objekt eindeutig sind. 
  
Eine Erläuterung der Verwendung der **NOTIFKEY** -Struktur zum Verwalten der Verbindungen zwischen den Advise-Senken und den Objekten, die die Benachrichtigungen generieren, finden Sie unter [unterstützende Ereignisbenachrichtigung](supporting-event-notification.md). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Strukturen](mapi-structures.md)

