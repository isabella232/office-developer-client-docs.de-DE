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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 87be6df27a3e6729cb514118438521d76a66b30c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339837"
---
# <a name="scontentrestriction"></a>SContentRestriction
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Inhaltseinschränkung, die verwendet wird, um eine Tabellenansicht auf die Zeilen einzuschränken, die eine Spalte mit Inhalten aufweisen, die mit einer Suchzeichenfolge übereinstimmen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
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
  
> Optionseinstellungen definieren die Genauigkeitsstufe, die die Inhaltseinschränkung erzwingen soll, wenn Sie eine Übereinstimmung überprüfen.
    
   Die **unteren 16 Bits** des **ulFuzzyLevel** -Elements gelten für die Eigenschaften vom Typ PT_BINARY und PT_String8 und müssen auf einen der folgenden Werte festgelegt werden: 
    
   - FL_FULLSTRING: zur Übereinstimmung muss die **lpProp** -Suchzeichenfolge in der durch **ulPropTag**angegebenen Eigenschaft enthalten sein.
        
   - FL_PREFIX: zur Übereinstimmung muss die **lpProp** -Suchzeichenfolge am Anfang der durch **ulPropTag**angegebenen Eigenschaft angezeigt werden. Die beiden Zeichenfolgen sollten nur bis zur Länge der durch **lpProp**angegebenen Suchzeichenfolge verglichen werden. 
        
   - FL_SUBSTRING: zur Übereinstimmung muss die **lpProp** -Suchzeichenfolge an beliebiger Stelle in der durch **ulPropTag**angegebenen Eigenschaft enthalten sein. 
        
   Die **oberen 16 Bits** des **ulFuzzyLevel** -Elements gelten nur für Eigenschaften vom Typ PT_String8 und können in einer beliebigen Kombination auf die folgenden Werte festgelegt werden: 
        
   - FL_IGNORECASE: der Vergleich sollte ohne Berücksichtigung der Groß-/Kleinschreibung erfolgen. 
        
   - FL_IGNORENONSPACE: der Vergleich sollte Unicode-definierte Zeichen, die nicht im Abstand stehen, wie diakritische Marken, ignorieren. 
        
   - FL_LOOSE: der Vergleich sollte, wenn möglich, eine Übereinstimmung erhalten, wobei die Zeichen für Groß-/Kleinschreibung und nicht-Abstand ignoriert werden. 
    
**ulPropTag**
  
> Property-Tag, der die Zeichenfolgeneigenschaft identifiziert, die auf das Vorkommen der Suchzeichenfolge überprüft werden soll. 
    
**lpProp**
  
> Zeiger auf eine Eigenschaftswert Struktur, die den Zeichenfolgenwert enthält, der als Suchzeichenfolge verwendet werden soll.
    
## <a name="remarks"></a>Bemerkungen

Es gibt zwei Property-Tags in einer **SContentRestriction** -Struktur: eine im **ulPropTag** -Element und die andere im **ulPropTag** -Element der **SPropValue** -Struktur, auf die von **lpProp**verwiesen wird. In beiden Tags erfordert MAPI nur das Feld Eigenschafts und ignoriert das Feld Eigenschaftsbezeichner. Die beiden Eigenschaftentypen müssen jedoch übereinstimmen, andernfalls wird der Fehlerwert MAPI_E_TOO_COMPLEX zurückgegeben, wenn die Einschränkung in einem Aufruf von [IMAPITable:: Restrict](imapitable-restrict.md) oder [IMAPITable:: FindRow](imapitable-findrow.md)verwendet wird. 
  
Die Werte FL_FULLSTRING, FL_PREFIX und FL_SUBSTRING schließen sich gegenseitig aus. Nur einer davon kann festgelegt werden, und eine davon muss festgelegt werden. Ihre Bedeutungen sind festgelegt, und der Anbieter muss Sie genau wie definiert implementieren. Der Anbieter sollte MAPI_E_TOO_COMPLEX zurückgeben, wenn diese Werte nicht unterstützt werden können. 
  
Die Werte FL_IGNORECASE, FL_IGNORENONSPACE und FL_LOOSE sind unabhängig. Überall von Null bis alle drei können festgelegt werden. Ihre Definitionen werden nur als Richtlinie bereitgestellt, und der Anbieter kann seine eigene spezifische Bedeutung jeder Kennzeichnung implementieren. Der Anbieter sollte keine Fehlermeldung zurückgeben, wenn er keine Implementierung eines angegebenen Flags hat. 
  
Das Ergebnis einer Inhaltseinschränkung für eine Eigenschaft ist nicht definiert, wenn die Eigenschaft nicht vorhanden ist. Wenn ein Client ein genau definiertes Verhalten für eine solche Einschränkung benötigt und nicht sicher ist, ob die Eigenschaft beispielsweise vorhanden ist, ist es keine erforderliche Spalte einer Tabelle, es sollte eine **und** -Einschränkung erstellen, um der Inhaltseinschränkung mit einer exist-Einschränkung beizutreten. Verwenden Sie eine [SExistRestriction](sexistrestriction.md) -Struktur, um die exist-Einschränkung und eine [SAndRestriction](sandrestriction.md) -Struktur zum Definieren der **und-** Einschränkung zu definieren. 
  
Weitere Informationen zur **SContentRestriction** -Struktur und zu Einschränkungen im Allgemeinen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).
  
## <a name="see-also"></a>Siehe auch

- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [MAPI-Strukturen](mapi-structures.md)

