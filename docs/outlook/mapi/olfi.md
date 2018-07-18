---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ff23472254df2bd9d2195c7cf2c4258b856ec430
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793302"
---
# <a name="olfi"></a>OLFI

  
  
**Betrifft**: Outlook 
  
Warteschlange der langfristigen ID Strukturen verwendet durch den Anbieter für Persönliche Ordner-Datei (PST) anmelden, eine Eintrags-ID für eine neue Nachricht oder einen Ordner im Offlinemodus zuzuweisen.
  
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
  
- Die Versionsnummer für die Struktur. 
    
 _muidReserved_
  
- Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
 _ulReserved_
  
- Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
 _dwAlloc_
  
- Die Anzahl der Einträge, die für die Zuweisung verfügbar sind. Diese Einträge freigeben denselben global eindeutigen Bezeichner (GUID).
    
 _dwNextAlloc_
  
- Die Anzahl der Einträge, die als Nächstes für die Zuweisung verfügbar sind. Diese Einträge Teilen dieselbe GUID.
    
 _ltidAlloc_
  
- Langfristige Struktur der-ID, **[LTID](ltid.md)**, der derzeit für die Zuweisung Posten identifizieren. Die langfristige ID-Datenstruktur enthält eine GUID und einen Index, die ein Objekt im Speicher identifiziert. Zusammen können die GUID und der Index eine eindeutige Eintrags-ID für ein Objekt bilden. 
    
 _ltidNextAlloc_
  
- Struktur der langfristigen-ID, die den nächsten verfügbaren Eintrag identifiziert.
    
## <a name="remarks"></a>Bemerkungen

Eine Eintrags-ID ist eine 4-Byte-MAPI-Eintrags-ID für einen Ordner oder eine Nachricht. Weitere Informationen finden Sie unter [ENTRYID](http://msdn.microsoft.com/en-us/library/ms836424).
  
Wenn ein neues Objekt durch eine PST-Speicheranbieter eine Eintrags-ID zugewiesen wird, benötigt es zunächst eine GUID, die den Server identifiziert und ein Index, der das Objekt im Speicher angibt. Obwohl die GUID über alle EntryIDs nicht eindeutig ist, geben Sie die GUID und der Index kombiniert einen eindeutigen Eintrag. Dieses Paar-GUID und der Index nachverfolgt wird durch eine langfristige ID-Struktur **LTID**, das Teil der Struktur **OLFI** ist. 
  
Der PST-Speicher-Anbieter ist nicht physisch im **OLFI** eine **LTID** -Struktur für jedes Paar GUID-Index aufbewahrt werden können. Es bleibt einer **LTID** Struktur *LtidAlloc* für das derzeit erste verfügbaren GUID-Index-Paar. Count, *DwAlloc* die Anzahl der verfügbaren Einträge, die in derselben GUID freigeben; und eine zweite **LTID** -Struktur *LtidNextAlloc* für das nächste verfügbare GUID-Index-Paar, die eine andere GUID verfügt. Die PST-Datei speichert Provider verwendet die Struktur der **OLFI** zum Nachverfolgen der GUIDs und der Indizes, die es, werden ausgegeben hat. Virtuelle Ebene verwaltet der Anbieter eine Reserve einer Zahl von **LTID** -Strukturen, die bereit sind, zugeordnet werden.  *DwAlloc* hält eine der verfügbaren **LTID** Strukturen. 
  
Anforderungen für die Eintrags-IDs werden blockiert. Wenn eine Anforderung für einen Block vorhanden ist, überprüft der PST-Speicher-Anbieter befindet sich über ausreichende Reserve verfügbar durch die angeforderte Größe mit *DwAlloc* vergleichen. Wenn über ausreichende Reserve vorhanden ist, gibt die GUID und der Index in *LtidAlloc* für die Zuordnung zurück. Klicken Sie dann verringert *DwAlloc* um die angeforderte Größe und erhöht den Index in *LtidAlloc* um die erforderliche Größe. Den PST-Speicheranbieter *LtidAlloc* bei der nächsten Anforderung für eine andere Block mit EntryIDs zugewiesen werden kann. Beachten Sie, dass die GUID für die nächste Anforderung unverändert bleibt. 
  
Wenn die Größe einer Anforderung *DwAlloc* übersteigt, versucht der PST-Speicher-Anbieter verwenden, was sie als Nächstes behalten Sie gemäß *DwNextAlloc* und *LtidNextAlloc* hat. Es kopiert *DwNextAlloc* und *LtidNextAlloc* *DwAlloc* und *LtidAlloc* und *DwNextAlloc* und *LtidNextAlloc* auf NULL festgelegt. 
  
Ein Anbieter, der umbrochen den PST-Speicher-Anbieter wird überprüfen regelmäßig *LtidNextAlloc* , um festzustellen, ob er NULL ist. Wenn dies der Fall, sollte der Anbieter füllen Sie sie mit einer neuen GUID und *DwNextAlloc* zurückgesetzt, sodass weitere Eintrags-IDs zugewiesen werden kann. 
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[LTID](ltid.md)

