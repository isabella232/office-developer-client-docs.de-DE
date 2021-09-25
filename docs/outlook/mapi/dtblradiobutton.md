---
title: DTBLRADIOBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLRADIOBUTTON
api_type:
- COM
ms.assetid: 64cef938-ef6f-43bb-8f6e-d4cd4d6c9888
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 323699bd8964e1da03dff3620bbaa17b78edeca6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588112"
---
# <a name="dtblradiobutton"></a>DTBLRADIOBUTTON

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt ein Optionsfeld, das Teil einer Optionsfeldgruppe sein wird. Die Optionsfeldgruppe wird in einem Dialogfeld verwendet, das aus einer Anzeigetabelle erstellt wird.
  
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
  
> Position im Speicher der Zeichenfolgenbeschriftung für das Optionsfeld.
    
 **ulFlags**
  
> Bitmaske von Flags, die zum Festlegen des Formats der Bezeichnung verwendet werden, auf die vom **ulbLpszLabel-Element** verwiesen wird. Das folgende Kennzeichen kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die Beschriftung hat das Unicode-Format. Wenn das MAPI_UNICODE-Kennzeichen nicht festgelegt ist, hat die Bezeichnung das ANSI-Format.
    
 **ulcButtons**
  
> Anzahl der Schaltflächen in der Optionsfeldgruppe. Die **DTBLRADIOBUTTON-Strukturen** für die anderen Schaltflächen in der Gruppe müssen in aufeinander folgenden Zeilen der Anzeigetabelle enthalten sein. Jede dieser Zeilen sollte denselben Wert für das **Element "ulcButtons"** enthalten. 
    
 **ulPropTag**
  
> Eigenschaftstag für eine Eigenschaft vom Typ PT_LONG. Die anfängliche Auswahl in der Optionsfeldgruppe basiert auf dem Anfangswert dieser Eigenschaft. Für jede Schaltfläche in der Gruppe muss **"ulPropTag"** auf dieselbe Eigenschaft festgelegt sein. 
    
 **lReturnValue**
  
> Eindeutige Nummer, die die ausgewählte Schaltfläche identifiziert.
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine **DTBLRADIOBUTTON-Struktur** beschreibt ein Optionsfeld-Steuerelement, das einer Gruppe von Schaltflächen zugeordnet ist. Es kann nur eine Schaltfläche in der Gruppe überprüft werden. Wenn Sie eine Schaltfläche festlegen, werden die anderen Schaltflächen in der Gruppe nicht mehr festgelegt. 
  
Die Anzahl der Schaltflächen ist die Anzahl der Optionsfelder in der Gruppe. Die Strukturen für die anderen Optionsfelder in der Gruppe müssen sich in nachfolgenden Zeilen in der Anzeigetabelle befinden. Jede dieser Strukturen sollte den gleichen Wert für die Anzahl der Schaltflächen haben.
  
Eine Übersicht über Anzeigetabellen finden Sie unter ["Anzeigetabellen".](display-tables.md) Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle.](display-table-implementation.md)
  
## <a name="see-also"></a>Siehe auch



[BuildDisplayTable](builddisplaytable.md)
  
[DTCTL](dtctl.md)
  
[SizedDtblButton](sizeddtblbutton.md)


[MAPI-Strukturen](mapi-structures.md)

