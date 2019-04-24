---
title: Kanonische Pidtagtnefcorrelationkey (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefCorrelationKey
api_type:
- COM
ms.assetid: a7f05c8c-59b4-4d5b-8e70-ebcde5f2ed45
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e38cf93523c14d2d58c48e24a79249674298b4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341951"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a>Kanonische Pidtagtnefcorrelationkey (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Wert, der eine TNEF-Anlage (Transport Neutral Encapsulation Format) mit einer Nachricht korreliert.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_TNEF_CORRELATION_KEY  <br/> |
|Kennung:  <br/> |0x007F  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Umschlag  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Es wird empfohlen, dass die TNEF-Anlagen-unter Objekte diese Eigenschaft verfügbar machen. Diese Eigenschaft bestimmt, ob eine eingehende TNEF-Datei zu der Nachricht gehört, mit der Sie verbunden ist. Sie wird hauptsächlich von Transportanbietern und Gateways verwendet.
  
Bei einer ausgehenden Nachricht sollte der Transportanbieter einen für diese Nachricht eindeutigen Binärwert berechnen oder einen vorhandenen Wert verwenden, der der Eindeutigkeitsanforderung entspricht, wie beispielsweise einem Nachrichtenbezeichner. Der Transportanbieter sollte diesen Wert in dieser Eigenschaft speichern und dann die [ITnef::](itnef-addprops.md) AddProps-Methode aufrufen, um Sie zu kapseln. Derselbe Wert sollte auch im Transport Umschlag an einem vom Anbieter definierten Ort wie dem Nachrichtenkopf gespeichert werden. 
  
Bei einer eingehenden Nachricht sollte der Transportanbieter die [ITnef:: ExtractProps](itnef-extractprops.md) -Methode aufrufen, um die TNEF-Anlage zu decapsulate, und diese Eigenschaft dann mit dem im Transport Umschlag gespeicherten Wert vergleichen. Wenn die Werte übereinstimmen, sollte TNEF normal verarbeitet werden, das heißt, alle aus der TNEF-Anlage extrahierten Eigenschaften sollten verwendet werden. Wenn die Werte nicht übereinstimmen, sollten alle Eigenschaften aus der TNEF-Anlage ignoriert werden. Wenn diese Eigenschaft nicht festgelegt ist, sollte die TNEF-Datei als zu dieser Nachricht gehören, und die anderen Eigenschaften, die daraus extrahiert werden verwendet werden. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Ablauf für die Datenübertragung zwischen einem Client und einem Server.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und dekodiert Message-und Attachment-Objekte in einer effizienten Datenstrom Darstellung.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

