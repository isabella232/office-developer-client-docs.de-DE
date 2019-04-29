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
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
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
  
> Zeiger auf eine [GUID](guid.md) -Struktur, die einen bestimmten Eigenschaftensatz definiert; Dieser Member darf nicht NULL sein. Folgende Werte sind gültig: 
    
PS_PUBLIC_STRINGS
  
> 
    
PS_MAPI
  
> 
    
Ein Client definierter Wert
  
> 
    
 **ulKind**
  
> Wert, der den Typ des Werts im **Kind** -Element beschreibt. Folgende Werte sind gültig: 
    
MNID_ID 
  
> Der Member **Kind** enthält einen ganzzahligen Wert, der den Namen der Eigenschaft darstellt. 
    
MNID_STRING 
  
> Der Member **Kind** enthält eine Unicode-Zeichenfolge, die den Namen der Eigenschaft darstellt. 
    
 **Kind**
  
> Union, die den Namen der benannten Eigenschaft beschreibt. Der Name kann ein ganzzahliger Wert sein, der im **Deckel**gespeichert ist, oder eine Unicode-Zeichenfolge, die in **lpwstrName**gespeichert ist.
    
## <a name="remarks"></a>Bemerkungen

Die **MAPINAMEID** -Struktur wird verwendet, um benannte Eigenschaften Eigenschaften mit Bezeichnern über 0X8000 zu beschreiben. Ein Eigenschaftensatz ist ein wichtiger Abschnitt einer benannten Eigenschaft. Beispielsweise sind PS_PUBLIC_STRINGS oder PS_ROUTING_ADDRTYPE Eigenschaftensätze, die von MAPI definiert werden. 
  
Mit benannten Eigenschaften können Clients benutzerdefinierte Eigenschaften in einem größeren Namespace definieren, als im MAPI-definierten Eigenschafts bezeichnerbereich verfügbar ist. Eigenschaftennamen können nicht verwendet werden, um Eigenschaftswerte direkt abzurufen; Sie müssen zunächst Eigenschaftenbezeichnern über die [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode zugeordnet werden. Für bestimmte Objekte wie Nachrichten reserviert MAPI eine Reihe von Eigenschaftenbezeichnern für benutzerdefinierte Eigenschaften. Daher müssen Clients für diese Objekte keine benannten Eigenschaften verwenden und den zugehörigen Overhead speichern. 
  
Weitere Informationen zu benannten Eigenschaften finden Sie unter [benannte Eigenschaften](mapi-named-properties.md).
  
## <a name="see-also"></a>Siehe auch



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)


[MAPI-Strukturen](mapi-structures.md)

