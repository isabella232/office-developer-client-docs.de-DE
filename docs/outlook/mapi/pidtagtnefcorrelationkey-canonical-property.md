---
title: PidTagTnefCorrelationKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagTnefCorrelationKey
api_type:
- COM
ms.assetid: a7f05c8c-59b4-4d5b-8e70-ebcde5f2ed45
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d086dda301bf527f42279d50be2f15f26f3213a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599298"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a>PidTagTnefCorrelationKey (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Wert, der eine TNEF-Anlage (Transport Neutral Encapsulation Format) mit einer Nachricht korreliert.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_TNEF_CORRELATION_KEY  <br/> |
|Kennung:  <br/> |0x007F  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Umschlag  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Es wird empfohlen, dass TNEF-Anlagenunterobjekte diese Eigenschaft verfügbar machen. Diese Eigenschaft bestimmt, ob eine eingehende TNEF-Datei zu der Nachricht gehört, an die sie angefügt ist. Es wird in erster Linie von Transportanbietern und Gateways verwendet.
  
Bei einer ausgehenden Nachricht sollte der Transportanbieter einen für diese Nachricht eindeutigen binären Wert berechnen oder einen vorhandenen Wert verwenden, der die Eindeutigkeitsanforderung erfüllt, z. B. einen Nachrichtenbezeichner. Der Transportanbieter sollte diesen Wert in dieser Eigenschaft speichern und dann die [ITnef::AddProps-Methode](itnef-addprops.md) aufrufen, um ihn zu kapseln. Derselbe Wert sollte auch im Transportumschlag an einem vom Anbieter definierten Ort gespeichert werden, z. B. der Nachrichtenkopf. 
  
Bei einer eingehenden Nachricht sollte der Transportanbieter die [ITnef::ExtractProps-Methode](itnef-extractprops.md) aufrufen, um die TNEF-Anlage zu kapseln und diese Eigenschaft dann mit dem im Transportumschlag gespeicherten Wert zu vergleichen. Wenn die Werte übereinstimmen, sollte TNEF normal verarbeitet werden, d. h., alle aus der TNEF-Anlage extrahierten Eigenschaften sollten verwendet werden. Wenn die Werte nicht übereinstimmen, sollten alle Eigenschaften aus der TNEF-Anlage ignoriert werden. Wenn diese Eigenschaft nicht festgelegt ist, sollte die TNEF-Datei als zu dieser Nachricht gehörend betrachtet werden, und die anderen daraus extrahierten Eigenschaften sollten verwendet werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und decodiert Nachrichten- und Anlagenobjekte in einer effizienten Datenstromdarstellung.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

