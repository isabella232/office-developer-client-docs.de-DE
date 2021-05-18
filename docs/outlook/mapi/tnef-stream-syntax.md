---
title: '#A0'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 12d2a92ff80897456707c7ab8af8f704605c85d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423027"
---
# <a name="tnef-stream-syntax"></a>#A0

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema wird eine Bakus-Nauer beschreibung der TNEF-Streamsyntax beschrieben. In dieser Beschreibung sind nicht terminale Elemente, die eine weitere Definition haben, italisch. Konstanten und Literalelemente sind fett formatiert. Sequenzen von Elementen werden in der Reihenfolge einer einzelnen Zeile aufgelistet. Das _Stream-Element_ besteht z. B. aus der TNEF_SIGNATURE **,** gefolgt von einem _Key_-Element, gefolgt von einem _Object -Element._ Wenn ein Element über mehrere mögliche Implementierungen verfügt, werden die Alternativen in aufeinander folgenden Zeilen aufgelistet. Ein Objekt  kann z. B. aus einer  Message_Seq _,_ einer Message_Seq gefolgt von einer Attach_Seq _oder_ einfach einer Attach_Seq _._
  
 _TNEF_Stream:_
  
> **TNEF_SIGNATURE** _Key-Objekt_ 
    
 _Schlüssel:_
  
> eine nicht signierte 16-Bit-Ganzzahl ungleich 16 Bit
    
TNEF-aktivierte Transporte generieren diesen Wert, bevor die TNEF-Implementierung zum Generieren eines TNEF-Datenstroms verwendet wird.
  
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
  
> **LVL_MESSAGE** attribut-ID attribut-length attribut-data checksum 
    
Attribut-ID ist eine der TNEF-Attributbezeichner, z. B. **attSubject**. Attributlänge ist die Länge in Bytes der Attributdaten. Attributdaten sind die Daten, die dem Attribut zugeordnet sind.
  
 _Attach_Seq:_
  
>  _attRenddata attRenddata Att_Attribute_Seq_
    
 _attRenddata:_
  
> **LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA)** renddata checksum 
    
Renddata sind die Der **RENDDATA-Struktur** zugeordneten Daten, die die Renderinginformationen für die entsprechende Anlage enthalten. Die **RENDDATA-Struktur** ist im TNEF definiert. H-Headerdatei. 
  
 _Att_Attribute_Seq:_
  
>  _Att_Attribute Att_Attribute Att_Attribute_Seq_
    
 _Att_Attribute:_
  
> **LVL_ATTACHMENT** attribut-ID attribut-length attribut-data checksum 
    
Attribut-ID, Attributlänge und Attributdaten haben die gleichen Bedeutungen wie für das Msg_Attribute Element.
  

