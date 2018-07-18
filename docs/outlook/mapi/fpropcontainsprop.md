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
ms.openlocfilehash: abf33e4167d836aeb88fdefb30ba05840e80ce63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791743"
---
# <a name="fpropcontainsprop"></a>FPropContainsProp

**Betrifft**: Outlook 
  
Vergleicht zwei Eigenschaftswerte, im Allgemeinen Zeichenfolgen oder binäre Arrays, um festzustellen, ob eines der anderen enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a>Parameter

_lpSPropValueDst_
  
> [in] Zeiger auf eine [SPropValue](spropvalue.md) Struktur definieren den Wert der Eigenschaft, der die zu suchende Zeichenfolge enthalten möglicherweise auf den durch den Parameter _LpSPropValueSrc_ verwiesen. 
    
_lpSPropValueSrc_
  
> [in] Zeiger auf eine **SPropValue** -Struktur, die die zu suchende Zeichenfolge, die **FPropContainsProp** Suchvorgänge ist in der Eigenschaftswert, der auf den durch den Parameter _LpSPropValueDst_ definieren. 
    
_ulFuzzyLevel_
  
> [in] Optionen definieren die Ebene der Webseitenentwicklung im Vergleich zu verwenden. 

  - Die **unteren 16 Bit** gelten für Eigenschaften vom Typ, PT_BINARY und PT_STRING8. Sie müssen auf genau einem der folgenden Werte festgelegt werden:
      
    - FL_FULLSTRING: Die _LpSPropValueSrc_ Suchzeichenfolge muss der Wert der Eigenschaft _LpSPropValueDst_identifizierten entsprechen.
        
    - FL_PREFIX: Die _LpSPropValueSrc_ Suchzeichenfolge muss am Anfang der Wert der Eigenschaft _LpSPropValueDst_identifizierten angezeigt werden. Die beiden Werte sollten nur bis zur Länge der Suchzeichenfolge angegeben durch _LpSPropValueSrc_verglichen werden. 
        
    - FL_SUBSTRING: Die _LpSPropValueSrc_ Suchzeichenfolge muss an einer beliebigen Stelle im _LpSPropValueDst_identifizierten-Eigenschaftenwert enthalten sein. 
      
  - Die **oberen 16 Bit** gelten nur für Eigenschaften vom Typ PT_STRING8. Sie können auf die folgenden Werte in beliebiger Kombination festgelegt werden:
    
    - FL_IGNORECASE: Ohne Berücksichtigung der Groß-/Kleinschreibung sollte der Vergleich durchgeführt werden. 
        
    - FL_IGNORENONSPACE: Der Vergleich sollten definierten Unicode Zeichen ohne Zwischenraum wie diakritischen Zeichen ignorieren. 
        
    - FL_LOOSE: Der Vergleich sollte eine Übereinstimmung nach Möglichkeit ignorieren Fall angeben Empfindlichkeit und Zeichen ohne Zwischenraum.
    
## <a name="return-value"></a>R�ckgabewert

TRUE 
  
> Die Parameter gültig sind und die _LpSPropValueSrc_ zu suchende Zeichenfolge enthalten ist der Wert der _LpSPropValueDst_ -Eigenschaft angegeben. 
    
FALSE 
  
> Die verglichenen Eigenschaftswerte sind nicht vom Typ PT_STRING8 oder PT_BINARY, die Eigenschaftswerte werden verschiedene Typen oder nicht enthalten, die zu suchende Zeichenfolge _LpSPropValueSrc_ wie in der Wert der _LpSPropValueDst_ -Eigenschaft angegeben. 
    
## <a name="remarks"></a>Bemerkungen

Die Vergleichsmethode hängt davon ab, die in die Definitionen der [SPropValue](spropvalue.md) -Eigenschaft angegebene Eigenschaftentypen und die fuzzy Ebene Heuristik im _UlFuzzyLevel_ -Parameter angegeben. Die Funktionen [FPropCompareProp](fpropcompareprop.md) und **FPropContainsProp** können verwendet werden, um Einschränkungen zum Generieren einer Tabelle vorzubereiten. 
  
Die oberen 16 Bit _UlFuzzyLevel_ werden für den Eigenschaftentyp PT_BINARY ignoriert. Wenn die Einstellungen in _UlFuzzyLevel_ fehlt oder ist ungültig sind, wird eine genaue Übereinstimmung Full-Zeichenfolge durchgeführt. Weitere Informationen zur Eigenschaft Beschränkung finden Sie unter der Struktur [SContentRestriction](scontentrestriction.md) . 
  

