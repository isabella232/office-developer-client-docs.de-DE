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
  
Warteschlange für langfristige ID-Strukturen, die vom Speicheranbieter für persönliche Ordner-Dateien (PST) verwendet werden, um eine Eintrags-ID für eine neue Nachricht oder einen neuen Ordner im Offlinemodus zuzuweisen.
  
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
  
- Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
 _ulReserved_
  
- Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
 _dwAlloc_
  
- Die Anzahl der Einträge, die für die Zuordnung zur Verfügung stehen. Diese Einträge haben dieselbe GUID (Globally Unique Identifier).
    
 _dwNextAlloc_
  
- Die Anzahl der Einträge, die als nächstes für die Zuordnung zur Verfügung stehen. Diese Einträge haben dieselbe GUID.
    
 _ltidAlloc_
  
- Die langfristige ID-Struktur, **[LTID](ltid.md)**, die den derzeit für die Zuordnung verfügbaren Eintrag identifiziert. Die langfristige ID-Struktur enthält eine GUID und einen Index, der ein Objekt im Speicher identifiziert. Zusammen können die GUID und der Index eine eindeutige Eintrags-ID für ein Objekt bilden. 
    
 _ltidNextAlloc_
  
- Langfristige ID-Struktur, die den nächsten verfügbaren Eintrag identifiziert.
    
## <a name="remarks"></a>Bemerkungen

Eine Eintrags-ID ist ein 4-Byte-MAPI-Eintragsbezeichner für einen Ordner oder eine Nachricht. Weitere Informationen finden Sie unter [Eintrags](https://msdn.microsoft.com/library/ms836424)-Nr.
  
Wenn ein PST-Speicheranbieter einem neuen Objekt eine Eintrags-ID zuweist, benötigt er zunächst eine GUID, die den Server identifiziert, und einen Index, der das Objekt im Speicher identifiziert. Obwohl die GUID für alle Eintrags-IDs nicht eindeutig ist, bieten die GUID und der kombinierte Index einen eindeutigen Eintrag. Dieses GUID-und Index-Paar wird durch eine langfristige ID-Struktur, **LTID**, nachverfolgt, die Teil der **OLFI** -Struktur ist. 
  
Der PST-Speicheranbieter hält in **OLFI** für jedes GUID-Index-paar keine **LTID** -Struktur an. Es behält eine **LTID** -Struktur, *ltidAlloc* , für das derzeit erste verfügbare GUID-Index-paar; count, *dwAlloc* , der Anzahl der verfügbaren Einträge, die dieselbe GUID verwenden; und eine zweite **LTID** -Struktur, *ltidNextAlloc* , für das nächste verfügbare GUID-Index-Paar mit einer anderen GUID. Der PST-Speicheranbieter verwendet die **OLFI** -Struktur, um die überLIEFERTen GUIDs und Indizes nachzuverfolgen. Auf einer virtuellen Ebene verwaltet der Anbieter eine Reserve für eine Reihe von **LTID** -Strukturen, die bereit für die Zuordnung sind.  *dwAlloc* verwaltet die Anzahl der verfügbaren **LTID** -Strukturen. 
  
Anforderungen für Eintrags-IDs werden in Blöcken gespeichert. Wenn es eine Anforderung für einen Block gibt, überprüft der PST-Speicheranbieter, ob ausreichend Reserve vorhanden ist, indem die angeforderte Größe mit *dwAlloc* verglichen wird. Wenn genügend Reserve vorhanden ist, werden die GUID und der Index in *ltidAlloc* für die Zuordnung zurückgegeben. Anschließend wird *dwAlloc* um die angeforderte Größe verringert und der Index in *ltidAlloc* um die angeforderte Größe erhöht. Dadurch wird der PST-Speicheranbieter darauf vorbereitet, *ltidAlloc* für die nächste Anforderung für einen weiteren Block von Eintrags-IDs zuzuweisen. Beachten Sie, dass die GUID für die nächste Anforderung identisch bleibt. 
  
Wenn die Größe einer Anforderung größer als *dwAlloc* ist, versucht der PST-Speicheranbieter zu verwenden, was er als nächstes in Reserve hat, wie von *dwNextAlloc* und *ltidNextAlloc* angegeben. *DwNextAlloc* und *LtidNextAlloc* werden in *dwAlloc* und *ltidAlloc* kopiert, und *dwNextAlloc* und *ltidNextAlloc* werden auf NULL festgelegt. 
  
Ein Anbieter, der den PST-Speicheranbieter umschließt, sollte *ltidNextAlloc* in regelmäßigen Abständen überprüfen, ob er NULL ist. Wenn dies der Fall ist, sollte der Anbieter es mit einer neuen GUID auffüllen und *dwNextAlloc* zurücksetzen, damit mehr Eintrags-IDs zugeordnet werden können. 
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[LTID](ltid.md)

