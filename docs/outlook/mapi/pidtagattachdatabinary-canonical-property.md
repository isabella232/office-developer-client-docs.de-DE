---
title: PidTagAttachDataBinary (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachDataBinary
api_type:
- HeaderDef
ms.assetid: 3b0a8b28-863e-4b96-a4c0-fdb8f40555b9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 33f850ba7ceb124522212459b25de0483a9495b7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563896"
---
# <a name="pidtagattachdatabinary-canonical-property"></a>PidTagAttachDataBinary (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält binäre Anlagendaten, auf die in der Regel über die **OLE-IStream-Schnittstelle** (Object Linking and Embedding) zugegriffen wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_DATA_BIN  <br/> |
|Kennung:  <br/> |0x3701  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft enthält die Anlage, wenn der Wert der **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) -Eigenschaft ATTACH_BY_VALUE ist. Dies ist die übliche Anlagemethode und die einzige, die unterstützt werden muss. **PR_ATTACH_DATA_BIN** enthält auch eine OLE 1.0 **OLESTREAM-Anlage,** wenn der Wert von **PR_ATTACH_METHOD** ATTACH_OLE ist. 
  
 **OLESTREAM-Anlagen** können durch Aufrufen der OLE **IStream::CopyTo-Methode** in eine Datei kopiert werden. Der OLE-Codierungstyp kann anhand der **eigenschaft PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) bestimmt werden. 
  
Bei einer OLE-Dokumentdateianlage muss der Nachrichtenspeicheranbieter auf einen [IMAPIProp::OpenProperty-Aufruf](imapiprop-openproperty.md) auf **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) reagieren und optional auf einen Aufruf auf **PR_ATTACH_DATA_BIN** antworten. Beachten Sie, dass **PR_ATTACH_DATA_BIN** und **PR_ATTACH_DATA_OBJ** denselben Eigenschaftsbezeichner verwenden und daher zwei Darstellungen derselben Eigenschaft sind. 
  
Für ein Speicherobjekt, z. B. eine Verbunddatei im OLE 2.0-Docfile-Format, ermöglichen einige Dienstanbieter das Öffnen mit der **MAPI-IStreamDocfile-Schnittstelle,** um die Leistung zu verbessern. Ein Anbieter, der **IStreamDocfile** unterstützt, muss ihn auf **PR_ATTACH_DATA_OBJ** verfügbar machen und kann ihn optional auf **PR_ATTACH_DATA_BIN** verfügbar machen. 
  
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

