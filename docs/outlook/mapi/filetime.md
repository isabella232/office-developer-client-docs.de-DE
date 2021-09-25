---
title: FILETIME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FILETIME
api_type:
- COM
ms.assetid: 4af8e79a-697e-44a1-8576-fdc57726e9ef
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ac1a9a4b84e50e1e979a3228d30067877f20eef5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614206"
---
# <a name="filetime"></a>FILETIME

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen nicht signierten 64-Bit-Datums- und Uhrzeitwert für eine Datei. Dieser Wert stellt die Anzahl von 100 Nanosekunden seit dem Anfang des 1. Januar 1601 dar. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a>Members

 **wetterLowDateTime**
  
> 32 Bit des Dateizeitwerts in niedriger Reihenfolge. 
    
 **"highDateTime"**
  
> 32 Bits des Dateizeitwerts in hoher Reihenfolge.
    
## <a name="remarks"></a>Bemerkungen

Eine Eigenschaft vom Typ PT_SYSTIME hat eine **FILETIME-Struktur** für ihren Wert. Eine solche Eigenschaft weist einen **FILETIME-Datentyp** für das **Value-Element** in der Definition in einer [SPropValue-Struktur](spropvalue.md) auf. 
  
Die Definition der **FILETIME-Struktur** befindet sich in der  _Win32-Programmierreferenz_ und in der MAPI-Headerdatei Mapidefs.h. MAPI definiert die Struktur bedingt, um sicherzustellen, dass sie definiert ist, wenn die Win32-Definition nicht verfügbar ist. 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

