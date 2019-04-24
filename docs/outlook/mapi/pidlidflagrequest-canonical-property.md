---
title: Kanonische Pidlidflagrequest (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagRequest
api_type:
- COM
ms.assetid: 38981f07-14b8-47c2-93df-e6aed91896e4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ddcf32df716fe2b0a02655278ff0cd8d821de1f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357806"
---
# <a name="pidlidflagrequest-canonical-property"></a>Kanonische Pidlidflagrequest (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt den Status einer Besprechungsanfrage dar.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidRequest  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long-ID (Deckel):  <br/> |0x00008530  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Kennzeichnen  <br/> |
   
## <a name="remarks"></a>Bemerkungen

In Microsoft Office Outlook ist eine Besprechungsanfrage ein Terminelement.
  
Diese Eigenschaft enthält benutzerspezifischen Text, der dem Flag zugeordnet werden soll, und sollte festgelegt werden, wenn das Nachrichtenobjekt gekennzeichnet oder abgeschlossen ist, aber für ein Besprechungs bezogenes Objekt nicht vorhanden sein sollte. Clients können diese Eigenschaft nicht unterstützen und immer "Follow up" (gegebenenfalls in die Sprache des Benutzers übersetzt) als Wert der Zeichenfolge schreiben, wenn diese Eigenschaft festgelegt werden soll. Diese Eigenschaft sollte basierend auf den Werten der Eigenschaften **dispidFlagStringEnum** ([Pidlidflagstring (](pidlidflagstring-canonical-property.md)) und **dispidValidFlagStringProof** ([pidlidvalidflagstringproof (](pidlidvalidflagstringproof-canonical-property.md)) bedingungslos ignoriert werden.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Markierung an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

