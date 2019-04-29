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
  
Beschreibt eine Bezeichnung, die in einem Dialogfeldverwendet wird, das aus einer Anzeigetabelle erstellt wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Zugehöriges Makro  <br/> |[SizedDtblLabel](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a>Members

 **ulbLpszLabelName**
  
> Position im Speicher der Zeichenfolgenbezeichnung.
    
 **ulFlags**
  
> Bitmaske der Flags, mit denen das Format der Bezeichnung festgelegt wird, auf die durch das **ulbLpszLabelName** -Element verwiesen wird. Das folgende Flag kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die Bezeichnung ist im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.
    
## <a name="remarks"></a>Bemerkungen

Eine **DTBLLABEL** -Struktur beschreibt einen Beschriftungssteuerelement Text, der mit einem anderen Steuerelementtyp angezeigt wird, um diesem Steuerelement eine Bedeutung hinzuzufügen. Die meisten Bearbeitungssteuerelemente werden beispielsweise neben Bezeichnungen positioniert, um den Benutzer über den Typ der einzugebenden Informationen zu informieren. Einige Steuerelemente wie Gruppen-und Optionsfelder enthalten eigene Beschriftungen. 
  
Die Bezeichnung kann eine Windows-Schnellinfo aufweisen, die als Zeichen nach dem kaufmännischen und (&amp;) identifiziert wird. Durch Drücken der Tastenkombination wird der Fokus in das erste nicht-Schaltflächen-Steuerelement, das dieser Beschriftung folgt, in der Anzeigetabelle platziert.
  
Mehrzeilige Beschriftungen werden nicht unterstützt. Das Anzeigen mehrerer Zeilen erfordert mehrere Bezeichnungen.
  
Eine Bezeichnung kann nicht als schreibgeschütztes Bearbeitungssteuerelement verwendet werden. Der Unterschied besteht darin, dass ein Bearbeitungssteuerelement ausgewählt und kopiert werden kann, während eine Bezeichnung nicht. 
  
Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md). Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

