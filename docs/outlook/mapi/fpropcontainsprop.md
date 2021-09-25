---
title: FPropContainsProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FPropContainsProp
api_type:
- COM
ms.assetid: 43da5b59-7691-49aa-b83c-753d43bfd8fd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c20b1bf6ba7a109db4e772e31faf53fa3c3f4179
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564386"
---
# <a name="fpropcontainsprop"></a>FPropContainsProp

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Eigenschaftswerte, in der Regel Zeichenfolgen oder binäre Arrays, um festzustellen, ob einer den anderen enthält. 
  
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
  
> [in] Zeiger auf eine [SPropValue-Struktur,](spropvalue.md) die den Eigenschaftswert definiert, der die Suchzeichenfolge enthalten kann, auf die der  _parameter lpSPropValueSrc_ verweist. 
    
_lpSPropValueSrc_
  
> [in] Zeiger auf eine **SPropValue-Struktur,** die die Suchzeichenfolge definiert, die **FPropContainsProp** in dem Eigenschaftswert sucht, auf den der  _parameter lpSPropValueDst_ verweist. 
    
_ulFuzzyLevel_
  
> [in] Optionseinstellungen, die den Grad der Genauigkeit definieren, der im Vergleich verwendet werden soll. 

  - Die **unteren 16 Bits** gelten für Eigenschaften vom Typ PT_BINARY und PT_STRING8. Sie müssen auf genau einen der folgenden Werte festgelegt werden:
      
    - FL_FULLSTRING: Die Suchzeichenfolge  _lpSPropValueSrc_ muss dem von  _lpSPropValueDst_ identifizierten Eigenschaftswert entsprechen.
        
    - FL_PREFIX: Die Suchzeichenfolge  _lpSPropValueSrc_ muss am Anfang des durch  _lpSPropValueDst_ identifizierten Eigenschaftswerts angezeigt werden. Die beiden Werte sollten nur bis zur Länge der durch  _lpSPropValueSrc_ angegebenen Suchzeichenfolge verglichen werden. 
        
    - FL_SUBSTRING: Die Suchzeichenfolge  _lpSPropValueSrc_ muss an einer beliebigen Stelle in dem von  _lpSPropValueDst_ identifizierten Eigenschaftswert enthalten sein. 
      
  - Die **oberen 16 Bits** gelten nur für Eigenschaften vom Typ PT_STRING8. Sie können in einer beliebigen Kombination auf die folgenden Werte festgelegt werden:
    
    - FL_IGNORECASE: Der Vergleich sollte ohne Berücksichtigung der Groß-/Kleinschreibung durchgeführt werden. 
        
    - FL_IGNORENONSPACE: Der Vergleich sollte Unicode-definierte nicht übergreifende Zeichen wie diakritische Markierungen ignorieren. 
        
    - FL_LOOSE: Der Vergleich sollte nach Möglichkeit eine Übereinstimmung angeben, wobei die Groß-/Kleinschreibung und zeichenfreie Zeichen ignoriert werden.
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Die Parameter sind alle gültig, und die Suchzeichenfolge  _lpSPropValueSrc_ ist wie im  _LpSPropValueDst-Eigenschaftswert_ angegeben enthalten. 
    
FALSE 
  
> Die verglichenen Eigenschaftswerte sind nicht vom Typ PT_STRING8 oder PT_BINARY, die Eigenschaftswerte weisen unterschiedliche Typen auf, oder die Suchzeichenfolge  _"lpSPropValueSrc"_ ist nicht wie im  _LpSPropValueDst-Eigenschaftswert_ angegeben enthalten. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Vergleichsmethode hängt von den in den [SPropValue-Eigenschaftsdefinitionen](spropvalue.md) angegebenen Eigenschaftstypen und der heuristischen Fuzzyebene ab, die im  _ulFuzzyLevel-Parameter_ bereitgestellt wird. Die Funktionen [FPropCompareProp](fpropcompareprop.md) und **FPropContainsProp** können verwendet werden, um Einschränkungen für das Generieren einer Tabelle vorzubereiten. 
  
Die oberen 16 Bits von  _ulFuzzyLevel_ werden für eigenschaftentyp PT_BINARY ignoriert. Wenn die Einstellungen in  _ulFuzzyLevel_ fehlen oder ungültig sind, wird eine genaue Übereinstimmung mit einer vollständigen Zeichenfolge ausgeführt. Weitere Informationen zur Eigenschaftseinschluss finden Sie in der [Struktur "SContentRestriction".](scontentrestriction.md) 
  

