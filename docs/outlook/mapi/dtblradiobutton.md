---
title: DTBLRADIOBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLRADIOBUTTON
api_type:
- COM
ms.assetid: 64cef938-ef6f-43bb-8f6e-d4cd4d6c9888
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: dee12ba9da83d2167afe13d00270a900bf0d73d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791612"
---
# <a name="dtblradiobutton"></a>DTBLRADIOBUTTON

  
  
**Betrifft**: Outlook 
  
Beschreibt ein Optionsfeld, die an eine Gruppe von Optionsfeldern werden sollen. Die Gruppe von Optionsfeldern wird in einem Dialogfeld verwendet werden, die aus einer Tabelle anzeigen erstellt wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLRADIOBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulcButtons;
  ULONG ulPropTag;
  long lReturnValue;
} DTBLRADIOBUTTON, FAR *LPDTBLRADIOBUTTON;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Die Position im Speicher der Zeichen Zeichenfolge Bezeichnung für das Optionsfeld.
    
 **ulFlags**
  
> Bitmaske aus Flags verwendet, um das Format der Beschriftung festzulegen, auf die der **UlbLpszLabel** Member. Das folgende Flag kann festgelegt werden: 
    
PARAMETER MAPI_UNICODE 
  
> Die Beschriftung wird im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.
    
 **ulcButtons**
  
> Anzahl der Schaltflächen in der Gruppe von Optionsfeldern. Die **DTBLRADIOBUTTON** Strukturen für die anderen Schaltflächen in der Gruppe müssen in aufeinander folgenden Zeilen der Tabelle anzeigen enthalten sein. Jeder dieser Zeilen sollte den gleichen Wert für das **UlcButtons** -Element enthalten. 
    
 **ulPropTag**
  
> Eigenschaftentag für eine Eigenschaft vom Typ PT_LONG. Die ursprüngliche Auswahl in die Gruppe von Optionsfeldern basiert auf den ursprünglichen Wert dieser Eigenschaft. Jede Schaltfläche in der Gruppe benötigen **UlPropTag** auf dieselbe Eigenschaft festgelegt. 
    
 **lReturnValue**
  
> Eindeutige Zahl, die die ausgewählte Schaltfläche identifiziert.
    
## <a name="remarks"></a>Hinweise

Eine Struktur **DTBLRADIOBUTTON** beschreibt ein Optionsfeld ein Button-Steuerelement, das eine Gruppe von Schaltflächen zugeordnet ist. Es kann nur eine Schaltfläche in der Gruppe überprüft werden soll; Festlegen einer Schaltfläche bewirkt, dass die anderen Schaltflächen in der Gruppe nicht festgelegt werden. 
  
Der Wert der Schaltfläche wird die Anzahl der Optionsfelder in der Gruppe. Die Strukturen für die anderen Optionsfelder in der Gruppe müssen in folgenden Zeilen in der Tabelle angezeigt werden. Jedes dieser Strukturen sollte den gleichen Wert für die Anzahl der Schaltfläche aufweisen.
  
Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md). Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[BuildDisplayTable](builddisplaytable.md)
  
[DTCTL](dtctl.md)
  
[SizedDtblButton](sizeddtblbutton.md)


[MAPI-Strukturen](mapi-structures.md)

