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
ms.openlocfilehash: f0ff4d8beb9c9d82d685630a35aefebaf7de71fc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570828"
---
# <a name="mapinameid"></a>MAPINAMEID

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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

 **x lpguid**
  
> Zeiger auf eine [GUID](guid.md) -Struktur definieren eine bestimmte Eigenschaft festgelegt. Dieser Member darf nicht NULL sein. Folgende Werte sind gültig: 
    
PS_PUBLIC_STRINGS
  
> 
    
PS_MAPI
  
> 
    
Ein Client definierten Wert
  
> 
    
 **ulKind**
  
> Wert, der den Typ von Wert in die **Kind** -Member beschreibt. Folgende Werte sind gültig: 
    
MNID_ID 
  
> Der **Kind** -Member enthält einen Integer-Wert, der Name der Eigenschaft darstellt. 
    
MNID_STRING 
  
> Der **Kind** -Member enthält eine Unicode-Zeichenfolge, die der Name der Eigenschaft darstellt. 
    
 **Kind**
  
> Beschreibung des Namens, der die benannte Eigenschaft Union. Der Name kann einen ganzzahligen Wert, der in **Abdeckung**, gespeichert oder ein Unicode-Zeichenfolge, die in **LpwstrName**gespeichert sein.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Struktur **MAPINAMEID** wird verwendet, um benannte Eigenschaften Eigenschaften zu beschreiben, die über 0 x 8000 Bezeichner aufweisen. Ein Eigenschaftensatz stellen einen wichtigen Bestandteil einer benannten Eigenschaft. Beispielsweise sind PS_PUBLIC_STRINGS oder PS_ROUTING_ADDRTYPE Eigenschaftensätze MAPI definiert. 
  
Benannte Eigenschaften ermöglichen Clients zum Definieren von benutzerdefinierter Eigenschaften in einem größeren Namespace als im Bereich Bezeichner definierte MAPI Eigenschaft verfügbar ist. Eigenschaftennamen können nicht direkt abrufen von Eigenschaftswerten verwendet werden. Sie müssen zuerst Eigenschaftenbezeichner über die [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode zugeordnet werden. Für bestimmte Objekte wie Nachrichten reserviert MAPI einen Bereich von IDs für benutzerdefinierte Eigenschaften. Aus diesem Grund für diese Objekte Clients müssen keine benannte Eigenschaften verwenden, und das zugeordnete speichern können Aufwand. 
  
Weitere Informationen zu benannten Eigenschaften finden Sie unter [Eigenschaften mit dem Namen](mapi-named-properties.md).
  
## <a name="see-also"></a>Siehe auch



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)


[MAPI-Strukturen](mapi-structures.md)

