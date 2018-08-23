---
title: SExistRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SExistRestriction
api_type:
- COM
ms.assetid: 48d5ab42-ee70-4f6e-9184-18d22b08ea1b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 218238bea277a2d57c77fcc9d71cd622f7da42fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571948"
---
# <a name="sexistrestriction"></a>SExistRestriction

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Eine vorhanden Beschränkung der verwendet wird, um zu testen, ob eine bestimmte Eigenschaft als Spalte in der Tabelle vorhanden ist beschrieben. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a>Elemente

 **ulReserved1**
  
> Reserviert. NULL muss sein. 
    
 **ulPropTag**
  
> Eigenschafts-Tag, identifiziert der Spalte auf Vorhandensein in jeder Zeile getestet werden soll.
    
 **ulReserved2**
  
> Reserviert. NULL muss sein.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Einschränkung vorhanden wird verwendet, um sinnvolle Ergebnisse für andere Arten von Einschränkungen zu gewährleisten, die Eigenschaften wie-Eigenschaft und Inhalte Einschränkungen betreffen. Wenn eine Einschränkung, die eine Eigenschaft beinhaltet [Methode IMAPITable:: Restrict](imapitable-restrict.md) oder [IMAPITable](imapitable-findrow.md) übergeben wird, und die Eigenschaft ist nicht vorhanden, sind die Ergebnisse der Einschränkung nicht definiert. Durch das Erstellen einer **und** Einschränkung, die die eigenschaftseinschränkung mit einer Einschränkung vorhanden teilnimmt, kann ein Anrufer genaue Ergebnisse garantiert werden. 
  
Vorhanden Einschränkungen können nicht verwendet werden, mit der untergeordnete Objekteigenschaften, die-Typ PT_OBJECT verfügen. 
  
Weitere Informationen zur Struktur **SExistRestriction** finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

