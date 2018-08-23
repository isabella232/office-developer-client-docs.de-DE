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
ms.openlocfilehash: 43703051193ffacec6a54355eeea74edf904f186
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580572"
---
# <a name="scontentrestriction"></a>SContentRestriction
 
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Content Einschränkung, die verwendet wird, um einer Tabellenansicht, um nur die Zeilen zu begrenzen, die eine Spalte mit eine Suchzeichenfolge übereinstimmenden Inhalt enthalten. 
  
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
  
> Einstellungen für die Option definieren Sie die Ebene der Webseitenentwicklung, die Content erzwingen sollten, wenn Sie nach einer Übereinstimmung überprüfen.
    
   Die **unteren 16 Bit** des Elements **UlFuzzyLevel** gelten für Eigenschaften vom Typ PT_BINARY und PT_STRING8 und muss auf einen der folgenden Werte festgelegt werden: 
    
   - FL_FULLSTRING: Um übereinstimmen, muss die **LpProp** zu suchende Zeichenfolge in der Eigenschaft identifizierten **UlPropTag**befinden.
        
   - FL_PREFIX: Entsprechend, muss die Suchzeichenfolge **LpProp** am Anfang der **UlPropTag**identifizierten-Eigenschaft angezeigt werden. Die beiden Zeichenfolgen sollte nur bis zur Länge der Suchzeichenfolge angegeben durch **LpProp**verglichen werden. 
        
   - FL_SUBSTRING: Entsprechend, muss die Suchzeichenfolge **LpProp** an einer beliebigen Stelle in der Eigenschaft identifizierten **UlPropTag**enthalten sein. 
        
   Die **oberen 16 Bit** des Elements **UlFuzzyLevel** gelten nur für Eigenschaften vom Typ PT_STRING8 und kann auf in beliebiger Kombination der folgenden Werte festgelegt werden: 
        
   - FL_IGNORECASE: Ohne Berücksichtigung der Fall sollte der Vergleich durchgeführt werden. 
        
   - FL_IGNORENONSPACE: Der Vergleich sollten Unicode-defined nicht-gesperrte Zeichen wie etwa diakritischen Zeichen ignorieren. 
        
   - FL_LOOSE: Der Vergleich, sollten Sie eine Übereinstimmung nach Möglichkeit Groß-/Kleinschreibung und nicht-gesperrte Zeichen ignorieren verfügen. 
    
**ulPropTag**
  
> Eigenschafts-Tag, identifiziert der Zeichenfolgeneigenschaft nach Vorkommen der Suchzeichenfolge überprüft werden soll. 
    
**lpProp**
  
> Zeiger auf eine Eigenschaft-Wert-Struktur, die den Zeichenfolgenwert für die Verwendung als die zu suchende Zeichenfolge enthält.
    
## <a name="remarks"></a>HinwBemerkungeneise

Es gibt zwei Eigenschaftentags in eine **SContentRestriction** -Struktur: eine in das **UlPropTag** -Element, und der andere im **UlPropTag** -Member der Struktur **SPropValue** auf die **LpProp**zeigt. In beiden Kategorien MAPI erfordert nur das Eigenschaftenfeld und das Feld für den Bezeichner ignoriert. Jedoch müssen die beiden Eigenschaftstypen übereinstimmen, sonst den Fehlerwert MAPI_E_TOO_COMPLEX wird zurückgegeben, wenn die Einschränkung wieder in einem Aufruf von [Methode IMAPITable:: Restrict](imapitable-restrict.md) oder [IMAPITable](imapitable-findrow.md)verwendet wird. 
  
Die Werte FL_FULLSTRING, FL_PREFIX und FL_SUBSTRING schließen sich gegenseitig aus. Nur eine von ihnen festgelegt werden kann, und einer von ihnen festgelegt werden muss. Ihre Bedeutung behoben werden, und der Anbieter muss diese genau wie definiert implementieren. Der Anbieter sollte MAPI_E_TOO_COMPLEX zurückgegeben, wenn diese Werte unterstützen kann. 
  
Die Werte FL_IGNORECASE, FL_IGNORENONSPACE und FL_LOOSE sind unabhängig. An einer beliebigen Stelle kann zwischen 0 (null), um alle drei festgelegt werden. Ihre Definitionen als nur eine Richtlinie bereitgestellt werden, und der Anbieter kann eine eigene spezifische Bedeutung von jedes Flag implementieren. Der Anbieter sollte keine Fehler weist darauf hin zurück, wenn es keine Implementierung eines angegebenen Flags vorhanden ist. 
  
Das Ergebnis der Inhalt beschränkt gegen eine Eigenschaft ist nicht definiert, wenn die Eigenschaft nicht vorhanden ist. Wenn ein Client eindeutig definiertes Verhalten für eine solche Beschränkung erfordert und nicht sicher ist, ob die Eigenschaft beispielsweise vorhanden ist, sie keine erforderliche Spalte einer Tabelle ist, sollten sie eine Einschränkung **und** zum Beitreten der Content Beschränkung mit einer Einschränkung vorhanden erstellen. Verwenden Sie eine [SExistRestriction](sexistrestriction.md) -Struktur, um die Einschränkung vorhanden und eine [SAndRestriction](sandrestriction.md) -Struktur so definieren Sie die Einschränkung **und** definieren. 
  
Weitere Informationen zu den **SContentRestriction** Struktur und Einschränkungen im Allgemeinen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).
  
## <a name="see-also"></a>Siehe auch

- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [MAPI-Strukturen](mapi-structures.md)

