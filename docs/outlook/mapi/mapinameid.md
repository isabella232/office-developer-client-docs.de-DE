---
title: MAPINAMEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MAPINAMEID
api_type:
- COM
ms.assetid: 9a92e9cd-8282-4cf0-93af-4089b3763594
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 68dbae7a6d2e7cc458b3b7ed71ddd06bab7fb1f8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584093"
---
# <a name="mapinameid"></a>MAPINAMEID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine benannte Eigenschaft. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _MAPINAMEID
{
  LPGUID lpguid;
  ULONG ulKind;
  union
  {
    LONG lID;
    LPWSTR lpwstrName;
  } Kind;
} MAPINAMEID, FAR *LPMAPINAMEID;

```

## <a name="members"></a>Members

 **lpguid**
  
> Zeiger auf eine [GUID-Struktur,](guid.md) die einen bestimmten Eigenschaftensatz definiert; dieser Member darf nicht NULL sein. Folgende Werte sind gültig: 
    
PS_PUBLIC_STRINGS
  
> 
    
PS_MAPI
  
> 
    
Ein clientdefinierter Wert
  
> 
    
 **ulKind**
  
> Wert, der den Typ des Werts im **Kind-Element** beschreibt. Folgende Werte sind gültig: 
    
MNID_ID 
  
> Das **Kind-Element** enthält einen ganzzahligen Wert, der den Eigenschaftsnamen darstellt. 
    
MNID_STRING 
  
> Das **Kind-Element** enthält eine Unicode-Zeichenfolge, die den Eigenschaftennamen darstellt. 
    
 **Kind**
  
> Union, die den Namen der benannten Eigenschaft beschreibt. Bei dem Namen kann es sich um einen ganzzahligen Wert handeln, der in **lID** gespeichert ist, oder um eine Unicode-Zeichenfolge, die in **lpwstrName** gespeichert ist.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **MAPINAMEID-Struktur** wird verwendet, um benannte Eigenschafteneigenschaften mit Bezeichnern über 0x8000 zu beschreiben. Ein Eigenschaftensatz ist ein wichtiger Teil einer benannten Eigenschaft. Beispielsweise sind PS_PUBLIC_STRINGS oder PS_ROUTING_ADDRTYPE von MAPI definierte Eigenschaftensätze. 
  
Mit benannten Eigenschaften können Clients benutzerdefinierte Eigenschaften in einem größeren Namespace definieren, als im MAPI-definierten Eigenschaftenbezeichnerbereich verfügbar ist. Eigenschaftsnamen können nicht verwendet werden, um Eigenschaftswerte direkt abzurufen; Sie müssen zuerst über die [IMAPIProp::GetIDsFromNames-Methode](imapiprop-getidsfromnames.md) Eigenschaftsbezeichnern zugeordnet werden. Für bestimmte Objekte wie Nachrichten reserviert MAPI einen Bereich von Eigenschaftsbezeichnern für benutzerdefinierte Eigenschaften. Daher müssen Clients für diese Objekte keine benannten Eigenschaften verwenden und können den damit verbundenen Overhead sparen. 
  
Weitere Informationen zu benannten Eigenschaften finden Sie unter ["Benannte Eigenschaften".](mapi-named-properties.md)
  
## <a name="see-also"></a>Siehe auch



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)


[MAPI-Strukturen](mapi-structures.md)

