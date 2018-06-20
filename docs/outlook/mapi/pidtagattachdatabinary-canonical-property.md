---
title: Kanonische PidTagAttachDataBinary-Eigenschaft
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
ms.openlocfilehash: 3646f3e3906e62fe148fe1c2b6ddca39013391e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794092"
---
# <a name="pidtagattachdatabinary-canonical-property"></a>Kanonische PidTagAttachDataBinary-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält die binären Anlagedaten in der Regel über die Schnittstelle Object Linking and Embedding (OLE) **IStream** zugegriffen. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_ATTACH_DATA_BIN  <br/> |
|Bezeichner:  <br/> |0x3701  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |E-Mail-Anlage  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft enthält das Attachment-Objekt, wenn der Wert der Eigenschaft **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) ATTACH_BY_VALUE, ist die übliche Anlage-Methode und die einzige unterstützt werden müssen. **PR_ATTACH_DATA_BIN** enthält auch Anlage OLE 1.0 **OLESTREAM** , wenn der Wert der **PR_ATTACH_METHOD** ATTACH_OLE ist. 
  
 **OLESTREAM** Anlagen können durch Aufrufen der OLE **:: CopyTo** -Methode in eine Datei kopiert werden. Das Codierungstyp OLE kann von der **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md))-Eigenschaft ermittelt werden. 
  
Für ein OLE-Dokument-Dateianlage Anbieter die Nachricht muss auf einen Aufruf [IMAPIProp::OpenProperty](imapiprop-openproperty.md) **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) reagieren und reagiert optional zu einem Anruf auf **PR_ATTACH_DATA_BIN **. Beachten Sie, dass **PR_ATTACH_DATA_BIN** und **PR_ATTACH_DATA_OBJ** der Bezeichner für die gleichen freigeben, und daher zwei Darstellungen der gleichen-Eigenschaft werden. 
  
Für ein Speicherobjekt können beispielsweise eine Verbunddatei in OLE 2.0-Dokumentdatei-Format, einige Dienstanbieter mit der MAPI- **IStreamDocfile** -Schnittstelle für verbesserte Leistung geöffnet werden. Ein Anbieter, der **IStreamDocfile** unterstützt muss es auf **PR_ATTACH_DATA_OBJ** verfügbar machen und kann optional auf **PR_ATTACH_DATA_BIN**machen. 
  
Weitere Informationen zu OLE-Schnittstellen und Formate finden Sie unter [OLE und Daten übertragen](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx). 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
## <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

