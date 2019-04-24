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
ms.openlocfilehash: 94e412f2f542298adcedf4414c19b5303330cf2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339417"
---
# <a name="dtblradiobutton"></a>DTBLRADIOBUTTON

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt ein Optionsfeld, das Teil einer Optionsfeldgruppe sein wird. Die Optionsschaltfläche-Gruppe wird in einem Dialogfeldverwendet, das aus einer Anzeigetabelle erstellt wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
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
  
> Position im Speicher der Zeichenfolgenbezeichnung für das Optionsfeld.
    
 **ulFlags**
  
> Bitmaske der Flags, mit denen das Format der Bezeichnung festgelegt wird, auf die durch das **ulbLpszLabel** -Element verwiesen wird. Das folgende Flag kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die Bezeichnung ist im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.
    
 **ulcButtons**
  
> Anzahl der Schaltflächen in der Optionsfeldgruppe. Die **DTBLRADIOBUTTON** -Strukturen für die anderen Schaltflächen in der Gruppe müssen in aufeinanderfolgenden Zeilen der Anzeigetabelle enthalten sein. Jede dieser Zeilen sollte den gleichen Wert für das **ulcButtons** -Element enthalten. 
    
 **ulPropTag**
  
> Property-Tag für eine Eigenschaft vom Typ PT_LONG. Die anfängliche Auswahl in der Optionsfeldgruppe basiert auf dem Anfangswert dieser Eigenschaft. Für jede Schaltfläche in der Gruppe muss **ulPropTag** auf dieselbe Eigenschaft festgelegt sein. 
    
 **lReturnValue**
  
> Eindeutige Zahl, die die ausgewählte Schaltfläche identifiziert.
    
## <a name="remarks"></a>Bemerkungen

Eine **DTBLRADIOBUTTON** -Struktur beschreibt ein Optionsfeld-Steuerelement, das einer Gruppe von Schaltflächen zugeordnet ist. Nur eine Schaltfläche in der Gruppe kann überprüft werden; durch Festlegen einer Schaltfläche werden die anderen Schaltflächen in der Gruppe festgelegt. 
  
Die Schaltflächen Anzahl ist die Anzahl der Optionsfelder in der Gruppe. Die Strukturen für die anderen Optionsfelder in der Gruppe müssen sich in nachfolgenden Zeilen in der Anzeigetabelle befinden. Jede dieser Strukturen sollte den gleichen Wert für die Schaltflächen Anzahl aufweisen.
  
Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md). Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[BuildDisplayTable](builddisplaytable.md)
  
[DTCTL](dtctl.md)
  
[SizedDtblButton](sizeddtblbutton.md)


[MAPI-Strukturen](mapi-structures.md)

