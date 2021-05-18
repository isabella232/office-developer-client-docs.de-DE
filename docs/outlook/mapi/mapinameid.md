---
title: MAPINAMEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPINAMEID
api_type:
- COM
ms.assetid: 9a92e9cd-8282-4cf0-93af-4089b3763594
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: baec750a460b3ba9becd2e1dddf967705424ac4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411680"
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

## <a name="members"></a>Elemente

 **lpguid**
  
> Zeiger auf eine [GUID-Struktur,](guid.md) die einen bestimmten Eigenschaftensatz definiert; Dieses Element darf nicht NULL sein. Folgende Werte sind gültig: 
    
PS_PUBLIC_STRINGS
  
> 
    
PS_MAPI
  
> 
    
Ein clientdefinierter Wert
  
> 
    
 **ulKind**
  
> Wert, der den Typ des Werts im **Element Kind** beschreibt. Folgende Werte sind gültig: 
    
MNID_ID 
  
> Das **Element Kind** enthält einen ganzzahligen Wert, der den Eigenschaftennamen darstellt. 
    
MNID_STRING 
  
> Das **Kind-Element** enthält eine Unicode-Zeichenzeichenfolge, die den Eigenschaftennamen darstellt. 
    
 **Kind**
  
> Union, die den Namen der benannten Eigenschaft beschreibt. Der Name kann entweder ein ganzzahliger Wert sein, der in **lID** gespeichert ist, oder eine Unicode-Zeichenzeichenfolge, die in **lpwstrName gespeichert ist.**
    
## <a name="remarks"></a>Hinweise

Die **MAPINAMEID-Struktur** wird verwendet, um benannte Eigenschaften zu beschreiben, die bezeichner über 0x8000. Ein Eigenschaftensatz ist ein wichtiger Teil einer benannten Eigenschaft. Beispielsweise sind PS_PUBLIC_STRINGS oder PS_ROUTING_ADDRTYPE von MAPI definierte Eigenschaftssätze. 
  
Mit benannten Eigenschaften können Clients benutzerdefinierte Eigenschaften in einem größeren Namespace definieren, als im MAPI-definierten Eigenschaftenbezeichnerbereich verfügbar ist. Eigenschaftsnamen können nicht direkt zum Abrufen von Eigenschaftswerten verwendet werden. Sie müssen zunächst eigenschaftenbezeichnern über die [IMAPIProp::GetIDsFromNames-Methode zugeordnet](imapiprop-getidsfromnames.md) werden. Für bestimmte Objekte wie Nachrichten reserviert MAPI einen Bereich von Eigenschaftenbezeichnern für benutzerdefinierte Eigenschaften. Daher müssen Clients für diese Objekte keine benannten Eigenschaften verwenden und können den damit verbundenen Aufwand sparen. 
  
Weitere Informationen zu benannten Eigenschaften finden Sie unter [Named Properties](mapi-named-properties.md).
  
## <a name="see-also"></a>Siehe auch



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)


[MAPI-Strukturen](mapi-structures.md)

