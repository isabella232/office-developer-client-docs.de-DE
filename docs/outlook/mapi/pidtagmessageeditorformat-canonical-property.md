---
title: Kanonische Pidtagmessageeditorformat (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageEditorFormat
api_type:
- HeaderDef
ms.assetid: 197b21ed-9f2f-425f-a6ed-cae1208fa2ca
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 029df4397f4d24c7c111d2017d34e6403df367d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325634"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a>Kanonische Pidtagmessageeditorformat (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt das Format an, mit dem ein Editor eine Nachricht anzeigen soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MSG_EDITOR_FORMAT  <br/> |
|Kennung:  <br/> |0x5909  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Sonstiges  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die möglichen Werte für **PR_MSG_EDITOR_FORMAT** können eine der folgenden sein: 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|**EDITOR_FORMAT_DONTKNOW** <br/> |Das Format für den zu verwendenden Editor ist unbekannt.  <br/> |
|**EDITOR_FORMAT_PLAINTEXT** <br/> |Der Editor sollte die Nachricht im nur-Text-Format anzeigen.  <br/> |
|**EDITOR_FORMAT_HTML** <br/> |Der Editor sollte die Nachricht im HTML-Format anzeigen.  <br/> |
|**EDITOR_FORMAT_RTF** <br/> |Der Editor sollte die Nachricht im Rich-Text-Format anzeigen.  <br/> |
   
Standardmäßig werden e-Mail-Nachrichten (mit der Nachrichtenklasse **IPM. Hinweis** oder mit einer benutzerdefinierten Nachrichtenklasse, die von IPM abgeleitet wurde **. Hinweis**) gesendet von einem POP3/SMTP-e-Mail-Konto werden im Transport Neutral encapsulatIon Format (TNEF) gesendet. Die **PR_MSG_EDITOR_FORMAT** -Eigenschaft kann verwendet werden, um beim Senden einer Nachricht nur einfachen Text und nicht TNEF zu erzwingen. Wenn **PR_MSG_EDITOR_FORMAT** auf **EDITOR_FORMAT_PLAINTEXT**festgelegt ist, wird die Nachricht als nur-Text ohne TNEF gesendet. Wenn **PR_MSG_EDITOR_FORMAT** auf **EDITOR_FORMAT_RTF**festgelegt ist, wird die TNEF-Codierung implizit aktiviert, und die Nachricht wird mithilfe des im Outlook-Client angegebenen Standard-Internet Formats gesendet.
  
Es gibt zwei weitere Möglichkeiten zum Erzwingen der Verwendung von TNEF beim Senden einer Nachricht.
  
- Festlegen der **dispidUseTNEF** ([pidlidusetnef (](pidlidusetnef-canonical-property.md)) benannte Eigenschaft auf true für eine Nachricht gibt an, dass TNEF beim Konvertieren der Nachricht von MAPI in MIME/SMTP eingeschlossen werden soll. Beachten Sie, dass **dispidUseTNEF** nur dann gilt, wenn die Nachricht von einem POP3/SMTP-e-Mail-Konto gesendet wird und nicht gilt, wenn die Nachricht von anderen Anbietern wie Microsoft Exchange Server gesendet wird. **dispidUseTNEF** überschreibt die Einstellung in **PR_MSG_EDITOR_FORMAT**.
    
- Das **CCSF_USE_TNEF** -Flag beim Aufrufen von [IConverterSession:: MAPItoMIMEStm](iconvertersession-mapitomimestm.md) zum Konvertieren einer ausgehenden MAPI-Nachricht in einen MIME-Stream kann auch TNEF erzwingen. Dies gilt auch dann, wenn **dispidUseTNEF** nicht festgelegt ist. 
    
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

