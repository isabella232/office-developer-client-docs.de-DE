---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 027905721b5730b4c3d78f496022b88a8e6b84d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279753"
---
# <a name="olfi"></a>OLFI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Warteschlange mit langfristigen ID-Strukturen, die vom Anbieter des Informationsspeichers für persönliche Ordner (Personal Folders File, PST) zum Zuweisen einer Eintrags-ID für eine neue Nachricht oder einen neuen Ordner im Offlinemodus verwendet werden.
  
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
    
 _dwAlloc_
  
- Die Anzahl der Einträge, die für die Zuweisung verfügbar sind. Diese Einträge haben dieselbe guiD (Globally Unique Identifier).
    
 _dwNextAlloc_
  
- Die Anzahl der Einträge, die als Nächstes für die Zuweisung verfügbar sind. Diese Einträge haben dieselbe GUID.
    
 _ltidAlloc_
  
- Die langfristige ID-Struktur **[LTID,](ltid.md)** die den eintrag identifiziert, der derzeit für die Zuweisung verfügbar ist. Die langfristige ID-Struktur enthält eine GUID und einen Index, der ein Objekt im Speicher identifiziert. Zusammen können die GUID und der Index eine eindeutige Eintrags-ID für ein Objekt bilden. 
    
 _ltidNextAlloc_
  
- Langfristige ID-Struktur, die den nächsten verfügbaren Eintrag identifiziert.
    
## <a name="remarks"></a>Hinweise

Eine Eintrags-ID ist eine 4-Byte-MAPI-Eintrags-ID für einen Ordner oder eine Nachricht. Weitere Informationen finden Sie unter [ENTRYID](https://msdn.microsoft.com/library/ms836424).
  
Wenn ein Pst Store-Anbieter einem neuen Objekt eine Eintrags-ID zu weist, benötigt er zunächst eine GUID, die den Server identifiziert, und einen Index, der das Objekt im Speicher identifiziert. Auch wenn die GUID nicht für alle Eintrags-IDs eindeutig ist, bieten die GUID und der Index zusammen einen eindeutigen Eintrag. Dieses GUID- und Indexpaar wird von einer langfristigen ID-Struktur, **LTID**, nachverfolgt, die Teil der **OLFI-Struktur** ist. 
  
Der Anbieter des PST-Speichers hält in **OLFI** keine **LTID-Struktur** für jedes GUID-Indexpaar. Es behält eine **LTID-Struktur,**  *ltidAlloc*  , für das derzeit erste verfügbare GUID-Index-Paar bei. eine Anzahl,  *dwAlloc*  , der Anzahl der verfügbaren Einträge, die dieselbe GUID gemeinsam verwenden; und eine zweite **LTID-Struktur,**  *ltidNextAlloc*  , für das nächste verfügbare GUID-Indexpaar mit einer anderen GUID. Der Anbieter des PST-Speichers verwendet die **OLFI-Struktur,** um die von ihm bereitgestellten GUIDs und Indizes nachzuverfolgen. Auf virtueller Ebene verwaltet der Anbieter eine Reserve einer Reihe von **LTID-Strukturen,** die zugeordnet werden können.  *dwAlloc* verwaltet eine Anzahl der verfügbaren **LTID-Strukturen.** 
  
Anforderungen für Eintrags-IDs werden in Blöcken verwendet. Wenn eine Anforderung für einen Block vorhanden ist, überprüft der Anbieter des PST-Speichers, ob genügend Reserve verfügbar ist, indem er die angeforderte Größe mit *dwAlloc vergleicht.* Wenn genügend Reserve vorhanden ist, werden die GUID und der Index in  *ltidAlloc für die Zuordnung*  zurückgegeben. Anschließend wird  *dwAlloc*  um die angeforderte Größe verringert und der Index in  *ltidAlloc*  um die angeforderte Größe erhöht. Dadurch wird der Anbieter des PST-Speichers darauf vorbereitet,  *ltidAlloc bei*  der nächsten Anforderung für einen weiteren Block von Eintrags-IDs zuzuordnen. Beachten Sie, dass die GUID für die nächste Anforderung unverändert bleibt. 
  
Wenn die Größe einer Anforderung größer als  *"dwAlloc"*  ist, versucht der Anbieter des PST-Speichers, das als Nächstes in der Reserve zu verwenden, wie von  *dwNextAlloc*  und  *ltidNextAlloc*  angegeben. Sie kopiert  *dwNextAlloc*  und  *ltidNextAlloc*  in  *dwAlloc*  bzw.  *ltidAlloc*  und legt  *dwNextAlloc*  und  *ltidNextAlloc*  auf NULL fest. 
  
Ein Anbieter, der den Anbieter für den PST-Speicher umschließt, sollte in regelmäßigen Abständen  *ltidNextAlloc*  überprüfen, um zu prüfen, ob er NULL ist. Falls ja, sollte der Anbieter eine neue GUID auffüllen und  *dwNextAlloc*  zurücksetzen, damit weitere Eintrags-IDs zugewiesen werden können. 
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[LTID](ltid.md)

