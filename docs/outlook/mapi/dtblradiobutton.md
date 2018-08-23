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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 493176029be3e7b154188aa164a95a8bc9c0e7d9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569743"
---
# <a name="dtblradiobutton"></a>DTBLRADIOBUTTON

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Elemente

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
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine Struktur **DTBLRADIOBUTTON** beschreibt ein Optionsfeld ein Button-Steuerelement, das eine Gruppe von Schaltflächen zugeordnet ist. Es kann nur eine Schaltfläche in der Gruppe überprüft werden soll; Festlegen einer Schaltfläche bewirkt, dass die anderen Schaltflächen in der Gruppe nicht festgelegt werden. 
  
Der Wert der Schaltfläche wird die Anzahl der Optionsfelder in der Gruppe. Die Strukturen für die anderen Optionsfelder in der Gruppe müssen in folgenden Zeilen in der Tabelle angezeigt werden. Jedes dieser Strukturen sollte den gleichen Wert für die Anzahl der Schaltfläche aufweisen.
  
Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md). Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[BuildDisplayTable](builddisplaytable.md)
  
[DTCTL](dtctl.md)
  
[SizedDtblButton](sizeddtblbutton.md)


[MAPI-Strukturen](mapi-structures.md)

