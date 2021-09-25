---
title: Kanonische PidLidFlagRequest-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidFlagRequest
api_type:
- COM
ms.assetid: 38981f07-14b8-47c2-93df-e6aed91896e4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 536ec8f3922aadcf71eb89f67d4237efc0dfea5b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555769"
---
# <a name="pidlidflagrequest-canonical-property"></a>Kanonische PidLidFlagRequest-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt den Status einer Besprechungsanfrage dar.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidRequest  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008530  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Kennzeichnen  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

In Microsoft Office Outlook ist eine Besprechungsanfrage ein Terminelement.
  
Diese Eigenschaft enthält benutzerdefinierten Text, der dem Flag zugeordnet werden soll, und sollte festgelegt werden, wenn das Nachrichtenobjekt gekennzeichnet oder abgeschlossen ist, aber für ein Besprechungsobjekt nicht vorhanden sein sollte. Clients können diese Eigenschaft nicht unterstützen und immer "Follow up" (ggf. in die Sprache des Benutzers übersetzt) als Wert der Zeichenfolge schreiben, wenn diese Eigenschaft festgelegt werden soll. Diese Eigenschaft sollte basierend auf den Werten der Eigenschaften **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) und **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) bedingt ignoriert werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

