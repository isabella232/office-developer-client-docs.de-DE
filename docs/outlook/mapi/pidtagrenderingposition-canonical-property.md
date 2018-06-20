---
title: Kanonische PidTagRenderingPosition-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRenderingPosition
api_type:
- COM
ms.assetid: bce46687-17dc-4a3f-96be-303d8755158e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: aa149a81102a4981712ea3ca897d8b1ad448a1eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794955"
---
# <a name="pidtagrenderingposition-canonical-property"></a>Kanonische PidTagRenderingPosition-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält einen Offset in Zeichen, die beim Rendern einer Anlage im Hauptfenster Nachrichtentext verwenden.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_RENDERING_POSITION  <br/> |
|Bezeichner:  <br/> |0x370B  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Anlage  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn der angegebene Offset-1 (0xFFFFFFFF) ist, wird die Anlage unter Verwendung dieser Eigenschaft nicht gerendert. Alle Werte, die als-1 Geben Sie an der Position innerhalb der **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft, an der die Anlage ist gerendert werden soll.
  
 **Hinweis** Die von dieser Eigenschaft in **PR_BODY** angegebene Zeichen wird durch die Anlage ersetzt. In der Regel ist dieses Zeichen ein Leerzeichen, obwohl eine spezielle Platzhalterzeichen auch verwendet werden kann. 
  
Diese Eigenschaft wird in Zeichen angegeben. In einigen Zeichensätzen entspricht dies nicht Bytes. Unicode-Anwendungen können die Position, basierend auf 2-Byte-Zeichen berechnen. Double-Byte-Zeichen (DBCS) Applications müssen den Text bis zum den Wert Eigenschaft überprüft den Ordner, da deren Darstellung von Zeichen zwischen ein oder zwei Bytes pro Zeichen variiert.
  
Diese Eigenschaft sollte nicht mit Rich Text Format (RTF) Text verwendet werden. Die Renderingposition wird durch Escapesequenz aufgerufen, den Platzhalter Objekt Anlage im RTF angezeigt. In den folgenden Schritten die Zeichenfolge besteht aus `\objattph` gefolgt von einem einzelnen Zeichen, normalerweise ein Leerzeichen, die durch das Rendering Anlage ersetzt werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
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

