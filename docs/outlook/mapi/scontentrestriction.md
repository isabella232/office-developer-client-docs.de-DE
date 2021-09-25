---
title: SContentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SContentRestriction
api_type:
- COM
ms.assetid: 784c8a5a-493e-48e6-8784-ba8122c76e3d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c007d2ea61810aa93685a2d91836afdc4209d623
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624279"
---
# <a name="scontentrestriction"></a>SContentRestriction
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Inhaltseinschränkung, die verwendet wird, um eine Tabellenansicht auf die Zeilen zu beschränken, die eine Spalte enthalten, deren Inhalt einer Suchzeichenfolge entspricht. 
  
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

## <a name="members"></a>Members

**ulFuzzyLevel**
  
> Optionseinstellungen, die den Grad der Genauigkeit definieren, den die Inhaltseinschränkung erzwingen soll, wenn Sie eine Übereinstimmung überprüfen.
    
   Die **unteren 16 Bit** des **ulFuzzyLevel-Elements** gelten für Eigenschaften vom Typ PT_BINARY und PT_STRING8 und müssen auf einen der folgenden Werte festgelegt werden: 
    
   - FL_FULLSTRING: Um eine Übereinstimmung  zu erzielen, muss die lpProp-Suchzeichenfolge in der durch **ulPropTag** identifizierten Eigenschaft enthalten sein.
        
   - FL_PREFIX: Um eine Übereinstimmung  zu erzielen, muss die lpProp-Suchzeichenfolge am Anfang der durch **ulPropTag** identifizierten Eigenschaft angezeigt werden. Die beiden Zeichenfolgen sollten nur bis zur Länge der durch **lpProp** angegebenen Suchzeichenfolge verglichen werden. 
        
   - FL_SUBSTRING: Um eine Übereinstimmung  zu erzielen, muss die lpProp-Suchzeichenfolge an einer beliebigen Stelle in der durch **ulPropTag** identifizierten Eigenschaft enthalten sein. 
        
   Die **oberen 16 Bits** des **ulFuzzyLevel-Elements** gelten nur für Eigenschaften vom Typ PT_STRING8 und können in beliebiger Kombination auf die folgenden Werte festgelegt werden: 
        
   - FL_IGNORECASE: Der Vergleich sollte ohne Berücksichtigung der Groß-/Kleinschreibung durchgeführt werden. 
        
   - FL_IGNORENONSPACE: Der Vergleich sollte unicodedefinierte Nicht-Leerzeichen wie diakritische Markierungen ignorieren. 
        
   - FL_LOOSE: Mit dem Vergleich sollten Sie nach Möglichkeit eine Übereinstimmung erhalten, wobei groß- und kleinschreibungsfreie Zeichen ignoriert werden. 
    
**ulPropTag**
  
> Eigenschaftstag, das die Zeichenfolgeneigenschaft identifiziert, die auf das Vorkommen der Suchzeichenfolge überprüft werden soll. 
    
**lpProp**
  
> Zeiger auf eine Eigenschaftswertstruktur, die den Zeichenfolgenwert enthält, der als Suchzeichenfolge verwendet werden soll.
    
## <a name="remarks"></a>Bemerkungen

Es gibt zwei Eigenschaftstags in einer **SContentRestriction-Struktur:** eines im **ulPropTag-Element** und das andere im **ulPropTag-Element** der **SPropValue-Struktur,** auf das von **lpProp** verwiesen wird. In beiden Tags erfordert MAPI nur das Eigenschaftentypfeld und ignoriert das Eigenschaftsbezeichnerfeld. Die beiden Eigenschaftstypen müssen jedoch übereinstimmen, andernfalls wird der Fehlerwert MAPI_E_TOO_COMPLEX zurückgegeben, wenn die Einschränkung in einem Aufruf von [IMAPITable::Restrict](imapitable-restrict.md) oder [IMAPITable::FindRow](imapitable-findrow.md)verwendet wird. 
  
Die Werte FL_FULLSTRING, FL_PREFIX und FL_SUBSTRING schließen sich gegenseitig aus. Es kann nur eine festgelegt werden, und eine davon muss festgelegt werden. Ihre Bedeutungen sind festgelegt, und der Anbieter muss sie genau wie definiert implementieren. Der Anbieter sollte MAPI_E_TOO_COMPLEX zurückgeben, wenn er diese Werte nicht unterstützen kann. 
  
Die Werte FL_IGNORECASE, FL_IGNORENONSPACE und FL_LOOSE sind unabhängig. Von Null bis alle drei können festgelegt werden. Ihre Definitionen werden nur als Richtlinie bereitgestellt, und der Anbieter kann seine eigene spezifische Bedeutung jedes Flags implementieren. Der Anbieter sollte keine Fehleranzeige zurückgeben, wenn er über keine Implementierung eines angegebenen Flags verfügt. 
  
Das Ergebnis einer für eine Eigenschaft geltenden Inhaltseinschränkung ist nicht definiert, wenn die Eigenschaft nicht vorhanden ist. Wenn ein Client ein klar definiertes Verhalten für eine solche Einschränkung erfordert und nicht sicher ist, ob die Eigenschaft beispielsweise vorhanden ist, handelt es sich nicht um eine erforderliche Spalte einer Tabelle, sollte eine **AND-Einschränkung** erstellt werden, um die Inhaltseinschränkung mit einer vorhandenen Einschränkung zu verknüpfen. Verwenden Sie eine [SExistRestriction-Struktur,](sexistrestriction.md) um die vorhandene Einschränkung zu definieren, und eine [SAndRestriction-Struktur,](sandrestriction.md) um die **AND-Einschränkung** zu definieren. 
  
Weitere Informationen zur Struktur und Einschränkungen von **SContentRestriction** im Allgemeinen finden Sie unter ["Einschränkungen".](about-restrictions.md)
  
## <a name="see-also"></a>Siehe auch

- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [MAPI-Strukturen](mapi-structures.md)

