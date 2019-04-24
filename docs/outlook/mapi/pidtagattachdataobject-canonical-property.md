---
title: Kanonische Pidtagattachdataobject (-Eigenschaft
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
ms.openlocfilehash: 3961330476cad8947f94152e49c90adb1e8f8b21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339284"
---
# <a name="pidtagattachdataobject-canonical-property"></a>Kanonische Pidtagattachdataobject (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Attachment-Objekt, auf das normalerweise über die OLE- **IStorage** -Schnittstelle (Object Linking and Embedding) zugegriffen wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_DATA_OBJ  <br/> |
|Kennung:  <br/> |0x3701  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft enthält die Anlage, wenn der Wert der **PR_ATTACH_METHOD** ([pidtagattachmethod (](pidtagattachmethod-canonical-property.md))-Eigenschaft **ATTACH_EMBEDDED_MSG** oder **ATTACH_OLE**ist. Der OLE-Codierungs kann von **PR_ATTACH_TAG** ([pidtagattachtag (](pidtagattachtag-canonical-property.md)) bestimmt werden. 
  
Für eine Anlage, die mit dem **ATTACH_EMBEDDED_MSG** -Wert verknüpft ist, kann die [IMessage: IMAPIProp](imessageimapiprop.md) -Schnittstelle für einen schnelleren Zugriff verwendet werden. 
  
Bei einem eingebetteten dynamischen OLE-Objekt enthält die **PR_ATTACH_DATA_OBJ** -Eigenschaft eigene Renderinginformationen, und die **PR_ATTACH_RENDERING** ([pidtagattachrendering (](pidtagattachrendering-canonical-property.md))-Eigenschaft sollte entweder nicht vorhanden oder leer sein. 
  
Bei einer OLE-Dokumentdatei Anlage muss der Nachrichtenspeicher Anbieter auf einen [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Aufruf für **PR_ATTACH_DATA_OBJ** reagieren und optional auf einen Aufruf von **PR_ATTACH_DATA_BIN** ([pidtagattachdatabinary (](pidtagattachdatabinary-canonical-property.md) ). Die Eigenschaften **PR_ATTACH_DATA_BIN** und **PR_ATTACH_DATA_OBJ** verwenden denselben Eigenschaftenbezeichner und sind daher zwei Darstellungen derselben Eigenschaft. 
  
Bei einem Speicherobjekt, wie beispielsweise einer Verbunddatei im DOCFILE-Format von OLE 2,0, können einige Dienstanbieter diese mit der MAPI- **IStreamDocfile** -Schnittstelle öffnen, eine Unterklasse von **IStream** ohne zusätzliche Mitglieder, die die Leistung optimieren soll. Das potenzielle speichern reicht aus, um das Öffnen von **PR_ATTACH_DATA_OBJ** über **IStreamDocfile**zu rechtfertigen. Wenn **MAPI_E_INTERFACE_NOT_SUPPORTED** zurückgegeben wird, kann der Client **PR_ATTACH_DATA_BIN** mit **IStream**öffnen. 
  
Wenn die Clientanwendung oder der Dienstanbieter ein Attachment-Unterobjekt nicht mithilfe von **PR_ATTACH_DATA_OBJ** mit der Hilfe von **PR_ATTACH_METHOD**öffnen kann, sollte es **PR_ATTACH_DATA_BIN**verwenden. 
  
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

