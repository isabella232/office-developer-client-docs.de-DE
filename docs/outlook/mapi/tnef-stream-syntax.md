---
title: TNEF-Datenstrom Syntax
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 12d2a92ff80897456707c7ab8af8f704605c85d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339634"
---
# <a name="tnef-stream-syntax"></a>TNEF-Datenstrom Syntax

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema stellt eine Bakus-Nauer-ähnliche Beschreibung der TNEF-Stream-Syntax dar. In dieser Beschreibung sind nicht-Terminal Elemente, die eine weitere Definition aufweisen, kursiv formatiert. Konstanten und Literale Elemente sind fett formatiert. Sequenzen von Elementen werden in einer bestimmten Reihenfolge aufgelistet. Das _Stream_ -Element besteht beispielsweise aus der Konstanten **TNEF_SIGNATURE**, gefolgt von einem _Schlüssel_und einem _Objekt_. Wenn ein Element mehr als eine mögliche Implementierung aufweist, werden die Alternativen in aufeinanderfolgenden Zeilen aufgeführt. Ein _Objekt_ kann beispielsweise aus einem _Message_Seq_, einem _Message_Seq_ gefolgt von einem _Attach_Seq_oder nur einem _Attach_Seq_bestehen.
  
 _TNEF_Stream:_
  
> **TNEF_SIGNATURE** _Schlüssel_ _Objekt_
    
 _Schlüssel_
  
> eine unsignierte 16-Bit-Ganzzahl ohne Vorzeichen
    
TNEF-aktivierte Übertragungen generieren diesen Wert, bevor Sie die TNEF-Implementierung zum Generieren eines TNEF-Streams verwenden.
  
 _Objekt_
  
>  _Message_Seq Message_Seq Attach_Seq Attach_Seq_
    
 _Message_Seq:_
  
>  _attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_
    
 _attTnefVersion:_
  
> **LVL_MESSAGE attTnefVersion sizeof (ULONG)** **0x00010000** -Prüfsumme 
    
 _attMessageClass:_
  
> **LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ -Prüfsumme 
    
 _Msg_Attribute_Seq:_
  
>  _Msg_Attribute Msg_Attribute Msg_Attribute_Seq_
    
 _Msg_Attribute:_
  
> **LVL_MESSAGE** -Attribut-ID Attribut-length-Attribut-Daten Prüfsumme 
    
Attribut-ID ist eine der TNEF-Attributbezeichner wie **attSubject**. Attribut Länge ist die Länge der Attributdaten in Byte. Attribut-Data ist die dem Attribut zugeordneten Daten.
  
 _Attach_Seq:_
  
>  _attRenddata attRenddata Att_Attribute_Seq_
    
 _attRenddata:_
  
> **LVL_ATTACHMENT attRenddata** **sizeof (RENDDATA) RENDDATA-** Prüfsumme 
    
Renddata ist die Daten, die der **Renddata** -Struktur zugeordnet sind, die die Renderinginformationen für die entsprechende Anlage enthält. Die **RENDDATA** -Struktur ist im TNEF definiert. H-Headerdatei. 
  
 _Att_Attribute_Seq:_
  
>  _Att_Attribute Att_Attribute Att_Attribute_Seq_
    
 _Att_Attribute:_
  
> **LVL_ATTACHMENT** -Attribut-ID Attribut-length-Attribut-Daten Prüfsumme 
    
Attribut-ID, Attribut Länge und Attribut-Data haben die gleichen Bedeutungen wie für das Msg_Attribute-Element.
  

