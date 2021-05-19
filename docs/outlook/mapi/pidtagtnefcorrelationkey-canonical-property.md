---
title: PidTagTnefCorrelationKey (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e38cf93523c14d2d58c48e24a79249674298b4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341951"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a>PidTagTnefCorrelationKey (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Wert, der eine Transport Neutral Encapsulation Format (TNEF)-Anlage mit einer Nachricht korreliert.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_TNEF_CORRELATION_KEY  <br/> |
|Kennung:  <br/> |0x007F  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Umschlag  <br/> |
   
## <a name="remarks"></a>Hinweise

Es wird empfohlen, dass TNEF-Anlagenunterobjekte diese Eigenschaft verfügbar machen. Diese Eigenschaft bestimmt, ob eine eingehende TNEF-Datei zu der Nachricht gehört, an die sie angefügt ist. Es wird hauptsächlich von Transportanbietern und Gateways verwendet.
  
In einer ausgehenden Nachricht sollte der Transportanbieter einen binären Wert berechnen, der für diese Nachricht eindeutig ist, oder einen vorhandenen Wert verwenden, der die Eindeutigkeitsanforderung erfüllt, z. B. eine Nachrichten-ID. Der Transportanbieter sollte diesen Wert in dieser Eigenschaft speichern und dann die [ITnef::AddProps-Methode](itnef-addprops.md) aufrufen, um ihn zu kapseln. Der gleiche Wert sollte auch im Transportumschlag an einem vom Anbieter definierten Ort gespeichert werden, z. B. im Nachrichtenkopf. 
  
Bei einer eingehenden Nachricht sollte der Transportanbieter die [ITnef::ExtractProps-Methode](itnef-extractprops.md) aufrufen, um die TNEF-Anlage zu entkapseln und diese Eigenschaft dann mit dem wert zu vergleichen, der im Transportumschlag gespeichert ist. Wenn die Werte übereinstimmen, sollte TNEF normal verarbeitet werden, d. h. alle aus der TNEF-Anlage extrahierten Eigenschaften sollten verwendet werden. Wenn die Werte nicht übereinstimmen, sollten alle Eigenschaften aus der TNEF-Anlage ignoriert werden. Wenn diese Eigenschaft nicht festgelegt ist, sollte die TNEF-Datei als Teil dieser Nachricht betrachtet werden, und die anderen aus ihr extrahierten Eigenschaften sollten verwendet werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

