---
title: Kanonische PidLidFlagString-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidFlagString
api_type:
- COM
ms.assetid: 4cf1e08b-c869-4965-a1e4-512a0684700f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f3cf778a4854e29c83c5728671f526788d363fb3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604606"
---
# <a name="pidlidflagstring-canonical-property"></a>Kanonische PidLidFlagString-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Index, der eine gruppe vordefinierter Textzeichenfolgen identifiziert, die dem Flag zugeordnet sind.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidFlagStringEnum  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x000085C0  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Vorgang  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn diese Eigenschaft festgelegt ist, sollten Clients den entsprechenden Zeichenfolgenwert in den folgenden Tabellen verwenden (z. B. um eine Zeichenfolge zu ersetzen, die in die Sprache des aktuellen Benutzers übersetzt wird) und den in **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) und **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) festgelegten Wert ignorieren. 
  
Die Standardwerte, die dem Benutzer für Kontaktobjekte vorgeschlagen werden, sind:
  
|**Wert**|**Englische Zeichenfolge**|
|:-----|:-----|
|0x00000000 oder nicht vorhanden  <br/> | Befolgen Sie die Anweisungen im Zusammenhang mit der Anzeige von **dispidFlagRequest**.  <br/> |
|0x0000006E  <br/> |"Nachverfolgung"  <br/> |
|0x0000006F  <br/> |"Call"  <br/> |
|0x00000070  <br/> |"Besprechung anordnen"  <br/> |
|0x00000071  <br/> |"E-Mail senden"  <br/> |
|0x00000072  <br/> |"Brief senden"  <br/> |
   
Die Standardwerte, die dem Benutzer für alle anderen Nachrichtenobjekte vorgeschlagen werden, sind:
  
|**Wert**|**Englische Zeichenfolge**|
|:-----|:-----|
|0x00000000 oder nicht vorhanden  <br/> | Befolgen Sie die Anweisungen im Zusammenhang mit der Anzeige von **dispidFlagRequest**.  <br/> |
|0x00000001  <br/> |"Call"  <br/> |
|0x00000002  <br/> |"Nicht weiterleiten"  <br/> |
|0x00000003  <br/> |"Nachverfolgung"  <br/> |
|0x00000004  <br/> |"Für Ihre Informationen"  <br/> |
|0x00000005  <br/> |"Weiterleiten"  <br/> |
|0x00000006  <br/> |"Keine Antwort erforderlich"  <br/> |
|0x00000007  <br/> |"Lesen"  <br/> |
|0x00000008  <br/> |"Antworten"  <br/> |
|0x00000009  <br/> |"Allen antworten"  <br/> |
|0x0000000A  <br/> |"Überprüfen"  <br/> |
   
Alle oben angegebenen Zeichenfolgen können ggf. in die Sprache des Benutzers übersetzt werden.
  
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

