---
title: PidTagMessageEditorFormat (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c9c12d3e8314dea5be67727d0f286e7df13038fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574370"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a>PidTagMessageEditorFormat (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt das Format für einen-Editor zu verwenden, um eine Nachricht anzuzeigen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MSG_EDITOR_FORMAT  <br/> |
|Kennung:  <br/> |0x5909  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Verschiedenes  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die möglichen Werte für **PR_MSG_EDITOR_FORMAT** können eine der folgenden sein: 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|**EDITOR_FORMAT_DONTKNOW** <br/> |Das Format für den Editor an ist unbekannt.  <br/> |
|**EDITOR_FORMAT_PLAINTEXT** <br/> |Im Editor sollten die Nachricht im nur-Text-Format angezeigt.  <br/> |
|**EDITOR_FORMAT_HTML** <br/> |Im Editor sollten die Nachricht im HTML-Format angezeigt.  <br/> |
|**EDITOR_FORMAT_RTF** <br/> |Im Editor sollten die Nachricht im RTF-Format angezeigt.  <br/> |
   
Standardmäßig Mail-Nachrichten (mit der Nachrichtenklasse IPM **. Hinweis** oder mit einer benutzerdefinierten Nachrichtenklasse IPM **abgeleitet. Beachten Sie**) gesendet von einem POP3/SMTP e-Mail Konto in Transport Neutral Encapsulation Format (TNEF) gesendet werden. Die **PR_MSG_EDITOR_FORMAT** -Eigenschaft kann nur nur-Text und nicht-TNEF zu erzwingen, beim Senden einer Nachricht verwendet werden. Wenn **bei** **PR_MSG_EDITOR_FORMAT** festgelegt ist, wird die Nachricht als nur-Text ohne TNEF gesendet. Wenn **PR_MSG_EDITOR_FORMAT** auf **EDITOR_FORMAT_RTF**festgelegt ist, TNEF-Codierung ist implizit aktiviert, und die Nachricht wird gesendet, mit der Internet-Standardformat, das im Outlook-Client angegeben ist.
  
Es gibt zwei andere Methoden, um die Verwendung von TNEF erzwingen beim Senden einer Nachricht.
  
- Festlegen der **DispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) mit dem Namen-Eigenschaft auf True für eine Nachricht gibt an, dass beim Konvertieren der Nachricht von MAPI in MIME/SMTP TNEF eingeschlossen werden sollen. Hinweis: Diese **DispidUseTNEF** gilt nur, wenn die Nachricht wird aus einem POP3/SMTP-Mail-Konto gesendet, und wird nicht angewendet, wenn die Nachricht von anderen Anbietern wie beispielsweise Microsoft Exchange Server gesendet wird. **DispidUseTNEF** überschreibt die Einstellung in **PR_MSG_EDITOR_FORMAT**.
    
- Verwenden die Kennzeichen **CCSF_USE_TNEF** beim Aufruf von [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) zum ausgehenden MAPI-Nachrichten in einen MIME-Stream konvertieren kann auch TNEF erzwingen. Dies gilt, auch wenn **DispidUseTNEF** nicht festgelegt ist. 
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Definiert die grundlegende Datenstrukturen, die verwendet werden remote-Vorgängen.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

