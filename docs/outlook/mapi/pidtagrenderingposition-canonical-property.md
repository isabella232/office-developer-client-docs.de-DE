---
title: PidTagRenderingPosition (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d463be4a14ecf478bdcbddc50b4ad9360829befc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355153"
---
# <a name="pidtagrenderingposition-canonical-property"></a>PidTagRenderingPosition (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Offset in Zeichen, der beim Rendern einer Anlage innerhalb des Hauptnachrichtentexts verwendet werden soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RENDERING_POSITION  <br/> |
|Kennung:  <br/> |0x370B  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Anlage  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn der angegebene Offset -1 (0xFFFFFFFF) ist, wird die Anlage nicht mithilfe dieser Eigenschaft gerendert. Alle anderen Werte als -1 geben die Position innerhalb der **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft an, an der die Anlage gerendert werden soll.
  
 **Hinweis** Das durch diese Eigenschaft **in** der PR_BODY angegebene Zeichen wird durch die Anlage ersetzt. In der Regel handelt es sich bei diesem Zeichen um ein Leerzeichen, obwohl auch ein spezielles Platzhalterzeichen verwendet werden kann. 
  
Diese Eigenschaft wird in Zeichen ausgedrückt. In einigen Zeichensätzen entspricht dies nicht Byte. Unicode-Anwendungen können die Position basierend auf zwei Bytezeichen berechnen. Double-Byte (Character Set, DBCS)-Anwendungen müssen den Text bis zu diesem Eigenschaftswert überprüfen, da die Zeichendarstellung zwischen einem und zwei Bytes pro Zeichen variiert.
  
Diese Eigenschaft sollte nicht mit Rich Text Format (RTF)-Text verwendet werden. Die Renderingposition wird in RTF durch eine Escapesequenz angegeben, die als Objektanlageplatzhalter bezeichnet wird. Diese Sequenz besteht aus der Zeichenfolge gefolgt von einem einzelnen Zeichen, normalerweise einem Leerzeichen, das durch das Rendering  `\objattph` der Anlage ersetzt wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

