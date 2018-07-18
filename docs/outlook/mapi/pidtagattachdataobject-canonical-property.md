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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b3fc7690a8c9eb2ada3a34bc44217ff463721e4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794081"
---
# <a name="pidtagattachdataobject-canonical-property"></a>PidTagAttachDataObject (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält ein Attachment-Objekt in der Regel über die Schnittstelle Object Linking and Embedding (OLE) **IStorage** zugegriffen. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_ATTACH_DATA_OBJ  <br/> |
|Bezeichner:  <br/> |0x3701  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |E-Mail-Anlage  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft enthält das Attachment-Objekt, wenn der Wert der Eigenschaft **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) **ATTACH_EMBEDDED_MSG** oder **ATTACH_OLE**ist. Das Codierungstyp OLE kann aus **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) bestimmt werden. 
  
Für eine Anlage **ATTACH_EMBEDDED_MSG** Wert zugeordnet ist kann die [IMessage:IMAPIProp](imessageimapiprop.md) -Schnittstelle für einen schnelleren Zugriff verwendet werden. 
  
Bei einem eingebetteten dynamische OLE-Objekt die **PR_ATTACH_DATA_OBJ** -Eigenschaft enthält eine eigenen Renderinginformationen und die **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md))-Eigenschaft sollte entweder nicht vorhanden oder leer sein. 
  
Für ein OLE-Dokument-Dateianlage Anbieter die Nachricht muss auf einen Aufruf [IMAPIProp::OpenProperty](imapiprop-openproperty.md) **PR_ATTACH_DATA_OBJ** reagieren und reagiert optional zu einem Anruf auf **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md) ). Die Eigenschaften **PR_ATTACH_DATA_BIN** und **PR_ATTACH_DATA_OBJ** Freigeben der Bezeichner für die gleichen und daher sind zwei Darstellungen der gleichen-Eigenschaft. 
  
Für ein Speicherobjekt können beispielsweise eine Verbunddatei in OLE 2.0-Dokumentdatei-Format, einige Dienstanbieter geöffnet werden, mit der MAPI- **IStreamDocfile** -Schnittstelle eine Unterklasse der **IStream** ohne zusätzliche Mitglieder, entwickelt, um die Leistung zu optimieren. Das potenzielle speichern reicht zu rechtfertigen Versuch **PR_ATTACH_DATA_OBJ** über **IStreamDocfile**zu öffnen. Wenn **MAPI_E_INTERFACE_NOT_SUPPORTED** zurückgegeben wurde, kann der Client **PR_ATTACH_DATA_BIN** mit **IStream**öffnen. 
  
Wenn der Clientanwendung oder Dienstanbieter ein Unterobjekt Anlage nicht öffnen kann mithilfe von **PR_ATTACH_DATA_OBJ** mit Hilfe von **PR_ATTACH_METHOD**, sollte **PR_ATTACH_DATA_BIN**verwendet werden. 
  
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

