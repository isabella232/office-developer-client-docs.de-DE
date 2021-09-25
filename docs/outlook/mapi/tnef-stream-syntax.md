---
title: TNEF-Streamsyntax
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 841404f5f7cb13fadd964f13174dc25c493e0015
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609327"
---
# <a name="tnef-stream-syntax"></a>TNEF-Streamsyntax

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema wird eine Bakus-Nauer wie die Beschreibung der TNEF-Datenstromsyntax vorgestellt. In dieser Beschreibung sind nicht terminale Elemente, die eine weitere Definition haben, kursiv formatierend. Konstanten und Literalelemente sind fett formatiert. Sequenzen von Elementen werden in einer einzelnen Zeile in der angegebenen Reihenfolge aufgelistet. Beispielsweise besteht das  _Stream_ -Element aus der Konstante **TNEF_SIGNATURE**, gefolgt von einem  _Schlüssel_, gefolgt von einem  _Objekt_. Wenn ein Element mehrere mögliche Implementierungen aufweist, werden die Alternativen in aufeinander folgenden Zeilen aufgeführt. Ein  _Objekt_ kann z. B. aus einem  _Message_Seq,_ einem  _Message_Seq_ gefolgt von einem  _Attach_Seq_ oder nur aus einem  _Attach_Seq_ bestehen.
  
 _TNEF_Stream:_
  
> **TNEF_SIGNATURE** _Key-Objekt_ 
    
 _Schlüssel:_
  
> Eine 16-Bit-Ganzzahl ohne Vorzeichen ungleich Null
    
TNEF-aktivierte Transporte generieren diesen Wert, bevor die TNEF-Implementierung zum Generieren eines TNEF-Streams verwendet wird.
  
 _Objekt:_
  
>  _Message_Seq Message_Seq Attach_Seq Attach_Seq_
    
 _Message_Seq:_
  
>  _attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_
    
 _attTnefVersion:_
  
> **LVL_MESSAGE attTnefVersion sizeof(ULONG)** **0x00010000** Prüfsumme 
    
 _attMessageClass:_
  
> **LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ Prüfsumme 
    
 _Msg_Attribute_Seq:_
  
>  _Msg_Attribute Msg_Attribute Msg_Attribute_Seq_
    
 _Msg_Attribute:_
  
> **LVL_MESSAGE** Attribut-ID-Attributlängenattribut-Datenprüfsumme 
    
Attribut-ID ist einer der TNEF-Attributbezeichner, z. B. **attSubject**. Die Attributlänge ist die Länge der Attributdaten in Byte. Attributdaten sind die dem Attribut zugeordneten Daten.
  
 _Attach_Seq:_
  
>  _attRenddata attRenddata Att_Attribute_Seq_
    
 _attRenddata:_
  
> **LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA) renddata** checksum 
    
"Renddata" sind die Daten, die der **RENDDATA-Struktur** zugeordnet sind und die Renderinginformationen für die entsprechende Anlage enthalten. Die **RENDDATA-Struktur** ist im TNEF definiert. H-Headerdatei. 
  
 _Att_Attribute_Seq:_
  
>  _Att_Attribute Att_Attribute Att_Attribute_Seq_
    
 _Att_Attribute:_
  
> **LVL_ATTACHMENT** Attribut-ID-Attributlängenattribut-Datenprüfsumme 
    
Attribut-ID, Attributlänge und Attributdaten haben die gleiche Bedeutung wie für das Msg_Attribute Element.
  

