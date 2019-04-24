---
title: FPropContainsProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropContainsProp
api_type:
- COM
ms.assetid: 43da5b59-7691-49aa-b83c-753d43bfd8fd
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ea56996ad56bb4ce93d103a75eba2c29e6059a87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328042"
---
# <a name="fpropcontainsprop"></a>FPropContainsProp

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Eigenschaftswerte, in der Regel Zeichenfolgen oder binäre Arrays, um zu sehen, ob eine die andere enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a>Parameter

_lpSPropValueDst_
  
> in Zeiger auf eine [SPropValue](spropvalue.md) -Struktur, die den Eigenschaftswert definiert, der die Suchzeichenfolge enthalten kann, auf die durch den _lpSPropValueSrc_ -Parameter verwiesen wird. 
    
_lpSPropValueSrc_
  
> in Zeiger auf eine **SPropValue** -Struktur, die die Suchzeichenfolge definiert, die **FPropContainsProp** im Eigenschaftswert sucht, der durch den _lpSPropValueDst_ -Parameter verweist. 
    
_ulFuzzyLevel_
  
> in Optionseinstellungen definieren die Genauigkeitsstufe für den Vergleich. 

  - Die **unteren 16 Bits** gelten für die Eigenschaften vom Typ PT_BINARY und PT_String8. Sie müssen auf einen der folgenden Werte festgelegt werden:
      
    - FL_FULLSTRING: die _lpSPropValueSrc_ -Suchzeichenfolge muss dem durch _lpSPropValueDst_angegebenen Eigenschaftswert entsprechen.
        
    - FL_PREFIX: die _lpSPropValueSrc_ -Suchzeichenfolge muss am Anfang des durch _lpSPropValueDst_angegebenen Eigenschaftswerts angezeigt werden. Die beiden Werte sollten nur bis zur Länge der durch _lpSPropValueSrc_angegebenen Suchzeichenfolge verglichen werden. 
        
    - FL_SUBSTRING: die _lpSPropValueSrc_ -Suchzeichenfolge muss an beliebiger Stelle im von _lpSPropValueDst_angegebenen Eigenschaftswert enthalten sein. 
      
  - Die **oberen 16 Bits** gelten nur für Eigenschaften vom Typ PT_String8. Sie können in einer beliebigen Kombination auf die folgenden Werte festgelegt werden:
    
    - FL_IGNORECASE: der Vergleich sollte ohne Berücksichtigung der Groß-/Kleinschreibung vorgenommen werden. 
        
    - FL_IGNORENONSPACE: der Vergleich sollte Unicode-definierte Zeichen, die nicht im Abstand stehen, wie diakritische Marken, ignorieren. 
        
    - FL_LOOSE: der Vergleich sollte nach Möglichkeit eine Übereinstimmung aufweisen, wobei die Groß-/Kleinschreibung und die Zeichen ohne Abstand ignoriert werden.
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Die Parameter sind alle gültig, und die _lpSPropValueSrc_ -Suchzeichenfolge ist im Wert der _lpSPropValueDst_ -Eigenschaft enthalten. 
    
FALSE 
  
> Die verglichenen Eigenschaftswerte sind nicht vom Typ PT_STRING8 oder PT_BINARY, die Eigenschaftswerte sind unterschiedlichen Typen, oder die _lpSPropValueSrc_ -Suchzeichenfolge ist nicht wie im Wert der _lpSPropValueDst_ -Eigenschaft angegeben. 
    
## <a name="remarks"></a>Bemerkungen

Die Vergleichsmethode hängt von den Eigenschaftentypen ab, die in den [SPropValue](spropvalue.md) -Eigenschaftsdefinitionen und der heuristischen Heuristik im _ulFuzzyLevel_ -Parameter angegeben sind. Die [FPropCompareProp](fpropcompareprop.md) -und **FPropContainsProp** -Funktionen können verwendet werden, um Einschränkungen für das Generieren einer Tabelle vorzubereiten. 
  
Die oberen 16 Bits von _ulFuzzyLevel_ werden für den Eigenschaftentyp PT_BINARY ignoriert. Wenn die Einstellungen in _ulFuzzyLevel_ fehlen oder ungültig sind, wird eine exakte Übereinstimmung mit vollständiger Zeichenfolge ausgeführt. Weitere Informationen zur Eigenschafts Kapselung finden Sie in der [SContentRestriction](scontentrestriction.md) -Struktur. 
  

