---
title: SExistRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SExistRestriction
api_type:
- COM
ms.assetid: 48d5ab42-ee70-4f6e-9184-18d22b08ea1b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8e2cf26b2e4388fac1432308df82ded911cf7501
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550036"
---
# <a name="sexistrestriction"></a>SExistRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Vorhandene Einschränkung, die verwendet wird, um zu testen, ob eine bestimmte Eigenschaft als Spalte in der Tabelle vorhanden ist. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a>Members

 **ulReserved1**
  
> Reserviert; muss Null sein. 
    
 **ulPropTag**
  
> Eigenschaftstag, das die Spalte identifiziert, die in jeder Zeile auf das Vorhandensein getestet werden soll.
    
 **ulReserved2**
  
> Reserviert; muss Null sein.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die vorhandene Einschränkung wird verwendet, um sinnvolle Ergebnisse für andere Arten von Einschränkungen zu gewährleisten, die Eigenschaften betreffen, z. B. Eigenschafts- und Inhaltseinschränkungen. Wenn eine Einschränkung, die eine Eigenschaft umfasst, an [IMAPITable::Restrict](imapitable-restrict.md) oder [IMAPITable::FindRow](imapitable-findrow.md) übergeben wird und die Eigenschaft nicht vorhanden ist, sind die Ergebnisse der Einschränkung nicht definiert. Durch Erstellen  einer AND-Einschränkung, die die Eigenschaftseinschränkung mit einer vorhandenen Einschränkung verknüpft, kann ein Aufrufer garantiert genaue Ergebnisse erhalten. 
  
Vorhandene Einschränkungen können nicht mit Unterobjekteigenschaften verwendet werden, die den Typ PT_OBJECT haben. 
  
Weitere Informationen zur **Struktur "SExistRestriction"** finden Sie unter ["Einschränkungen".](about-restrictions.md) 
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

