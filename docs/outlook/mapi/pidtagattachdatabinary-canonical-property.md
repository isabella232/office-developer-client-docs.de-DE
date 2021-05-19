---
title: PidTagAttachDataBinary (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1a5f8688b8ea747590cf2a2d6d5efb271aa488f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356546"
---
# <a name="pidtagattachdatabinary-canonical-property"></a>PidTagAttachDataBinary (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält binäre Anlagendaten, auf die in der Regel über die Ole-IStream-Schnittstelle (Object Linking and Embedding) **zugegriffen** wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_DATA_BIN  <br/> |
|Kennung:  <br/> |0x3701  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft enthält die Anlage, wenn der Wert der **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) -Eigenschaft ATTACH_BY_VALUE ist, was die übliche Anlagemethode ist und die einzige, die unterstützt werden muss. **PR_ATTACH_DATA_BIN** enthält auch eine OLE 1.0-OLESTREAM-Anlage, wenn der Wert PR_ATTACH_METHOD **wert** ATTACH_OLE.  
  
 **OLESTREAM-Anlagen** können durch Aufrufen der OLE **IStream::CopyTo-Methode** in eine Datei kopiert werden. Der #A0 kann anhand der **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) bestimmt werden. 
  
Für eine #A0 muss der Nachrichtenspeicheranbieter auf einen [IMAPIProp::OpenProperty-Aufruf](imapiprop-openproperty.md) von **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) reagieren und kann optional auf einen Aufruf von PR_ATTACH_DATA_BIN **.** Beachten **Sie, PR_ATTACH_DATA_BIN** und **PR_ATTACH_DATA_OBJ** denselben Eigenschaftenbezeichner verwenden und somit zwei Wiedergaben derselben Eigenschaft sind. 
  
Für ein Speicherobjekt, z. B. eine Zusammengesetztdatei im OLE 2.0-Docfile-Format, ermöglichen einige Dienstanbieter das Öffnen mit der **MAPI-IStreamDocfile-Schnittstelle,** um die Leistung zu verbessern. Ein Anbieter, der **IStreamDocfile**  unterstützt, muss es auf PR_ATTACH_DATA_OBJ verfügbar machen und kann es optional auf **PR_ATTACH_DATA_BIN.** 
  
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

