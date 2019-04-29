---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Stellt eine gesamte Zeitzone einschließlich aller historischen, aktuellen und zukünftigen Zeitzone-Schicht Regeln für Sommerzeit dar.
ms.openlocfilehash: 5f7000ecc1fa602b330670c2ee1c39f673a11a65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429341"
---
# <a name="tzdefinition"></a>TZDEFINITION

Stellt eine gesamte Zeitzone einschließlich aller historischen, aktuellen und zukünftigen Zeitzone-Schicht Regeln für Sommerzeit dar.
  
## <a name="quick-info"></a>QuickInfo

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a>Elemente

_wFlags_
  
> Gibt an, dass der Schlüsselname, der die Zeitzone in der Windows-Registrierung darstellt, gültig ist. Da jede Zeitzone immer mit einem Schlüsselnamen identifiziert werden sollte, sollte dieser Member immer den Wert **TZDEFINITION_FLAG_VALID_KEYNAME**haben.
    
_pwszKeyName_
  
> Der Name des Schlüssels für diese Zeitzone in der Windows-Registrierung. Dieser Name darf nicht lokalisiert werden. Es hat eine maximale Größe von **MAX_PATH**, die in der Windows Software Development Kit (SDK)-Headerdatei Windows. h definiert ist. 
    
_cRules_
  
> Die Anzahl der Zeitzonenregeln für diese Definition. Die maximale Anzahl von Regeln lautet **TZ_MAX_RULES**. 
    
_rgRules_
  
> Ein Array von Regeln, die beschreiben, wenn Verschiebungen auftreten.
    
## <a name="remarks"></a>Bemerkungen

Es muss mindestens eine Regel in *RgRules* vorhanden sein. Die erste Regel in *rgRules* gilt als die Regel, die verwendet werden soll, bis die zweite Regel gestartet wird, unabhängig von der *stStart* für die erste Regel. 
  
Die Regeln sollten vom ältesten zum neuesten sortiert werden. Zwischen den Regeln ist keine Überlappung zulässig, sodass eine frühere Regel als beendet gilt, wenn eine neue Regel beginnt.
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Outlook exportierter APIs)](constants-outlook-exported-apis.md)
- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)

