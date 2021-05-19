---
title: PidLidFlagString (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagString
api_type:
- COM
ms.assetid: 4cf1e08b-c869-4965-a1e4-512a0684700f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b3cd88db7e93b53990cf0181af623ebca75f0c6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357785"
---
# <a name="pidlidflagstring-canonical-property"></a>PidLidFlagString (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Index, der eine der vordefinierten Textzeichenfolgen identifiziert, die dem Flag zugeordnet sind.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidFlagStringEnum  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Lange ID (LID):  <br/> |0x000085C0  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn diese Eigenschaft festgelegt ist, sollten Clients den entsprechenden Zeichenfolgenwert in den folgenden Tabellen verwenden (beispielsweise, um eine Zeichenfolge zu ersetzen, die in die Sprache des aktuellen Benutzers übersetzt wird), und den in **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) und **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) festgelegten Wert ignorieren. 
  
Folgende Standardeinstellungen werden dem Benutzer für Kontaktobjekte vorgeschlagen:
  
|**Wert**|**Englische Zeichenfolge**|
|:-----|:-----|
|0x00000000 oder nicht vorhanden  <br/> | Befolgen Sie die Anweisungen zum Anzeigen von **dispidFlagRequest**.  <br/> |
|0x0000006E  <br/> |"Follow up"  <br/> |
|0x0000006F  <br/> |"Anruf"  <br/> |
|0x00000070  <br/> |"Besprechung anordnen"  <br/> |
|0x00000071  <br/> |"E-Mail senden"  <br/> |
|0x00000072  <br/> |"Brief senden"  <br/> |
   
Für alle anderen Nachrichtenobjekte werden dem Benutzer die folgenden Standardwerte vorgeschlagen:
  
|**Wert**|**Englische Zeichenfolge**|
|:-----|:-----|
|0x00000000 oder nicht vorhanden  <br/> | Befolgen Sie die Anweisungen zum Anzeigen von **dispidFlagRequest**.  <br/> |
|0x00000001  <br/> |"Anruf"  <br/> |
|0x00000002  <br/> |"Nicht weiterleiten"  <br/> |
|0x00000003  <br/> |"Follow up"  <br/> |
|0x00000004  <br/> |"For Your Information"  <br/> |
|0x00000005  <br/> |"Weiterleiten"  <br/> |
|0x00000006  <br/> |"Keine Antwort erforderlich"  <br/> |
|0x00000007  <br/> |"Read"  <br/> |
|0x00000008  <br/> |"Antworten"  <br/> |
|0x00000009  <br/> |"Allen antworten"  <br/> |
|0x0000000A  <br/> |"Review"  <br/> |
   
Alle oben angegebenen Zeichenfolgen können gegebenenfalls in die Sprache des Benutzers übersetzt werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

