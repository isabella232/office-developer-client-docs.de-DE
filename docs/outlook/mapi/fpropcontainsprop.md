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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ea56996ad56bb4ce93d103a75eba2c29e6059a87
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432631"
---
# <a name="fpropcontainsprop"></a>FPropContainsProp

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Eigenschaftswerte, in der Regel Zeichenfolgen oder binäre Arrays, um zu sehen, ob einer den anderen enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a>Parameter

_lpSPropValueDst_
  
> [in] Zeiger auf eine [SPropValue-Struktur,](spropvalue.md) die den Eigenschaftswert definiert, der die Suchzeichenfolge enthalten kann, auf die der  _lpSPropValueSrc-Parameter_ verweist. 
    
_lpSPropValueSrc_
  
> [in] Zeiger auf eine **SPropValue-Struktur,** die die Suchzeichenfolge definiert, die **FPropContainsProp** in dem Eigenschaftswert sucht, auf den der  _lpSPropValueDst-Parameter_ verweist. 
    
_ulFuzzyLevel_
  
> [in] Optionseinstellungen, die die im Vergleich zu verwendende Präzisionsstufe definieren. 

  - Die **unteren 16 Bit** gelten für Eigenschaften vom Typ PT_BINARY und PT_STRING8. Sie müssen auf genau einen der folgenden Werte festgelegt werden:
      
    - FL_FULLSTRING: Die _lpSPropValueSrc-Suchzeichenfolge_ muss gleich dem Eigenschaftswert sein, der von _lpSPropValueDst identifiziert wird._
        
    - FL_PREFIX: Die _lpSPropValueSrc-Suchzeichenfolge_ muss am Anfang des durch _lpSPropValueDst identifizierten Eigenschaftswerts angezeigt werden._ Die beiden Werte sollten nur bis zur Länge der suchzeichenfolge verglichen werden, die von _lpSPropValueSrc angegeben wird._ 
        
    - FL_SUBSTRING: Die _lpSPropValueSrc-Suchzeichenfolge_ muss an einer beliebigen Stelle im Eigenschaftswert enthalten sein, der von _lpSPropValueDst identifiziert wird._ 
      
  - Die **oberen 16 Bit gelten** nur für Eigenschaften vom Typ PT_STRING8. Sie können in beliebiger Kombination auf die folgenden Werte festgelegt werden:
    
    - FL_IGNORECASE: Der Vergleich sollte ohne Berücksichtigung der Fallempfindlichkeit vorgenommen werden. 
        
    - FL_IGNORENONSPACE: Der Vergleich sollte Unicode-definierte Zeichen ohne Abstand ignorieren, z. B. diakritische Zeichen. 
        
    - FL_LOOSE: Der Vergleich sollte nach Möglichkeit eine Übereinstimmung angeben, wobei die Zwischenfallempfindlichkeit und zeichenfreier Abstand ignoriert werden.
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Die Parameter sind alle gültig, und die  _lpSPropValueSrc-Suchzeichenfolge_ ist wie im  _lpSPropValueDst-Eigenschaftswert_ angegeben enthalten. 
    
FALSE 
  
> Die zu vergleichenden Eigenschaftswerte sind nicht vom Typ PT_STRING8 oder PT_BINARY, die Eigenschaftswerte sind unterschiedliche Typen, oder die  _lpSPropValueSrc-Suchzeichenfolge_ ist nicht wie im  _lpSPropValueDst-Eigenschaftswert_ angegeben enthalten. 
    
## <a name="remarks"></a>Hinweise

Die Vergleichsmethode hängt von den in den [SPropValue-Eigenschaftsdefinitionen](spropvalue.md) angegebenen Eigenschaftstypen und der im  _ulFuzzyLevel-Parameter_ bereitgestellten Heuristik auf Fuzzyebene ab. Die [Funktionen FPropCompareProp](fpropcompareprop.md) und **FPropContainsProp** können verwendet werden, um Einschränkungen für das Generieren einer Tabelle vorzubereiten. 
  
Die oberen 16 Bits von  _ulFuzzyLevel_ werden für Eigenschaftentyptypen PT_BINARY. Wenn die Einstellungen in  _ulFuzzyLevel_ fehlen oder ungültig sind, wird eine genaue Übereinstimmung mit der vollständigen Zeichenfolge ausgeführt. Weitere Informationen zum Eindämmung von Eigenschaften finden Sie in der [SContentRestriction-Struktur.](scontentrestriction.md) 
  

