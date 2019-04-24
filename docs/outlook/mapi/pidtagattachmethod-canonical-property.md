---
title: Kanonische Pidtagattachmethod (-Eigenschaft
manager: soliver
ms.date: 9/7/2016
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMethod
api_type:
- HeaderDef
ms.assetid: 32089213-ef7b-4152-84ab-b44e9911332b
description: 'Zuletzt geändert: 2016'
ms.openlocfilehash: b84549ab31c939b4e6115795916ebd3520a96dbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327258"
---
# <a name="pidtagattachmethod-canonical-property"></a>Kanonische Pidtagattachmethod (-Eigenschaft

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine MAPI-definierte Konstante, die die Art darstellt, in der auf den Inhalt einer Anlage zugegriffen werden kann. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_METHOD  <br/> |
|Kennung:  <br/> |0x3705  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann genau einen der folgenden Werte haben:
  
NO_ATTACHMENT 
  
> Die Anlage wurde soeben erstellt. 
    
ATTACH_BY_VALUE 
  
> Die **PR_ATTACH_DATA_BIN** ([pidtagattachdatabinary (](pidtagattachdatabinary-canonical-property.md))-Eigenschaft enthält die Anlagendaten. 
    
ATTACH_BY_REFERENCE 
  
> Die **PR_ATTACH_PATHNAME** ([pidtagattachpathname (](pidtagattachpathname-canonical-property.md))-oder **PR_ATTACH_LONG_PATHNAME** ([pidtagattachlongpathname (](pidtagattachlongpathname-canonical-property.md))-Eigenschaft enthält einen vollqualifizierten Pfad, der die Anlage von Empfängern mit Zugriff auf eine gemeinsame Datei identifiziert. Server. 
    
ATTACH_BY_REF_RESOLVE 
  
> Die **PR_ATTACH_PATHNAME** -oder die **PR_ATTACH_LONG_PATHNAME** -Eigenschaft enthält einen vollqualifizierten Pfad, der die Anlage identifiziert. 
    
ATTACH_BY_REF_ONLY 
  
> Die **PR_ATTACH_PATHNAME** -oder die **PR_ATTACH_LONG_PATHNAME** -Eigenschaft enthält einen vollqualifizierten Pfad, der die Anlage identifiziert. 
    
ATTACH_EMBEDDED_MSG 
  
> Die **PR_ATTACH_DATA_OBJ** ([pidtagattachdataobject (](pidtagattachdataobject-canonical-property.md))-Eigenschaft enthält ein eingebettetes Objekt, das die **IMessage** -Schnittstelle unterstützt. 
    
ATTACH_OLE 
  
> Die Anlage ist ein eingebettetes OLE-Objekt.
    
ATTACH_BY_WEBREFERENCE 
  
> Der Anlageninhalt befindet sich nicht in der Nachricht. 
    
Bei der Erstellung haben alle Attachment-Objekte einen anfänglichen **PR_ATTACH_METHOD** -Wert von **NO_ATTACHMENT**. 
  
Client Anwendungen und Dienstanbieter sind nur für die Unterstützung der vom **ATTACH_BY_VALUE** -Wert dargestellten Anlagen Methode erforderlich. Die anderen Anlagen Methoden sind optional. Der Nachrichtenspeicher erzwingt keine Konsistenz zwischen dem Wert von **PR_ATTACH_METHOD** und den Werten der anderen Anlageneigenschaften. 
  
UNC-Namen (Universal Naming Convention) werden für vollqualifizierte Pfade empfohlen, die mit **ATTACH_BY_REFERENCE** und **ATTACH_BY_REF_ONLY**verwendet werden sollen. Bei **ATTACH_BY_REF_RESOLVE**ist ein absoluter Pfad schneller, da der MAPI-Spooler die Anlage in **ATTACH_BY_VALUE**konvertiert. 
  
Wenn **ATTACH_BY_REFERENCE** festgelegt ist, muss **PR_ATTACH_DATA_BIN** leer sein. Ein ausgehendes Gateway kann eine **ATTACH_BY_REFERENCE** -Anlage in eine **ATTACH_BY_VALUE** -Anlage umwandeln, indem die Anlagendaten in die **PR_ATTACH_DATA_BIN** -Eigenschaft kopiert werden. 
  
Wenn **ATTACH_BY_REF_RESOLVE** festgelegt ist, muss **PR_ATTACH_DATA_BIN** leer sein. Wenn die Nachricht, die die **ATTACH_BY_REF_RESOLVE** -Anlage enthält, gesendet wird, werden die Anlagendaten vom MAPI-Spooler in eine **ATTACH_BY_VALUE** -Anlage kopiert. Dieser Lösungsprozess platziert die Anlagendaten in **PR_ATTACH_DATA_BIN**. 
  
Wenn **ATTACH_BY_REF_ONLY** festgelegt ist, muss **PR_ATTACH_DATA_BIN** leer sein, und das Messagingsystem löst die Anlagen Referenz nie auf. Verwenden Sie diesen Wert, wenn Sie den Link, aber nicht die Daten senden möchten. 
  
Wenn sich das OLE-Objekt im OLE 2,0- **IStorage** -Format befindet, können Sie über **PR_ATTACH_DATA_OBJ**auf die Daten zugreifen. Wenn sich das OLE-Objekt im OLE 1,0- **OLESTREAM** -Format befindet, können die Daten über **PR_ATTACH_DATA_BIN** als **IStream**aufgerufen werden. Der Typ der OLE-Codierung kann durch den **PR_ATTACH_TAG** ([pidtagattachtag (](pidtagattachtag-canonical-property.md))-Wert bestimmt werden. 
  
Weitere Informationen zu OLE-Schnittstellen und-Formaten finden Sie unter *OLE Programmer es Reference* . 
  
## <a name="remarks"></a>Bemerkungen

Wenn das **PR_ATTACH_METHOD** - **ATTACH_BY_WEBREFERENCE**ist, ist der Anlageninhalt nicht in der Nachricht. Stattdessen enthält die **PR_ATTACH_LONG_FILENAME** -Eigenschaft eine absolute URL für den Anlageninhalt, der Online gespeichert wird. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagStoreSupportMask-Eigenschaft](pidtagstoresupportmask-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

