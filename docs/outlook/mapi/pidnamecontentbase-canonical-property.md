---
title: PidNameContentBase (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentBase
api_type:
- COM
ms.assetid: ab197ace-6e7d-4ec5-9f6d-4a63a1eda11c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 21469b944bb2ce5db0576e40012335d89d48cb49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793982"
---
# <a name="pidnamecontentbase-canonical-property"></a>PidNameContentBase (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Einen Wert für [RFC3282] Content-Base Kopfzeile Feld enthält.
  
|||
|:-----|:-----|
|Anzeigenamen:  <br/> |BodyContentBase  <br/> |
|-Eigenschaft festgelegt:  <br/> |PS_INTERNET_HEADERS  <br/> |
|Name der Eigenschaft:  <br/> |Content-Base  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |E-Mail  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Um den Wert dieser Eigenschaft festzulegen, müssen Multipurpose Internet Message Extensions (MIME) Clients den gewünschten Wert in ein Kopfzeilenfeld Content-Base auf eine Entität MIME geschrieben werden, die Textkörper einer Nachricht zugeordnet ist. MIME-Leser müssen auf den Wert dieser Eigenschaft den Wert eines Felds Header Content-Base für solche eine MIME-Entität kopieren.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

