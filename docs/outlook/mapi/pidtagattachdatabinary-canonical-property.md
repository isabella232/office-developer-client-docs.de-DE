---
title: Kanonische Pidtagattachdatabinary (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataBinary
api_type:
- HeaderDef
ms.assetid: 3b0a8b28-863e-4b96-a4c0-fdb8f40555b9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1a5f8688b8ea747590cf2a2d6d5efb271aa488f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356546"
---
# <a name="pidtagattachdatabinary-canonical-property"></a>Kanonische Pidtagattachdatabinary (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält binäre Anlagendaten, auf die normalerweise über die **IStream** -Schnittstelle Object Linking and Embedding (OLE) zugegriffen wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_DATA_BIN  <br/> |
|Kennung:  <br/> |0x3701  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft enthält die Anlage, wenn der Wert der **PR_ATTACH_METHOD** ([pidtagattachmethod (](pidtagattachmethod-canonical-property.md))-Eigenschaft ATTACH_BY_VALUE ist, bei dem es sich um die übliche Anlagemethode handelt und die einzige, die unterstützt werden muss. **PR_ATTACH_DATA_BIN** enthält auch eine OLE 1,0- **OLESTREAM** -Anlage, wenn der Wert von **PR_ATTACH_METHOD** ATTACH_OLE ist. 
  
 **OLESTREAM** -Anlagen können durch Aufrufen der OLE **IStream:: CopyTo** -Methode in eine Datei kopiert werden. Der OLE-Codierungs kann anhand der **PR_ATTACH_TAG** ([pidtagattachtag (](pidtagattachtag-canonical-property.md))-Eigenschaft bestimmt werden. 
  
Bei einer OLE-Dokumentdatei Anlage muss der Nachrichtenspeicher Anbieter auf einen [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Aufruf unter **PR_ATTACH_DATA_OBJ** ([pidtagattachdataobject (](pidtagattachdataobject-canonical-property.md)) Antworten und optional auf einen Aufruf von **PR_ATTACH_DATA_BIN **. Beachten Sie, dass **PR_ATTACH_DATA_BIN** und **PR_ATTACH_DATA_OBJ** denselben Eigenschaftenbezeichner verwenden und daher zwei Darstellungen derselben Eigenschaft sind. 
  
Bei einem Speicherobjekt, wie beispielsweise einer Verbunddatei im DOCFILE-Format von OLE 2,0, können einige Dienstanbieter diese mit der MAPI- **IStreamDocfile** -Schnittstelle für eine verbesserte Leistung öffnen. Ein Anbieter, der **IStreamDocfile** unterstützt, muss ihn auf **PR_ATTACH_DATA_OBJ** verfügbar machen und optional auf **PR_ATTACH_DATA_BIN**verfügbar machen. 
  
Weitere Informationen zu OLE-Schnittstellen und Formaten finden Sie unter [OLE und Daten Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx). 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
## <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

