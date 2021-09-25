---
title: PidTagAttachMethod (kanonische Eigenschaft)
manager: soliver
ms.date: 9/7/2016
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachMethod
api_type:
- HeaderDef
ms.assetid: 32089213-ef7b-4152-84ab-b44e9911332b
description: 'Last modified: September 07, 2016'
ms.openlocfilehash: b4e6aa70b793fafc08d0b975641f5bc0d07bc831
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609901"
---
# <a name="pidtagattachmethod-canonical-property"></a>PidTagAttachMethod (kanonische Eigenschaft)

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine MAPI-definierte Konstante, die angibt, wie auf den Inhalt einer Anlage zugegriffen werden kann. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_METHOD  <br/> |
|Kennung:  <br/> |0x3705  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft kann genau einen der folgenden Werte haben:
  
NO_ATTACHMENT 
  
> Die Anlage wurde gerade erstellt. 
    
ATTACH_BY_VALUE 
  
> Die **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) -Eigenschaft enthält die Anlagendaten. 
    
ATTACH_BY_REFERENCE 
  
> Die **eigenschaft PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) oder **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) enthält einen vollqualifizierten Pfad, der die Anlage an Empfänger mit Zugriff auf einen gemeinsamen Dateiserver identifiziert. 
    
ATTACH_BY_REF_RESOLVE 
  
> Die **eigenschaft PR_ATTACH_PATHNAME** oder **PR_ATTACH_LONG_PATHNAME** enthält einen vollqualifizierten Pfad, der die Anlage identifiziert. 
    
ATTACH_BY_REF_ONLY 
  
> Die **eigenschaft PR_ATTACH_PATHNAME** oder **PR_ATTACH_LONG_PATHNAME** enthält einen vollqualifizierten Pfad, der die Anlage identifiziert. 
    
ATTACH_EMBEDDED_MSG 
  
> Die **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) -Eigenschaft enthält ein eingebettetes Objekt, das die **IMessage-Schnittstelle** unterstützt. 
    
ATTACH_OLE 
  
> Die Anlage ist ein eingebettetes OLE-Objekt.
    
ATTACH_BY_WEBREFERENCE 
  
> Der Anlageninhalt ist nicht in der Nachricht enthalten. 
    
Bei der Erstellung weisen alle Anlagenobjekte einen anfänglichen **PR_ATTACH_METHOD** Wert **von NO_ATTACHMENT auf.** 
  
Clientanwendungen und Dienstanbieter müssen nur die Anlagenmethode unterstützen, die durch den **wert ATTACH_BY_VALUE** dargestellt wird. Die anderen Anlagenmethoden sind optional. Der Nachrichtenspeicher erzwingt keine Konsistenz zwischen dem Wert von **PR_ATTACH_METHOD** und den Werten der anderen Anlageneigenschaften. 
  
UnC-Namen (Universal Naming Convention) werden für vollqualifizierte Pfade empfohlen, die mit **ATTACH_BY_REFERENCE** und **ATTACH_BY_REF_ONLY** verwendet werden sollten. Bei **ATTACH_BY_REF_RESOLVE** ist ein absoluter Pfad schneller, da der MAPI-Spooler die Anlage in **ATTACH_BY_VALUE** konvertiert. 
  
Wenn **ATTACH_BY_REFERENCE** festgelegt ist, muss **PR_ATTACH_DATA_BIN** leer sein. Ein ausgehendes Gateway kann eine **ATTACH_BY_REFERENCE** Anlage in eine **ATTACH_BY_VALUE** Anlage umwandeln, indem die Anlagendaten in die eigenschaft PR_ATTACH_DATA_BIN kopiert **werden.** 
  
Wenn **ATTACH_BY_REF_RESOLVE** festgelegt ist, muss **PR_ATTACH_DATA_BIN** leer sein. Wenn die Nachricht, die die **ATTACH_BY_REF_RESOLVE** Anlage enthält, gesendet wird, kopiert der MAPI-Spooler die Anlagendaten in eine **ATTACH_BY_VALUE** Anlage. Bei diesem Lösungsprozess werden die Anlagendaten in **PR_ATTACH_DATA_BIN** platziert. 
  
Wenn **ATTACH_BY_REF_ONLY** festgelegt ist, muss **PR_ATTACH_DATA_BIN** leer sein, und das Messagingsystem löst den Anlagenverweis nie auf. Verwenden Sie diesen Wert, wenn Sie den Link senden möchten, aber nicht die Daten. 
  
Wenn das OLE-Objekt im OLE 2.0-IStorage-Format vorliegt, kann auf die Daten über PR_ATTACH_DATA_OBJ zugegriffen **werden.**  Wenn sich das OLE-Objekt im OLE 1.0 **OLESTREAM-Format** befindet, kann auf die Daten über **PR_ATTACH_DATA_BIN** als **IStream** zugegriffen werden. Der Typ der OLE-Codierung kann durch den **wert PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) bestimmt werden. 
  
Weitere Informationen zu OLE-Schnittstellen und -Formaten finden Sie in der *OLE-Programmierreferenz.* 
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn die **PR_ATTACH_METHOD** **ATTACH_BY_WEBREFERENCE** ist, befindet sich der Anlageninhalt nicht in der Nachricht. Stattdessen enthält die **PR_ATTACH_LONG_FILENAME-Eigenschaft** eine absolute URL zum Anlageninhalt, der online gespeichert wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagStoreSupportMask-Eigenschaft](pidtagstoresupportmask-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

