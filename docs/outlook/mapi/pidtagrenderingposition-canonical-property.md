---
title: Kanonische Pidtagrenderingposition (-Eigenschaft
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
ms.openlocfilehash: d463be4a14ecf478bdcbddc50b4ad9360829befc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355153"
---
# <a name="pidtagrenderingposition-canonical-property"></a>Kanonische Pidtagrenderingposition (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Offset in Zeichen, der beim Rendern einer Anlage im Hauptnachrichtentext verwendet werden soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RENDERING_POSITION  <br/> |
|Kennung:  <br/> |0x370B  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Anlage  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn der angegebene Offset-1 (0xFFFFFFFF) ist, wird die Anlage nicht mithilfe dieser Eigenschaft gerendert. Alle anderen Werte als-1 geben die Position in der **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft an, in der die Anlage gerendert werden soll.
  
 **Hinweis** Das von dieser Eigenschaft in **PR_BODY** angegebene Zeichen wird durch die Anlage ersetzt. In der Regel handelt es sich um ein Leerzeichen, auch wenn ein besonderes Platzhalterzeichen verwendet werden kann. 
  
Diese Eigenschaft wird in Zeichen ausgedrückt. In einigen Zeichensätzen ist dies nicht gleichbedeutend mit Bytes. Unicode-Anwendungen können die Position anhand von zwei-Byte-Zeichen berechnen. DBCS-Anwendungen (Double-Byte Character Set) müssen den Text bis zu diesem Eigenschaftswert überprüfen, da ihre Zeichendarstellung zwischen 1 und 2 Byte pro Zeichen variiert.
  
Diese Eigenschaft sollte nicht mit RTF-Text (Rich Text Format) verwendet werden. Die Wiedergabeposition wird in RTF durch eine Escape-Sequenz mit dem Namen Object Attachment PlaceHolder angegeben. Diese Sequenz besteht aus der Zeichen `\objattph` Folge, gefolgt von einem einzelnen Zeichen, normalerweise einem Leerraum, der durch das Anlagen Rendering ersetzt wird. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
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

