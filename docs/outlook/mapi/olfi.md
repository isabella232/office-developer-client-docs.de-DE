---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ba40df92e19de903388b930e6264535f521d2a2d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625182"
---
# <a name="olfi"></a>OLFI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Warteschlange mit langfristigen ID-Strukturen, die vom PST-Speicheranbieter (Personal Folders File) verwendet werden, um eine Eintrags-ID für eine neue Nachricht oder einen neuen Ordner im Offlinemodus zuzuweisen.
  
## <a name="quick-info"></a>QuickInfo

```cpp
typedef struct { 
    ULONG    ulVersion; 
    MAPIUID  muidReserved; 
    ULONG    ulReserved; 
    DWORD    dwAlloc; 
    DWORD    dwNextAlloc; 
    LTID     ltidAlloc; 
    LTID     ltidNextAlloc; 
} OLFI, *POLFI;
```

## <a name="members"></a>Elemente

 _ulVersion_
  
- Versionsnummer für die Struktur. 
    
 _muidReserved_
  
- Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
 _ulReserved_
  
- Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
 _ressourcenAlloc_
  
- Die Anzahl der Einträge, die für die Zuordnung verfügbar sind. Diese Einträge haben dieselbe GUID (Globally Unique Identifier).
    
 _ressourcenNextAlloc_
  
- Die Anzahl der Einträge, die als Nächstes für die Zuordnung verfügbar sind. Diese Einträge verwenden dieselbe GUID.
    
 _ltidAlloc_
  
- Die langfristige ID-Struktur **[LTID,](ltid.md)** die den eintrag identifiziert, der derzeit für die Zuordnung verfügbar ist. Die langfristige ID-Struktur enthält eine GUID und einen Index, der ein Objekt im Speicher identifiziert. Zusammen können die GUID und der Index eine eindeutige Eintrags-ID für ein Objekt bilden. 
    
 _ltidNextAlloc_
  
- Langfristige ID-Struktur, die den nächsten verfügbaren Eintrag identifiziert.
    
## <a name="remarks"></a>Bemerkungen

Eine Eintrags-ID ist ein 4-Byte-MAPI-Eintragsbezeichner für einen Ordner oder eine Nachricht. Weitere Informationen finden Sie unter [ENTRYID](https://msdn.microsoft.com/library/ms836424).
  
Wenn ein PST-Speicheranbieter einem neuen Objekt eine Eintrags-ID zuweist, benötigt er zuerst eine GUID, die den Server identifiziert, und einen Index, der das Objekt im Speicher identifiziert. Obwohl die GUID nicht für alle Eintrags-IDs eindeutig ist, stellen die GUID und der Index zusammen einen eindeutigen Eintrag bereit. Dieses GUID- und Indexpaar wird durch die langfristige ID-Struktur **LTID** nachverfolgt, die Teil der **OLFI-Struktur** ist. 
  
Der ANBIETER des PST-Speichers speichert nicht physisch in **OLFI** eine **LTID-Struktur** für jedes GUID-Indexpaar. Es behält eine **LTID-Struktur,**  *ltidAlloc,*  für das derzeit erste verfügbare GUID-Indexpaar bei. Anzahl,  *wetterAlloc*  der Anzahl der verfügbaren Einträge, die dieselbe GUID verwenden; und eine zweite **LTID-Struktur,**  *ltidNextAlloc,*  für das nächste verfügbare GUID-Indexpaar mit einer anderen GUID. Der ANBIETER des PST-Speichers verwendet die **OLFI-Struktur,** um die von ihm übergebenen GUIDs und Indizes nachzuverfolgen. Auf virtueller Ebene verwaltet der Anbieter eine Reserve einer Reihe von **LTID-Strukturen,** die für die Zuweisung bereit sind.  *für die Anzahl* der verfügbaren **LTID-Strukturen.** 
  
Anforderungen für Eintrags-IDs werden in Blöcken gesendet. Wenn eine Anforderung für einen Block vorliegt, überprüft der ANBIETER des PST-Speichers, ob genügend Reserve vorhanden ist, indem er die angeforderte Größe mit  *"wetterAlloc"*  vergleicht. Wenn genügend Reserve vorhanden ist, werden die GUID und der Index in  *ltidAlloc*  für die Zuordnung zurückgegeben. Anschließend wird die Größe von  *"ntAlloc"*  um die angeforderte Größe verringert und der Index in  *ltidAlloc*  um die angeforderte Größe erhöht. Dadurch wird der ANBIETER des PST-Speichers darauf vorbereitet,  *ltidAlloc*  bei der nächsten Anforderung für einen anderen Block von Eintrags-IDs zuzuweisen. Beachten Sie, dass die GUID für die nächste Anforderung gleich bleibt. 
  
Wenn die Größe einer Anforderung größer als  *"ntAlloc"*  ist, versucht der ANBIETER des PST-Speichers zu verwenden, was er als Nächstes in der Reserve hat, wie durch  *"wetterNextAlloc"*  und  *"ltidNextAlloc"*  angegeben. Sie kopiert *wetterNextAlloc* und *ltidNextAlloc* bzw. ltidNextAlloc in ntAlloc bzw. *ltidNextAlloc* und legt *ltidNextAlloc* auf NULL fest.   
  
Ein Anbieter, der den PST-Speicheranbieter umschließt, sollte in regelmäßigen  *Abständen überprüfen,*  ob er NULL ist. Falls ja, sollte der Anbieter ihn mit einer neuen GUID auffüllen und  *"wetterNextAlloc"*  zurücksetzen, damit weitere Eintrags-IDs zugewiesen werden können. 
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[LTID](ltid.md)

