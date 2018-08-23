---
title: STnefProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblem
api_type:
- COM
ms.assetid: 3fe651b7-0ddf-42fd-8277-9224505be1a8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 90829f8fff530d22a7dee68dc227655064147cee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575329"
---
# <a name="stnefproblem"></a>STnefProblem

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält Informationen zu einer Eigenschaft oder eines Attributs Verarbeitungsproblem, das in die Codierung oder Decodierung eines Streams Transport Neutral Encapsulation Format (TNEF) aufgetreten sind.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |TNEF.h  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a>Elemente

 **ulComponent**
  
> Der Typ der Verarbeitung während der das Problem aufgetreten ist. Wenn während der Verarbeitung das Problem aufgetreten ist, wird das Element **UlComponent** auf NULL gesetzt. Wenn während der Verarbeitung von Anlagen das Problem aufgetreten ist, wird die **UlComponent** auf die entsprechende Anlage **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) Wert festgelegt.
    
 **ulAttribute**
  
> Attribut der Eigenschaft zugeordneten angegeben durch die **UlPropTag** Mitglied oder, wenn das TNEF Verarbeitungsproblem tritt auf, wenn eine Kapselung Decodierung zu blockieren, einen der folgenden Werte: 
    
 _attMAPIProps_
  
> Nachrichtenebene
    
 _attAttachment_
  
> Anlage-Ebene
    
 **ulPropTag**
  
> Eigenschaftentag der Eigenschaft, die Ursache für das Problem der TNEF-Verarbeitung, außer wenn das Problem auftritt, wenn einen Block Encapsulation Decodierung in dem Groß-/Kleinschreibung **UlPropTag** auf 0 (null) festgelegt ist. 
    
 **SCODE**
  
> Fehler-Wert zurück, der das Problem aufgetreten ist, während der Verarbeitung angibt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn eine Struktur **STnefProblem** während der Verarbeitung eines Attribut oder Eigenschaft nicht generiert wird, kann die Anwendung unter der Annahme fortgesetzt, die die Verarbeitung dieses Attribut oder Eigenschaft erfolgreich waren. Die einzige Ausnahme tritt auf, wenn das Problem aufgetreten ist, während der Decodierung eines Blocks Kapselung. In diesem Fall die Decodierung der die entsprechende Komponente für den Block wird angehalten und der Decodierung in einer anderen Komponente fortgesetzt wird. 
  
## <a name="see-also"></a>Siehe auch



[STnefProblemArray](stnefproblemarray.md)
  
[PidTagAttachNumber (kanonische Eigenschaft)](pidtagattachnumber-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

