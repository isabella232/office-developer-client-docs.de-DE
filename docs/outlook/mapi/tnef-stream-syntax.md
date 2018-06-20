---
title: Die Syntax der TNEF-Stream-Objekt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cbaf37415608dd1d79a06be65b34632f2b4afc89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795756"
---
# <a name="tnef-stream-syntax"></a>Die Syntax der TNEF-Stream-Objekt

  
  
**Betrifft**: Outlook 
  
In diesem Thema wird ein Bakus-Nauer wie Beschreibung der Syntax der TNEF-Stream. In dieser Beschreibung werden nicht terminale Elemente, die eine weitere Definition kursiv angezeigt. Konstanten und Literale Elemente sind fett dargestellt. Sequences-Elemente sind in der Reihenfolge, in einer separaten Zeile aufgeführt. Das _Stream_ -Element umfasst beispielsweise die Konstante **TNEF_SIGNATURE**, gefolgt von einem _Schlüssel_, gefolgt von einem _Objekt_. Wenn ein Element mehr als eine mögliche Implementierung aufweist, werden die alternativen in aufeinander folgenden Zeilen aufgeführt. Ein _Objekt_ kann beispielsweise eine _Message_Seq_, eine _Message_Seq_ gefolgt von einer _Attach_Seq_oder nur ein _Attach_Seq_bestehen.
  
 _TNEF_Stream:_
  
> **TNEF_SIGNATURE** _Schlüssel_ _Objekt_
    
 _Wichtige Punkte:_
  
> eine ungleich NULL 16-Bit-Ganzzahl ohne Vorzeichen
    
TNEF aktiviert Transporten Generieren dieser Wert vor der Verwendung von TNEF-Implementierung zum Generieren der TNEF-Stream.
  
 _Objekt:_
  
>  _Message_Seq Message_Seq Attach_Seq Attach_Seq_
    
 _Message_Seq:_
  
>  _AttTnefVersion AttTnefVersion Msg_Attribute_Seq AttTnefVersion AttMessageClass AttTnefVersion AttMessageClass Msg_Attribute_Seq AttMessageClass AttMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_
    
 _AttTnefVersion:_
  
> **LVL_MESSAGE AttTnefVersion sizeof(ULONG)** **0 x 00010000** Prüfsumme 
    
 _AttMessageClass:_
  
> **LVL_MESSAGE attMessageClass** _Msg_class_length Msg_class_ Prüfsumme 
    
 _Msg_Attribute_Seq:_
  
>  _Msg_Attribute Msg_Attribute Msg_Attribute_Seq_
    
 _Msg_Attribute:_
  
> **LVL_MESSAGE** Attribut-ID-Attribut Länge Attributdaten Prüfsumme 
    
Attribut-ID ist eine der TNEF-Attribut Bezeichner, wie beispielsweise **AttSubject**. Attribut Länge hat die Länge der Attributdaten in Bytes. Attributdaten ist das Attribut zugeordneten Daten.
  
 _Attach_Seq:_
  
>  _AttRenddata AttRenddata Att_Attribute_Seq_
    
 _AttRenddata:_
  
> **LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA)** Renddata Prüfsumme 
    
Renddata ist die zugehörigen Daten für die **RENDDATA** -Struktur, die Renderinginformationen für die entsprechende Anlage enthält. Die Struktur **RENDDATA** ist in die TNEF definiert. H-Headerdatei. 
  
 _Att_Attribute_Seq:_
  
>  _Att_Attribute Att_Attribute Att_Attribute_Seq_
    
 _Att_Attribute:_
  
> **LVL_ATTACHMENT** Attribut-ID-Attribut Länge Attributdaten Prüfsumme 
    
Attribut-ID-Attribut Länge und Attributdaten haben die dieselbe Bedeutung wie für das Msg_Attribute-Element.
  

