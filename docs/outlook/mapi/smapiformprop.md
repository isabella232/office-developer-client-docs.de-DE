---
title: SMAPIFormProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormProp
api_type:
- COM
ms.assetid: 80f1c2e0-3567-4b16-86cb-d5e6ac95c2ee
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 968f9e1dad3a233b31f0ce29d3ce935b1257948c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416699"
---
# <a name="smapiformprop"></a>SMAPIFormProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine benannte Eigenschaft, die mit einem Formular verwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
   
```cpp
typedef struct _SMAPIFormProp
{
  ULONG ulFlags;
  ULONG nPropType;
  MAPINAMEID nmid;
  LPSTR pszDisplayName;
  FORMPROPSPECIALTYPE nSpecialType;
  union
  {
    struct
    {
      MAPINAMEID nmidIdx;
      ULONG cfpevAvailable;
      LPMAPIFORMPROPENUMVAL pfpevAvailable;
    } s1;
  } u;
} SMAPIFormProp, FAR * LPMAPIFORMPROP;

```

## <a name="members"></a>Elemente

 **ulFlags**
  
> Flags, die zum Unterscheiden des Formats der Zeichenfolgen in der **SMAPIFormProp-Struktur verwendet** werden. Das folgende Flag kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen sind im Unicode-Format. Wenn MAPI_UNICODE nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format angezeigt.
    
 **nPropType**
  
> Typ der benannten Eigenschaft, bei der das wichtigste Wort auf Null festgelegt ist. 
    
 **nmid**
  
> Name für die benannte Eigenschaft, die eine **GUID-Struktur** enthält, die den Eigenschaftensatz identifiziert, sowie einen numerischen wert oder einen Zeichenfolgenwert, der eine Schnittstellen-ID und einen Formularnamen darstellt. 
    
 **pszDisplayName**
  
> Zeiger auf den Anzeigenamen der benannten Eigenschaft.
    
 **nSpecialType**
  
> Wert, der den Typ der im u-Element enthaltenen **Daten** beschreibt. Mögliche Werte sind: 
    
FPST_VANILLA 
  
> Das **u-Element** enthält keine Enumeration. 
    
FPST_ENUM_PROP 
  
> Das **u-Element** enthält eine Struktur, die eine Enumeration beschreibt. 
    
 **u**
  
> Union, die die Zuordnung zwischen dem Namen und der Nummer der benannten Eigenschaft beschreibt. Mithilfe einiger Eigenschaften ist das **u-Element** leer. Bei anderen Eigenschaften wird sie in einer Struktur dargestellt, die aus den folgenden Mitgliedern besteht: 
    
 **nmidIdx**
  
> Die [MAPINAMEID-Struktur,](mapinameid.md) die den Eigenschaftensatz und den Bezeichner für die benannte Eigenschaft enthält. 
    
 **cfpevAvailable**
  
> Anzahl der [SMAPIFormPropEnumVal-Strukturen](smapiformpropenumval.md) im Array, auf die das **pfpevAvailable-Element verweist.** 
    
 **pfpevAvailable**
  
> Zeiger auf ein Array von **SMAPIFormPropEnumVal-Strukturen,** von denen jede einen Wert für die benannte Eigenschaft enthält. 
    
## <a name="remarks"></a>Hinweise

Die **SMAPIFormProp-Struktur** enthält Informationen zu einer Formulareigenschaft, die als Teil der Definitionen der [IMAPIFormInfo-Schnittstelle verwendet](imapiforminfoimapiprop.md) wird. **nSpecialType** enthält ein Tag, das für die **u-Union** gilt, die Teil von **SMAPIFormProp ist.**
  
## <a name="see-also"></a>Siehe auch



[MAPINAMEID](mapinameid.md)
  
[SMAPIFormPropEnumVal](smapiformpropenumval.md)


[MAPI-Strukturen](mapi-structures.md)

