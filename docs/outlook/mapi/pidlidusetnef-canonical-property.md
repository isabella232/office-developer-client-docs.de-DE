---
title: Kanonische PidLidUseTnef-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidUseTnef
api_type:
- COM
ms.assetid: 954048d6-e2eb-43e7-b52c-c2f047bb84a4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 73fa4311a61be9259d8c45aca79d719785c213a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793906"
---
# <a name="pidlidusetnef-canonical-property"></a>Kanonische PidLidUseTnef-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Gibt an, ob Transport Neutral Encapsulation Format (TNEF) für eine Nachricht eingeschlossen werden soll, wenn die Nachricht von MAPI (MULTIPURPOSE Internet Mail Extensions) oder Simple Mail Transfer Protocol (SMTP)-Format konvertiert wird.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidUseTNEF  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Common  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008582  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Laufzeit-Konfiguration  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt an, ob TNEF für eine Nachricht eingeschlossen werden soll, wenn dieser Nachricht von TNEF in MIME- oder SMTP-Format konvertiert wird. Diese Eigenschaft ist nicht vorhanden, und gegebenenfalls TNEF darf nicht enthalten sein für die Nachricht.
  
Diese Eigenschaft gilt nur, wenn die Nachricht aus einem POP3/SMTP-Mail-Konto gesendet wird und wird nicht angewendet, wenn die Nachricht von anderen Anbietern wie beispielsweise Microsoft Exchange Server gesendet wird.
  
Unter bestimmten Umständen wie beim Stimmabgabe Schaltflächen aktiviert sind, oder eine OLE eingebettete Objekt an eine Nachricht angefügt ist kann Outlook diese Eigenschaft so erzwingen Sie die Verwendung von TNEF festlegen.
  
Die **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md))-Eigenschaft kann nur nur-Text und nicht-TNEF zu erzwingen, beim Senden einer Nachricht verwendet werden. Da **PidLidUseTNEF** die Einstellung in **PR_MSG_EDITOR_FORMAT**überschreibt, sollte auch eine Anwendung, die nur-Text für eine ausgehende Nachricht erzwingen möchte **PidLidUseTNEF** suchen und ihn auf FALSE zurücksetzen. Darüber hinaus muss das Add-in die Nachrichtenfunktionen entfernen, die TNEF benötigen, um Endbenutzern nicht genutzt werden Anlagen für die Nachricht zu vermeiden, die schließlich gesendet wird. 
  
Verwenden Sie das Kennzeichen **CCSF_USE_TNEF** beim Aufruf von [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) zum Konvertieren einer ausgehenden MAPI-Nachricht in einen MIME-Stream kann auch TNEF durchsetzen. Dies gilt, auch wenn **PidLidUseTNEF** nicht festgelegt ist. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

