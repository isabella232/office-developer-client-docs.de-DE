---
title: PidTagAttachMethod (kanonische Eigenschaft)
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
description: 'Zuletzt geändert: 07 September 2016'
ms.openlocfilehash: 697f7e8045ca198c2c10b9396f19cb2d7ce8346e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583652"
---
# <a name="pidtagattachmethod-canonical-property"></a>PidTagAttachMethod (kanonische Eigenschaft)

 
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält eine benutzerdefinierte MAPI-Konstante darstellt, die den Inhalt einer Anlage zugegriffen werden können wie. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_METHOD  <br/> |
|Kennung:  <br/> |0x3705  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:
  
NO_ATTACHMENT 
  
> Die Anlage wurde soeben erstellt. 
    
ATTACH_BY_VALUE 
  
> Die **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md))-Eigenschaft enthält die Anlagendaten. 
    
ATTACH_BY_REFERENCE 
  
> Der **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) oder **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md))-Eigenschaft enthält einen vollqualifizierten Pfad, identifiziert die Anlage an Empfänger mit Zugriff auf eine gemeinsame Datei Server. 
    
ATTACH_BY_REF_RESOLVE 
  
> Die **PR_ATTACH_PATHNAME** oder **PR_ATTACH_LONG_PATHNAME** -Eigenschaft enthält einen vollqualifizierten Pfad, die das Attachment-Objekt identifiziert. 
    
ATTACH_BY_REF_ONLY 
  
> Die **PR_ATTACH_PATHNAME** oder **PR_ATTACH_LONG_PATHNAME** -Eigenschaft enthält einen vollqualifizierten Pfad, die das Attachment-Objekt identifiziert. 
    
ATTACH_EMBEDDED_MSG 
  
> Die **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md))-Eigenschaft enthält ein eingebettetes Objekt, das die **IMessage** -Schnittstelle unterstützt. 
    
ATTACH_OLE 
  
> Die Anlage ist ein eingebettetes OLE-Objekt.
    
ATTACH_BY_WEBREFERENCE 
  
> Gescannt ist nicht in der Nachricht. 
    
Wenn erstellt, haben alle Attachment-Objekte **PR_ATTACH_METHOD** Anfangswert **NO_ATTACHMENT**. 
  
Clientanwendungen und Dienstanbieter sind nur erforderlich, zur Unterstützung der Anlage-Methode den Wert **ATTACH_BY_VALUE** dargestellt. Die anderen Anlage Methoden sind optional. Nachrichtenspeicher erzwingt Konsistenz zwischen dem Wert der **PR_ATTACH_METHOD** und die Werte der anderen Eigenschaften Anlage nicht. 
  
Universal naming Convention (UNC) Namen werden für vollqualifizierte Pfade empfohlen, die mit **ATTACH_BY_REFERENCE** und **ATTACH_BY_REF_ONLY**verwendet werden sollte. Mit **ATTACH_BY_REF_RESOLVE**ist ein absoluter Pfad schneller, da die MAPI-Warteschlange das Attachment-Objekts **ATTACH_BY_VALUE**konvertiert. 
  
Wenn **ATTACH_BY_REFERENCE** festgelegt ist, muss **PR_ATTACH_DATA_BIN** leer sein. Kopieren der Anlagendaten in die **PR_ATTACH_DATA_BIN** -Eigenschaft kann ein ausgehender Gateway Anlage **ATTACH_BY_REFERENCE** in Anlage **ATTACH_BY_VALUE** deaktivieren. 
  
Wenn **ATTACH_BY_REF_RESOLVE** festgelegt ist, muss **PR_ATTACH_DATA_BIN** leer sein. Wenn die Nachricht mit der **ATTACH_BY_REF_RESOLVE** Anlage gesendet wird, kopiert die MAPI-Warteschlange die Anlagendaten in eine Anlage **ATTACH_BY_VALUE** . Dieser Prozess Lösung platziert die Anlagedaten in **PR_ATTACH_DATA_BIN**. 
  
Wenn **ATTACH_BY_REF_ONLY** festgelegt ist, **PR_ATTACH_DATA_BIN** muss leer sein, und Nachrichtensystem wird nie der Anlage Verweis aufgelöst. Verwenden Sie diesen Wert, wenn Sie den Link jedoch nicht die Daten senden möchten. 
  
Wenn das OLE-Objekt im OLE 2.0 **IStorage** Format ist, sind die Daten über **PR_ATTACH_DATA_OBJ**zugegriffen werden. Wenn das OLE-Objekt im OLE 1.0 **OLESTREAM** Format ist, können die Daten als **IStream**über **PR_ATTACH_DATA_BIN** zugreifen. Der Typ der Codierung OLE kann durch den Wert **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) bestimmt werden. 
  
Weitere Informationen zu OLE-Schnittstellen und Formate finden Sie unter der *OLE Programmer's Reference* . 
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn die **PR_ATTACH_METHOD** **ATTACH_BY_WEBREFERENCE**ist, ist gescannt nicht in der Nachricht. Stattdessen enthält die **PR_ATTACH_LONG_FILENAME** -Eigenschaft eine absolute URL zu gescannt, der online gespeichert wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[PidTagStoreSupportMask (kanonische Eigenschaft)](pidtagstoresupportmask-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

