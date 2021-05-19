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
ms.openlocfilehash: 94e412f2f542298adcedf4414c19b5303330cf2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434599"
---
# <a name="dtblradiobutton"></a>DTBLRADIOBUTTON

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt ein Optionsfeld, das Teil einer Optionsfeldgruppe sein wird. Die Optionsfeldgruppe wird in einem Dialogfeld verwendet, das aus einer Anzeigetabelle erstellt wurde.
  
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
  
> Position im Speicher der Zeichenzeichenfolgenbeschriftung für das Optionsfeld.
    
 **ulFlags**
  
> Bitmaske von Flags, die verwendet werden, um das Format der Bezeichnung zu bestimmen, auf das das **ulbLpszLabel-Element** verweist. Das folgende Flag kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die Bezeichnung ist im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich die Bezeichnung im ANSI-Format.
    
 **ulcButtons**
  
> Anzahl der Schaltflächen in der Optionsfeldgruppe. Die **DTBLRADIOBUTTON-Strukturen** für die anderen Schaltflächen in der Gruppe müssen in aufeinander folgenden Zeilen der Anzeigetabelle enthalten sein. Jede dieser Zeilen sollte denselben Wert für das **ulcButtons-Element** enthalten. 
    
 **ulPropTag**
  
> Eigenschaftstag für eine Eigenschaft vom Typ PT_LONG. Die anfängliche Auswahl in der Optionsfeldgruppe basiert auf dem Anfangswert dieser Eigenschaft. Für jede Schaltfläche in der Gruppe muss **ulPropTag auf** dieselbe Eigenschaft festgelegt sein. 
    
 **lReturnValue**
  
> Eindeutige Nummer, die die ausgewählte Schaltfläche identifiziert.
    
## <a name="remarks"></a>Hinweise

Eine **DTBLRADIOBUTTON-Struktur** beschreibt ein Optionsfeld ein Schaltflächensteuerelement, das einer Gruppe von Schaltflächen zugeordnet ist. Es kann nur eine Schaltfläche in der Gruppe aktiviert werden. Wenn Sie eine Schaltfläche festlegen, werden die anderen Schaltflächen in der Gruppe nicht mehr verwendet. 
  
Die Anzahl der Schaltflächen ist die Anzahl der Optionsfelder in der Gruppe. Die Strukturen für die anderen Optionsfelder in der Gruppe müssen sich in nachfolgenden Zeilen in der Anzeigetabelle enthalten. Jede dieser Strukturen sollte denselben Wert für die Anzahl der Schaltflächen haben.
  
Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md). Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[BuildDisplayTable](builddisplaytable.md)
  
[DTCTL](dtctl.md)
  
[SizedDtblButton](sizeddtblbutton.md)


[MAPI-Strukturen](mapi-structures.md)

