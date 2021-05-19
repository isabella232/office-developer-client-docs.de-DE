---
title: PidTagAttachDataObject (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataObject
api_type:
- HeaderDef
ms.assetid: b76312c6-7682-4ded-be25-55e21b0b091b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3961330476cad8947f94152e49c90adb1e8f8b21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339284"
---
# <a name="pidtagattachdataobject-canonical-property"></a>PidTagAttachDataObject (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Attachment-Objekt, auf das in der Regel über die **Ole-IStorage-Schnittstelle** (Object Linking and Embedding) zugegriffen wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_DATA_OBJ  <br/> |
|Kennung:  <br/> |0x3701  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft enthält die Anlage, wenn der Wert der **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) -Eigenschaft ATTACH_EMBEDDED_MSG **oder** **ATTACH_OLE**. Der #A0 kann anhand von PR_ATTACH_TAG **(** [PidTagAttachTag](pidtagattachtag-canonical-property.md)) bestimmt werden. 
  
Für eine Anlage, die dem ATTACH_EMBEDDED_MSG **zugeordnet** ist, kann die [IMessage:IMAPIProp-Schnittstelle](imessageimapiprop.md) für einen schnelleren Zugriff verwendet werden. 
  
Für ein eingebettetes dynamisches #A0 enthält die **PR_ATTACH_DATA_OBJ-Eigenschaft** eigene Renderinginformationen, und die **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) -Eigenschaft sollte nicht vorhanden oder leer sein. 
  
Für eine #A0 muss der Nachrichtenspeicheranbieter auf einen [IMAPIProp::OpenProperty-Aufruf](imapiprop-openproperty.md) an **PR_ATTACH_DATA_OBJ** reagieren und kann optional auf einen Aufruf von **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) reagieren. Die **PR_ATTACH_DATA_BIN** und **PR_ATTACH_DATA_OBJ** haben dieselbe Eigenschafts-ID und sind somit zwei Wiedergaben derselben Eigenschaft. 
  
Für ein Speicherobjekt, z. B. eine Zusammengesetztdatei im OLE 2.0-Docfile-Format, ermöglichen einige Dienstanbieter das Öffnen mit der MAPI **IStreamDocfile-Schnittstelle,** einer Unterklasse von **IStream** ohne zusätzliche Member, die zur Optimierung der Leistung entwickelt wurde. Das potenzielle Speichern reicht aus,  um den Versuch zu rechtfertigen, PR_ATTACH_DATA_OBJ **IStreamDocfile zu öffnen.** Wenn **MAPI_E_INTERFACE_NOT_SUPPORTED** zurückgegeben wird, kann der Client  die PR_ATTACH_DATA_BIN **IStream öffnen.** 
  
Wenn die Clientanwendung oder der Dienstanbieter ein Anlagenunterobjekt nicht mithilfe von PR_ATTACH_DATA_OBJ mithilfe von **PR_ATTACH_METHOD** öffnen **kann,** sollte PR_ATTACH_DATA_BIN **.** 
  
Weitere Informationen zu OLE-Schnittstellen und -Formaten finden Sie unter [OLE und Datenübertragung](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
## <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

