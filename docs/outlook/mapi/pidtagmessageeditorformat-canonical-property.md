---
title: PidTagMessageEditorFormat (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageEditorFormat
api_type:
- HeaderDef
ms.assetid: 197b21ed-9f2f-425f-a6ed-cae1208fa2ca
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dd107de00ebc7ab55b6d255c4bc993d9c3210086
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560886"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a>PidTagMessageEditorFormat (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt das Format an, das ein Editor zum Anzeigen einer Nachricht verwenden soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MSG_EDITOR_FORMAT  <br/> |
|Kennung:  <br/> |0x5909  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Sonstiges  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die möglichen Werte für **PR_MSG_EDITOR_FORMAT** können eine der folgenden Sein: 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|**EDITOR_FORMAT_DONTKNOW** <br/> |Das für den Editor zu verwendende Format ist unbekannt.  <br/> |
|**EDITOR_FORMAT_PLAINTEXT** <br/> |Der Editor sollte die Nachricht im Nur-Text-Format anzeigen.  <br/> |
|**EDITOR_FORMAT_HTML** <br/> |Der Editor sollte die Nachricht im HTML-Format anzeigen.  <br/> |
|**EDITOR_FORMAT_RTF** <br/> |Der Editor sollte die Nachricht im Rich-Text-Format anzeigen.  <br/> |
   
Standardmäßig E-Mail-Nachrichten (mit der Nachrichtenklasse **IPM. Hinweis** oder mit einer von IPM abgeleiteten benutzerdefinierten **Nachrichtenklasse. Hinweis**) gesendet von einem POP3/SMTP-E-Mail-Konto werden im transportneutralen Kapselungsformat (Transport Neutral Encapsulation Format, TNEF) gesendet. Die **PR_MSG_EDITOR_FORMAT-Eigenschaft** kann verwendet werden, um beim Senden einer Nachricht nur Nur-Text und nicht TNEF zu erzwingen. Wenn **PR_MSG_EDITOR_FORMAT** auf **EDITOR_FORMAT_PLAINTEXT** festgelegt ist, wird die Nachricht als Nur-Text ohne TNEF gesendet. Wenn **PR_MSG_EDITOR_FORMAT** auf **EDITOR_FORMAT_RTF** festgelegt ist, wird die TNEF-Codierung implizit aktiviert, und die Nachricht wird mithilfe des Standard-Internetformats gesendet, das im Outlook-Client angegeben ist.
  
Es gibt zwei weitere Möglichkeiten, die Verwendung von TNEF beim Senden einer Nachricht zu erzwingen.
  
- Wenn Sie die benannte Eigenschaft **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) in einer Nachricht auf "True" festlegen, bedeutet dies, dass TNEF beim Konvertieren der Nachricht von MAPI in MIME/SMTP eingeschlossen werden sollte. Beachten Sie, dass **dispidUseTNEF** nur gilt, wenn die Nachricht von einem POP3/SMTP-E-Mail-Konto gesendet wird, und nicht, wenn die Nachricht von anderen Anbietern wie Microsoft Exchange Server gesendet wird. **dispidUseTNEF** setzt die Einstellung in **PR_MSG_EDITOR_FORMAT** außer Kraft.
    
- Die  Verwendung des CCSF_USE_TNEF-Flags beim Aufrufen von [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) zum Konvertieren einer ausgehenden MAPI-Nachricht in einen MIME-Stream kann auch TNEF erzwingen. Dies gilt auch, wenn **dispidUseTNEF** nicht festgelegt ist. 
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

