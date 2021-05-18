---
title: PidTagResponseRequested (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponseRequested
api_type:
- COM
ms.assetid: e52bb48c-7107-4ac4-b030-885409759ee7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 77c724affd2057ca6347d752323c5ba0a3094ecf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330156"
---
# <a name="pidtagresponserequested-canonical-property"></a>PidTagResponseRequested (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn der Nachrichtensender eine Antwort auf eine Besprechungsanfrage erhalten möchte.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RESPONSE_REQUESTED  <br/> |
|Kennung:  <br/> |0x0063  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |MAPI-Umschlag  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird für Besprechungsanfragen verwendet. Die empfangende Clientanwendung sollte den Benutzer bitten, die Anforderung zu akzeptieren oder zu ablehnen, und diese Antwort dann an den Absender zurücksendet.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichten zulässig sind.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.
    
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

