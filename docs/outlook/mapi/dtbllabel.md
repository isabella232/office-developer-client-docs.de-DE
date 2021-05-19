---
title: DTBLLABEL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLABEL
api_type:
- COM
ms.assetid: 5837facf-acd3-48fe-9610-f88085d99aef
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: aa3345740c534b5ff156f062e731c98bc6164eed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410686"
---
# <a name="dtbllabel"></a>DTBLLABEL

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Bezeichnung, die in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandtes Makro  <br/> |[SizedDtblLabel](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a>Elemente

 **ulbLpszLabelName**
  
> Position im Arbeitsspeicher der Zeichenzeichenfolgenbeschriftung.
    
 **ulFlags**
  
> Bitmaske von Flags, die zum Festlegen des Formats der Bezeichnung verwendet werden, auf das das **ulbLpszLabelName-Element** verweist. Das folgende Flag kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die Bezeichnung ist im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich die Bezeichnung im ANSI-Format.
    
## <a name="remarks"></a>Hinweise

Eine **DTBLLABEL-Struktur** beschreibt einen Beschriftungssteuerelementtext, der mit einem anderen Steuerelementtyp angezeigt wird, um diesem Steuerelement Bedeutung hinzuzufügen. Die meisten Bearbeitungssteuerelemente werden beispielsweise neben Beschriftungen positioniert, um den Benutzer über die Art der eingegebenen Informationen zu informieren. Einige Steuerelemente, z. B. Gruppenfelder und Optionsfelder, enthalten eigene Bezeichnungen. 
  
Die Bezeichnung kann eine Windows, die als Zeichen nach dem ampersand ( ) identifiziert &amp; wird. Durch Drücken der Zugriffstaste wird der Fokus im ersten nicht gekennzeichneten, nicht auf diese Bezeichnung folgenden Steuerelement in der Anzeigetabelle angezeigt.
  
Es gibt keine Unterstützung für mehrstufige Bezeichnungen. Das Anzeigen mehrerer Zeilen erfordert mehrere Bezeichnungen.
  
Es ist nicht möglich, eine Bezeichnung als schreibgeschütztes Bearbeitungssteuerelement zu verwenden. Der Unterschied ist, dass ein Bearbeitungssteuerelement ausgewählt und kopiert werden kann, während eine Bezeichnung nicht möglich ist. 
  
Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md). Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

