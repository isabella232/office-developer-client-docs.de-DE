---
title: PidTagMappingSignature (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMappingSignature
api_type:
- HeaderDef
ms.assetid: a5e9f807-12a9-4bc9-a6a5-17579e747ffa
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3f3f1ca6d0160a13cab0f49b88c893c6b4647e0b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609866"
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
   
## <a name="remarks"></a>HinwBemerkungeneise

Es wird empfohlen, dass Objekte mit benannten Eigenschaften diese Eigenschaft verfügbar machen. Eine Clientanwendung sollte die **PR_MAPPING_SIGNATURE** Eigenschaft beider Objekte überprüfen, wenn benannte Eigenschaften von einem Objekt in ein anderes kopiert werden. Die Verwendung dieser Eigenschaft kann die Übersetzung zwischen den Namen und Bezeichnern der kopierten Eigenschaften minimieren. 
  
Wenn diese Eigenschaft für ein bestimmtes MAPI-Objekt nicht vorhanden ist, verfügt das Objekt über eine eigene eindeutige Zuordnung von Namen und Bezeichnern. In diesem Fall muss der Client die [IMAPIProp::GetNamesFromIDs-Methode](imapiprop-getnamesfromids.md) für das Quellobjekt und dann die [IMAPIProp::GetIDsFromNames-Methode](imapiprop-getidsfromnames.md) für das Zielobjekt aufrufen. 
  
Wenn zwei Objekte denselben **PR_MAPPING_SIGNATURE** Wert aufweisen, muss der Client den Namen nicht in einen Bezeichner und einen Bezeichner in einen Namen übersetzen. Der Client kann einfach die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) für die Quelle und dann die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) auf dem Ziel aufrufen. Dies ist praktisch für Clients, die das benutzerdefinierte Kopieren benannter Eigenschaften ausführen, und für Anbieter, die die Methoden [IMAPIProp::CopyTo](imapiprop-copyto.md) und [IMAPIProp::CopyProps](imapiprop-copyprops.md) implementieren. 
  
Weitere Informationen zu benannten Eigenschaften und zur Zuordnung von Namen und Bezeichnern finden Sie unter [MAPI Named Properties](mapi-named-properties.md). 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPINAMEID](mapinameid.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

