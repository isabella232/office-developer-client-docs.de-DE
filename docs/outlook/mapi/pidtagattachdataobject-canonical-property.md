---
title: PidTagAttachDataObject (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachDataObject
api_type:
- HeaderDef
ms.assetid: b76312c6-7682-4ded-be25-55e21b0b091b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 84cfacf841299ed3552f0f25f25ee7cbc52975a1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566885"
---
# <a name="pidtagattachdataobject-canonical-property"></a>PidTagAttachDataObject (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Anlagenobjekt, auf das in der Regel über die **OLE-Schnittstelle** (Object Linking and Embedding) zugegriffen wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_DATA_OBJ  <br/> |
|Kennung:  <br/> |0x3701  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft enthält die Anlage, wenn der Wert der **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) -Eigenschaft **ATTACH_EMBEDDED_MSG** oder **ATTACH_OLE** ist. Der OLE-Codierungstyp kann anhand **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) bestimmt werden. 
  
Für eine Anlage, die dem **ATTACH_EMBEDDED_MSG** Wert zugeordnet ist, kann die [IMessage:IMAPIProp-Schnittstelle](imessageimapiprop.md) für schnelleren Zugriff verwendet werden. 
  
Für ein eingebettetes dynamisches OLE-Objekt enthält die **PR_ATTACH_DATA_OBJ-Eigenschaft** eigene Renderinginformationen, und die **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) -Eigenschaft sollte entweder nicht vorhanden oder leer sein. 
  
Bei einer OLE-Dokumentdateianlage muss der Nachrichtenspeicheranbieter auf einen [IMAPIProp::OpenProperty-Aufruf](imapiprop-openproperty.md) auf **PR_ATTACH_DATA_OBJ** reagieren und optional auf einen Aufruf von **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) antworten. Die **Eigenschaften PR_ATTACH_DATA_BIN** und **PR_ATTACH_DATA_OBJ** weisen denselben Eigenschaftsbezeichner auf und sind daher zwei Darstellungen derselben Eigenschaft. 
  
Für ein Speicherobjekt, z. B. eine Verbunddatei im OLE 2.0-Docfile-Format, ermöglichen einige Dienstanbieter das Öffnen mit der **MAPI-IStreamDocfile-Schnittstelle,** einer Unterklasse von **IStream** ohne zusätzliche Elemente, die die Leistung optimieren soll. Die potenzielle Kosteneinsparung reicht aus, um den Versuch zu rechtfertigen, **PR_ATTACH_DATA_OBJ** über **IStreamDocfile** zu öffnen. Wenn **MAPI_E_INTERFACE_NOT_SUPPORTED** zurückgegeben wird, kann der Client **PR_ATTACH_DATA_BIN** mit **IStream** öffnen. 
  
Wenn die Clientanwendung oder der Dienstanbieter ein Anlagenunterobjekt nicht mithilfe von **PR_ATTACH_DATA_OBJ** mithilfe von **PR_ATTACH_METHOD** öffnen kann, sollte **PR_ATTACH_DATA_BIN** verwendet werden. 
  
Weitere Informationen zu OLE-Schnittstellen und -Formaten finden Sie unter [OLE und Datenübertragung.](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
## <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

