---
title: SSubRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSubRestriction
api_type:
- COM
ms.assetid: 5f7012f7-060d-4f2d-bcff-2aa9f6980e71
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 152f3032876d6473f1716afa46507196cd5ecc55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795624"
---
# <a name="ssubrestriction"></a>SSubRestriction

  
  
**Betrifft**: Outlook 
  
Eine untergeordnete Objekt Beschränkung der verwendet wird, um die Zeilen der Anlage einer Nachricht oder ein Empfänger Tabelle Filtern beschrieben.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a>Elemente

 **ulSubObject**
  
> Typ des untergeordneten Objekts als Ziel für die Einschränkung. Mögliche Werte sind wie folgt: 
    
PR_MESSAGE_RECIPIENTS 
  
> Wenden Sie die Einschränkung auf Empfänger einer Nachricht-Tabelle. 
    
PR_MESSAGE_ATTACHMENTS 
  
>  Die Beschränkung auf eine Nachricht Anlagentabelle anwenden. 
    
 **lpRes**
  
> Zeiger auf eine [SRestriction](srestriction.md) -Struktur. 
    
## <a name="remarks"></a>Bemerkungen

Untergeordnete Objekt Einschränkungen werden durch die alle Tabellen nicht unterstützt. In der Regel nur Ordner Inhalt Tabellen und die Ergebnisse Suchordner unterstützt. Beispielsweise werden Einschränkungen untergeordneten Objekts verwendet, um eine Nachricht zu suchen, die einen bestimmten Typ Anlage oder ein Empfänger hat. 
  
Wenn eine Implementierung der untergeordneten Objekts Einschränkungen nicht unterstützt werden, gibt die [Methode IMAPITable:: Restrict](imapitable-restrict.md) oder [IMAPITable](imapitable-findrow.md) Methoden MAPI_E_TOO_COMPLEX zurück. 
  
Eine allgemeine Erläuterung der Funktionsweise von Einschränkungen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

