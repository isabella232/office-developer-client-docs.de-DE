---
title: Kanonische PidTagTnefCorrelationKey-Eigenschaft
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
ms.openlocfilehash: 5a0216616d9a35ef5ad4509bc377044c1d217d79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795256"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a>Kanonische PidTagTnefCorrelationKey-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält einen Wert, der eine Anlage Transport Neutral Encapsulation Format (TNEF) mit einer Nachricht verknüpft.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_TNEF_CORRELATION_KEY  <br/> |
|Bezeichner:  <br/> |0x007F  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Umschlag  <br/> |
   
## <a name="remarks"></a>Hinweise

Es wird empfohlen, dass TNEF-Anlage Unterobjekte diese Eigenschaft verfügbar machen. Diese Eigenschaft bestimmt, ob eine eingehende TNEF-Datei an die Nachricht gehört, für die Sie verbunden ist. Es wird hauptsächlich von Transportanbieter und Gateways verwendet.
  
Für eine ausgehende Nachricht sollte der Adressbuchhierarchie einen Binärwert für diese Nachricht eindeutig zu berechnen, oder verwenden einen vorhandenen Wert, der die Anforderung an die Eindeutigkeit, wie eine Nachricht-ID entspricht. Der Transportdienst sollte diesen Wert in dieser Eigenschaft speichern und rufen Sie dann die [ITnef::AddProps](itnef-addprops.md) -Methode, um es kapseln. Der gleiche Wert sollten auch im Umschlag Transport in einer vom Anbieter, wie der Nachrichtenkopf definierten Stelle gespeichert werden. 
  
Auf eine eingehende Nachricht sollte der Adressbuchhierarchie rufen Sie die [ITnef::ExtractProps](itnef-extractprops.md) -Methode, die die TNEF-Anlage entkapseln und vergleichen Sie diese Eigenschaft mit dem Wert in der Transport Umschlag gespeichert. Wenn die Werte übereinstimmen, TNEF normalerweise verarbeitet werden soll, d. h., alle Eigenschaften aus der TNEF-Anlage extrahiert verwendet werden soll. Wenn die Werte nicht übereinstimmen, sollte alle Eigenschaften aus der TNEF-Anlage ignoriert werden. Wenn diese Eigenschaft nicht festgelegt ist, sollte die TNEF-Datei zu dieser Nachricht gehören berücksichtigt werden, und die anderen Eigenschaften daraus extrahiert sollte verwendet werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

