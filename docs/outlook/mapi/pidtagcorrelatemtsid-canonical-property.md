---
title: Kanonische Pidtagcorrelatemtsid (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelateMtsid
api_type:
- HeaderDef
ms.assetid: d0fc4e91-ed90-4d27-bd23-f01e99728e2d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 96bfc184752b6a3e15434ad67ac8c2b4b26cac4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359934"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a>Kanonische Pidtagcorrelatemtsid (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den MTS-Bezeichner (Message Transfer System), der bei der Korrelation von Berichten mit gesendeten Nachrichten verwendet wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CORRELATE_MTSID  <br/> |
|Kennung:  <br/> |0x0E0D  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn ein Transportanbieter eine übermittelte Nachricht findet, deren Eigenschaft auf TRUE festgelegt ist, wird diese Eigenschaft auf den MTS-Bezeichner für diese Nachricht gesetzt. Nach der Übertragung wird diese Eigenschaft mit der Nachricht im Ordner "Gesendete Elemente" zwischenmenschlichen Nachrichten (IPM) gespeichert.
  
Messaging Systeme, die eine Korrelation durch MTS-ID, wie X. 400, unterstützen, behalten den Bezeichner als Teil des Transport Umschlags der ursprünglichen Nachricht und auch für alle als Antwort generierten Berichte bei. Wenn ein Bericht von einem solchen Messagingsystem übermittelt wird, wird diese Eigenschaft vom Transportanbieter auf den ursprünglichen MTS-Bezeichner aus dem Transport Umschlag des Berichts festgelegt. Diese Eigenschaft wird dann mit dem Bericht gespeichert.
  
Eine Clientanwendung kann einen Suchergebnisordner aller Nachrichten mit dieser Eigenschaft verwalten. Wenn ein Bericht für eine solche Nachricht eingeht, kann der Client Einschränkungen für den Ordner Suchergebnisse anwenden, die ursprüngliche Version der Nachricht suchen und die ursprünglichen Nachrichten Informationen mit den neuen Informationen korrelieren.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

