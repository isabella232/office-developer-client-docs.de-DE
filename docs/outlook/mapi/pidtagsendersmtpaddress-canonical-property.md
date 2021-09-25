---
title: PidTagSenderSmtpAddress (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 321cde5a-05db-498b-a9b8-cb54c8a14e34
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 43600035e8fa7b003e43ba8cc22b3f9b510f6662
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609775"
---
# <a name="pidtagsendersmtpaddress-canonical-property"></a>PidTagSenderSmtpAddress (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält das Format der SMTP-E-Mail-Adresse (Simple Mail Transport Protocol) des Besitzers des sendenden Postfachs.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SENDER_SMTP_ADDRESS, PR_SENDER_SMTP_ADDRESS_A, PR_SENDER_SMTP_ADDRESS_W  <br/> |
|Kennung:  <br/> |0x5D01  <br/> |
|Datentyp:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Bereich:  <br/> |Adresse  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft ist ein Beispiel für die Adresseigenschaften des Nachrichtensenders. Sie muss vom ausgehenden Transportanbieter festgelegt werden, der zuvor vorhandene Werte niemals übertragen sollte.
  
Wenn kein Transportanbieter Absenderadresseigenschaften angegeben hat, versucht der MAPI-Spooler, diese auszufüllen, indem er die [IMAPISession::QueryIdentity-Methode](imapisession-queryidentity.md) für einen Eintragsbezeichner aufruft. Wenn keine Eintragsbezeichner angegeben wurden, speichert der MAPI-Spooler "Unknown" in allen Absenderadresseigenschaften des Typs PT_UNICODE oder PT_STRING8. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Microsoft Exchange Server Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.
    
[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Post-Objekte zulässig sind.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakt- und persönliche Verteilerlistenobjekte zulässig sind.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und decodiert Nachrichten- und Anlagenobjekte in einer effizienten Datenstromdarstellung.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

