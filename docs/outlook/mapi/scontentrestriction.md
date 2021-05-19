---
title: SContentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SContentRestriction
api_type:
- COM
ms.assetid: 784c8a5a-493e-48e6-8784-ba8122c76e3d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 87be6df27a3e6729cb514118438521d76a66b30c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423664"
---
# <a name="scontentrestriction"></a>SContentRestriction
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Inhaltseinschränkung, die verwendet wird, um eine Tabellenansicht auf die Zeilen zu beschränken, die eine Spalte mit Inhalten enthalten, die mit einer Suchzeichenfolge übereinstimmen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a>Elemente

**ulFuzzyLevel**
  
> Optionseinstellungen, die den Grad der Exaktheit definieren, den die Inhaltseinschränkung erzwingen soll, wenn Sie eine Übereinstimmung überprüfen.
    
   Die **unteren 16** Bit des **ulFuzzyLevel-Members** gelten für Eigenschaften vom Typ PT_BINARY und PT_STRING8 und müssen auf einen der folgenden Werte festgelegt werden: 
    
   - FL_FULLSTRING: Um eine Übereinstimmung zu finden, muss die **lpProp-Suchzeichenfolge** in der eigenschaft enthalten sein, die durch **ulPropTag identifiziert wird.**
        
   - FL_PREFIX : Um eine Übereinstimmung zu finden, muss die **lpProp-Suchzeichenfolge** am Anfang der durch **ulPropTag** identifizierten Eigenschaft angezeigt werden. Die beiden Zeichenfolgen sollten nur bis zur Länge der durch lpProp angegebenen Suchzeichenfolge **verglichen werden.** 
        
   - FL_SUBSTRING: Die **lpProp-Suchzeichenfolge** muss an einer beliebigen Stelle in der durch **ulPropTag** identifizierten Eigenschaft enthalten sein. 
        
   Die **oberen 16** Bit des **ulFuzzyLevel-Members** gelten nur für Eigenschaften vom Typ PT_STRING8 und können in beliebiger Kombination auf die folgenden Werte festgelegt werden: 
        
   - FL_IGNORECASE: Der Vergleich sollte ohne Berücksichtigung der Fälle vorgenommen werden. 
        
   - FL_IGNORENONSPACE: Der Vergleich sollte Unicode-definierte Nichtabstandszeichen, z. B. diakritische Zeichen, ignorieren. 
        
   - FL_LOOSE: Der Vergleich sollte Ihnen nach Möglichkeit eine Übereinstimmung bieten, wobei die Zeichen "Case" und "Non-Spacing" ignoriert werden. 
    
**ulPropTag**
  
> Eigenschaftstag, das die Zeichenfolgeneigenschaft identifiziert, die auf das Vorkommen der Suchzeichenfolge überprüft werden soll. 
    
**lpProp**
  
> Zeiger auf eine Eigenschaftswertstruktur, die den zeichenfolgenwert enthält, der als Suchzeichenfolge verwendet werden soll.
    
## <a name="remarks"></a>Hinweise

Es gibt zwei Eigenschaftstags in einer **SContentRestriction-Struktur:** eines im **ulPropTag-Element** und das andere im **ulPropTag-Element** der **SPropValue-Struktur,** auf die von **lpProp** verwiesen wird. In beiden Tags erfordert MAPI nur das Eigenschaftentypfeld und ignoriert das Eigenschaftenbezeichnerfeld. Die beiden Eigenschaftstypen müssen jedoch übereinstimmen, sonst wird der Fehlerwert MAPI_E_TOO_COMPLEX zurückgegeben, wenn die Einschränkung in einem Aufruf von [IMAPITable::Restrict](imapitable-restrict.md) oder [IMAPITable::FindRow](imapitable-findrow.md)verwendet wird. 
  
Die Werte FL_FULLSTRING, FL_PREFIX und FL_SUBSTRING schließen sich gegenseitig aus. Es kann nur einer von ihnen festgelegt werden, und eine davon muss festgelegt werden. Ihre Bedeutungen sind festgelegt, und der Anbieter muss sie genau wie definiert implementieren. Der Anbieter sollte MAPI_E_TOO_COMPLEX zurückgeben, wenn er diese Werte nicht unterstützen kann. 
  
Die Werte FL_IGNORECASE, FL_IGNORENONSPACE und FL_LOOSE sind unabhängig. Zwischen null und allen drei kann festgelegt werden. Ihre Definitionen werden nur als Richtlinie bereitgestellt, und der Anbieter kann seine eigene spezifische Bedeutung jedes Flags implementieren. Der Anbieter sollte keine Fehleranzeige zurückgeben, wenn er keine Implementierung eines angegebenen Flags besitzt. 
  
Das Ergebnis einer Für eine Eigenschaft auferlegten Inhaltseinschränkung ist nicht definiert, wenn die Eigenschaft nicht vorhanden ist. Wenn ein Client für eine solche Einschränkung ein definiertes Verhalten erfordert und nicht sicher ist, ob die Eigenschaft vorhanden ist, sollte er keine erforderliche Spalte einer Tabelle erstellen und eine **AND-Einschränkung** erstellen, um die Inhaltseinschränkung mit einer vorhandenen Einschränkung zu verbinden. Verwenden Sie eine [SExistRestriction-Struktur,](sexistrestriction.md) um die exist-Einschränkung und eine [SAndRestriction-Struktur](sandrestriction.md) zu definieren, um die **AND-Einschränkung zu** definieren. 
  
Weitere Informationen zur Struktur und Einschränkungen **von SContentRestriction** im Allgemeinen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).
  
## <a name="see-also"></a>Siehe auch

- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [MAPI-Strukturen](mapi-structures.md)

