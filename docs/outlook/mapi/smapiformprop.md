---
title: SMAPIFormProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SMAPIFormProp
api_type:
- COM
ms.assetid: 80f1c2e0-3567-4b16-86cb-d5e6ac95c2ee
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 69bf149f4d70c34212ecea4c0ea4c55f25d0fc2a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578592"
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
  
> Kennzeichen, die verwendet werden, um das Format der Zeichenfolgen in der **SMAPIFormProp-Struktur** zu unterscheiden. Das folgende Kennzeichen kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen sind im Unicode-Format. Wenn MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
 **nPropType**
  
> Typ der benannten Eigenschaft, wobei das wichtigste Wort auf Null festgelegt ist. 
    
 **nmid**
  
> Name für die benannte Eigenschaft, die eine **GUID-Struktur** enthält, die den Eigenschaftensatz identifiziert, sowie einen numerischen oder Zeichenfolgenwert, der einen Schnittstellenbezeichner und formularnamen darstellt. 
    
 **pszDisplayName**
  
> Zeiger auf den Anzeigenamen der benannten Eigenschaft.
    
 **nSpecialType**
  
> Wert, der den Im **u-Member** enthaltenen Datentyp beschreibt. Mögliche Werte sind: 
    
FPST_VANILLA 
  
> Das **u-Element** enthält keine Enumeration. 
    
FPST_ENUM_PROP 
  
> Das **u-Element** enthält eine Struktur, die eine Enumeration beschreibt. 
    
 **u**
  
> Union, die die Zuordnung zwischen dem Namen und der Nummer der benannten Eigenschaft beschreibt. Bei Verwendung einiger Eigenschaften ist das **u-Element** leer. Bei anderen Eigenschaften wird sie in einer Struktur dargestellt, die aus den folgenden Elementen besteht: 
    
 **nmidIdx**
  
> Die [MAPINAMEID-Struktur,](mapinameid.md) die den Eigenschaftensatz und den Bezeichner für die benannte Eigenschaft enthält. 
    
 **cfpevAvailable**
  
> Die Anzahl der [SMAPIFormPropEnumVal-Strukturen](smapiformpropenumval.md) im Array, auf das der **pfpevAvailable-Member** verweist. 
    
 **pfpevAvailable**
  
> Zeiger auf ein Array von **SMAPIFormPropEnumVal-Strukturen,** die jeweils einen Wert für die benannte Eigenschaft enthalten. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **SMAPIFormProp-Struktur** enthält Informationen zu einer Formulareigenschaft, die als Teil der Definitionen der [IMAPIFormInfo-Schnittstelle](imapiforminfoimapiprop.md) verwendet wird. **nSpecialType** enthält ein Tag, das für die **U-Union** gilt, die Teil von **SMAPIFormProp** ist.
  
## <a name="see-also"></a>Siehe auch



[MAPINAMEID](mapinameid.md)
  
[SMAPIFormPropEnumVal](smapiformpropenumval.md)


[MAPI-Strukturen](mapi-structures.md)

