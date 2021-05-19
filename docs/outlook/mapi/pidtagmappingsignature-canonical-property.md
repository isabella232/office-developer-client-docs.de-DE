---
title: PidTagMappingSignature (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMappingSignature
api_type:
- HeaderDef
ms.assetid: a5e9f807-12a9-4bc9-a6a5-17579e747ffa
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d12e8510686f51698981c47327f79ef40d3ec342
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342546"
---
# <a name="pidtagmappingsignature-canonical-property"></a>PidTagMappingSignature (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Zuordnungssignatur für benannte Eigenschaften eines bestimmten MAPI-Objekts. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MAPPING_SIGNATURE  <br/> |
|Kennung:  <br/> |0x0FF8  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Sonstiges  <br/> |
   
## <a name="remarks"></a>Hinweise

Es wird empfohlen, dass Objekte mit benannten Eigenschaften diese Eigenschaft verfügbar machen. Eine Clientanwendung sollte die **PR_MAPPING_SIGNATURE** beiden Objekten überprüfen, wenn benannte Eigenschaften von einem Objekt in ein anderes kopiert werden. Die Verwendung dieser Eigenschaft kann die Übersetzung zwischen den Namen und Bezeichnern kopierter Eigenschaften minimieren. 
  
Wenn diese Eigenschaft für ein bestimmtes MAPI-Objekt nicht vorhanden ist, verfügt das Objekt über eine eigene eindeutige Zuordnung von Namen und Bezeichnern. In diesem Fall muss der Client die [IMAPIProp::GetNamesFromIDs-Methode](imapiprop-getnamesfromids.md) für das Quellobjekt und dann die [IMAPIProp::GetIDsFromNames-Methode](imapiprop-getidsfromnames.md) für das Zielobjekt aufrufen. 
  
Wenn zwei Objekte denselben PR_MAPPING_SIGNATURE **haben,** muss der Client den Namen nicht in bezeichner und bezeichner in name übersetzen. Der Client kann einfach die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) für die Quelle und dann die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) für das Ziel aufrufen. Dies ist für Clients geeignet, die benutzerdefiniertes Kopieren benannter Eigenschaften ausführen, und für Anbieter, die die [METHODEN IMAPIProp::CopyTo](imapiprop-copyto.md) und [IMAPIProp::CopyProps](imapiprop-copyprops.md) implementieren. 
  
Weitere Informationen zu benannten Eigenschaften und der Zuordnung von Namen und Bezeichnern finden Sie unter [MAPI Named Properties](mapi-named-properties.md). 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPINAMEID](mapinameid.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

