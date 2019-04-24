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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 968f9e1dad3a233b31f0ce29d3ce935b1257948c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309499"
---
# <a name="smapiformprop"></a>SMAPIFormProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine benannte Eigenschaft, die mit einem Formular verwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform. h  <br/> |
   
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
  
> Flags, mit denen das Format der Zeichenfolgen in der **SMAPIFormProp** -Struktur unterschieden wird. Das folgende Flag kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen sind im Unicode-Format. Wenn MAPI_UNICODE nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    
 **nPropType**
  
> Typ der benannten Eigenschaft, wobei das bedeutendste Wort auf NULL festgelegt ist. 
    
 **nmid**
  
> Name für die benannte Eigenschaft, die eine **GUID** -Struktur enthält, die den Eigenschaftensatz identifiziert, und entweder einen numerischen oder einen String-Wert, der eine Schnittstellen-ID und einen Formularnamen darstellt. 
    
 **pszDisplayName**
  
> Zeiger auf den Anzeigenamen der benannten Eigenschaft.
    
 **nSpecialType**
  
> Wert, der den Typ der im **u** -Element enthaltenen Daten beschreibt. Folgende Werte sind möglich: 
    
FPST_VANILLA 
  
> Der **u** -Member enthält keine Enumeration. 
    
FPST_ENUM_PROP 
  
> Das **u** -Element enthält eine Struktur, die eine Enumeration beschreibt. 
    
 **u**
  
> Union, die die Zuordnung zwischen dem Namen und der Nummer der benannten Eigenschaft beschreibt. Bei Verwendung einiger Eigenschaften ist das **u** -Element leer. Mit anderen Eigenschaften wird es in einer Struktur dargestellt, die aus den folgenden Elementen besteht: 
    
 **nmidIdx**
  
> Die [MAPINAMEID](mapinameid.md) -Struktur, die den Eigenschaftensatz und Bezeichner für die benannte Eigenschaft enthält. 
    
 **cfpevAvailable**
  
> Die Anzahl der [SMAPIFormPropEnumVal](smapiformpropenumval.md) -Strukturen im Array, auf die vom **pfpevAvailable** -Element verwiesen wird. 
    
 **pfpevAvailable**
  
> Zeiger auf ein Array von **SMAPIFormPropEnumVal** -Strukturen, die jeweils einen Wert für die benannte Eigenschaft enthält. 
    
## <a name="remarks"></a>Bemerkungen

Die **SMAPIFormProp** -Struktur enthält Informationen zu einer Formulareigenschaft, die als Teil der Definitionen der [IMAPIFormInfo](imapiforminfoimapiprop.md) -Schnittstelle verwendet wird. **nSpecialType** enthält ein Tag, das für die **u** -Union gilt, die Teil von **SMAPIFormProp**ist.
  
## <a name="see-also"></a>Siehe auch



[MAPINAMEID](mapinameid.md)
  
[SMAPIFormPropEnumVal](smapiformpropenumval.md)


[MAPI-Strukturen](mapi-structures.md)

