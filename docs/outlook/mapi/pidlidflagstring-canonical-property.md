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
ms.openlocfilehash: b29fdbb82635ca7706be15ee9f674262d2204ad5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576183"
---
# <a name="pidlidflagstring-canonical-property"></a>PidLidFlagString (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält einen Index, der eine Reihe von vordefinierten Textzeichenfolgen, die das Flag zugeordnet identifiziert.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidFlagStringEnum  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Common  <br/> |
|Long-ID (Abdeckung):  <br/> |0x000085C0  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn diese Eigenschaft festgelegt ist, sollten Clients den entsprechenden String-Wert in den Tabellen unten (beispielsweise um eine Zeichenfolge zu ersetzen, die in der aktuellen Sprache des Benutzers übersetzt wird), und den Wert im **DispidFlagRequest** ([ ignorieren soll PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) und **DispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)). 
  
Standardeinstellungen für den Benutzer für Kontaktobjekte vorgeschlagene lauten wie folgt:
  
|**Wert**|**Englische Zeichenfolge**|
|:-----|:-----|
|0 x 00000000 oder nicht vorhanden  <br/> | Führen Sie die Anweisungen im Zusammenhang mit **DispidFlagRequest**anzeigen.  <br/> |
|0x0000006E  <br/> |"Nachverfolgung"  <br/> |
|0x0000006F  <br/> |"Anrufen"  <br/> |
|0 x 00000070  <br/> |"Meeting anordnen"  <br/> |
|0 x 00000071  <br/> |"Senden Sie E-Mail"  <br/> |
|0x00000072  <br/> |"Senden Sie Brief"  <br/> |
   
Standardeinstellungen für den Benutzer für alle anderen Nachrichtenobjekte vorgeschlagenen lauten wie folgt:
  
|**Wert**|**Englische Zeichenfolge**|
|:-----|:-----|
|0 x 00000000 oder nicht vorhanden  <br/> | Führen Sie die Anweisungen im Zusammenhang mit **DispidFlagRequest**anzeigen.  <br/> |
|0x00000001  <br/> |"Anrufen"  <br/> |
|0x00000002  <br/> |"Nicht weiterleiten"  <br/> |
|0 x 00000003  <br/> |"Nachverfolgung"  <br/> |
|0 x 00000004  <br/> |"Zu Ihrer Information"  <br/> |
|0 x 00000005  <br/> |"Weiterleiten"  <br/> |
|0 x 00000006  <br/> |"Antwort nicht erforderlich"  <br/> |
|0 x 00000007  <br/> |"Read"  <br/> |
|0 x 00000008  <br/> |"Antwort"  <br/> |
|0x00000009  <br/> |"Allen Antworten"  <br/> |
|0x0000000A  <br/> |"Prüfung"  <br/> |
   
Alle oben angegebene Zeichenfolgen können in der Sprache des Benutzers, falls zutreffend übersetzt werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

