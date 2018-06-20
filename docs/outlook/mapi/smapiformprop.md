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
ms.openlocfilehash: 73475c5ee4e715796e06642756c05746b271d128
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795569"
---
# <a name="smapiformprop"></a>SMAPIFormProp

  
  
**Betrifft**: Outlook 
  
Beschreibt eine benannte Eigenschaft mit einem Formular verwendet. 
  
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

## <a name="members"></a>Members

 **ulFlags**
  
> Kennzeichen, die das Format der Zeichenfolgen in der Struktur **SMAPIFormProp** zu unterscheiden. Das folgende Flag kann festgelegt werden: 
    
PARAMETER MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen sind im Unicode-Format. Wenn der Parameter MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
 **nPropType**
  
> Typ der benannten Eigenschaft, mit dem wichtigste Wort auf 0 (null) festgelegt. 
    
 **nmid**
  
> Der Name für die benannte Eigenschaft, die enthält eine **GUID** -Struktur, identifiziert der Eigenschaftswert festlegen und einem numerischen oder Zeichenfolge, die ein Schnittstellennamen-ID und das Formular darstellt. 
    
 **pszDisplayName**
  
> Zeiger auf den Anzeigenamen der benannten Eigenschaft.
    
 **nSpecialType**
  
> Wert, der den Typ der Daten enthalten im **u** -Member beschreibt. Mögliche Werte sind wie folgt: 
    
FPST_VANILLA 
  
> Das **u** -Element enthält eine Enumeration nicht. 
    
FPST_ENUM_PROP 
  
> Das **u** -Element enthält eine Struktur, die eine Enumeration beschreibt. 
    
 **u**
  
> Union, die die Zuordnung zwischen den Namen und die Anzahl der benannten Eigenschaft beschreibt. Einige Eigenschaften verwenden, ist der Member **u** leer. Mit anderen Eigenschaften wird in einer Struktur bestehend aus der folgenden Elemente dargestellt: 
    
 **nmidIdx**
  
> Die [MAPINAMEID](mapinameid.md) -Struktur, die den Eigenschaftensatz und Bezeichner für die benannte Eigenschaft enthält. 
    
 **cfpevAvailable**
  
> Anzahl der [SMAPIFormPropEnumVal](smapiformpropenumval.md) Strukturen im Array auf der Member **PfpevAvailable** zeigt. 
    
 **pfpevAvailable**
  
> Zeiger auf ein Array von **SMAPIFormPropEnumVal** -Strukturen, von denen jeder einen Wert für die benannte Eigenschaft enthält. 
    
## <a name="remarks"></a>Hinweise

Die **SMAPIFormProp** -Datenstruktur enthält Informationen zu einer Formulareigenschaft als Teil der Definitionen der [IMAPIFormInfo](imapiforminfoimapiprop.md) Schnittstelle verwendet; **nSpecialType** enthält einen Tag, der für die Vereinigung **u** gilt, die Teil der **SMAPIFormProp**ist.
  
## <a name="see-also"></a>Siehe auch



[MAPINAMEID](mapinameid.md)
  
[SMAPIFormPropEnumVal](smapiformpropenumval.md)


[MAPI-Strukturen](mapi-structures.md)

