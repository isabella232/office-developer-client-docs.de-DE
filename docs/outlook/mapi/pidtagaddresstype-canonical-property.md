---
title: PidTagAddressType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressType
api_type:
- HeaderDef
ms.assetid: 986719d2-8837-46b4-8d04-c24508f5e19a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6051d3403cede21fa4aebdb6ca561dd3efb46771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360085"
---
# <a name="pidtagaddresstype-canonical-property"></a>PidTagAddressType (kanonische Eigenschaft)

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den E-Mail-Adresstyp des Messagingbenutzers, z. B. SMTP.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ADDRTYPE, PR_ADDRTYPE_A, PR_ADDRTYPE_W  <br/> |
|Kennung:  <br/> |0x3002  <br/> |
|Datentyp:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Bereich:  <br/> |Adresse  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften sind Beispiele für die Basisadresseneigenschaften, die allen Messagingbenutzern gemeinsam sind. Es gibt an, welches Messagingsystem MAPI zum Verarbeiten einer bestimmten Nachricht verwendet.
  
Diese Eigenschaft bestimmt auch das Format der Adresszeichenfolge im **PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)). Die zeichenfolge, die sie enthält, kann nur die großbuchstaben alphabetischen Zeichen von A bis Z und die Zahlen von 0 bis 9 enthalten.
  
Gültige Beispiele für die Zeichenfolge sind: 
  
```cpp
FAX
MHS
PROFS
SMTP
X400

```

## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Verarbeitet die Kommunikation eines Clients mit einem NSPI-Server (Name Service Provider Interface).
    
[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)
  
> Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Gibt zulässige Vorgänge für die Zentralen Nachrichtenspeicherobjekte an.
    
[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Adressbuchvorlagen zulässig sind.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Bearbeitet eingehende E-Mail-Nachrichten auf einem Server.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge zum Bearbeiten einer Suchordnerlistenkonfiguration an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)
  
[MAPI-Adresstypen](mapi-address-types.md)

