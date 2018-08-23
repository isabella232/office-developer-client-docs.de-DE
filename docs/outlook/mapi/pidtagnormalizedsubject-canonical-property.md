---
title: PidTagNormalizedSubject (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNormalizedSubject
api_type:
- HeaderDef
ms.assetid: 2000e6e8-d908-4814-8093-28f8011250c8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b5bc464bc5a251579d262f5926193b7f7a731728
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563661"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a>PidTagNormalizedSubject (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält den Betreff der Nachricht mit dem Präfix entfernt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W  <br/> |
|Kennung:  <br/> |0x0E1D  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |E-Mail  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaften werden berechnet, indem Nachrichtenspeicher oder transport-Anbieter aus der **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) und **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))-Eigenschaften auf folgende Weise.
  
- Wenn die **PR_SUBJECT_PREFIX** vorhanden ist und eine anfängliche Teilzeichenfolge **PR_SUBJECT**ist, werden **PR_NORMALIZED_SUBJECT** und die zugehörigen Eigenschaften auf den Inhalt der **PR_SUBJECT** mit dem Präfix entfernt festgelegt. 
    
- Wenn es sich nicht um eine anfängliche Teilzeichenfolge **PR_SUBJECT**, aber **PR_SUBJECT_PREFIX** vorhanden ist, wird **PR_SUBJECT_PREFIX** gelöscht und neu berechnet aus **PR_SUBJECT** mithilfe der folgenden Regel: Wenn die Zeichenfolge in **PR_SUBJECT** enthalten beginnt mit ein bis drei numerische Zeichen, gefolgt von einem Doppelpunkt und ein Leerzeichen ein, und klicken Sie dann die Zeichenfolge zusammen mit dem Doppelpunkt und die leere das Präfix wird. Zahlen, Leerzeichen und Interpunktionszeichen sind keine gültigen Präfixzeichen. 
    
- Wenn **PR_SUBJECT_PREFIX** nicht vorhanden ist, wird es von **PR_SUBJECT** mithilfe der Regel, die im vorherigen Schritt beschrieben berechnet. Diese Eigenschaft wird auf den Inhalt der **PR_SUBJECT** mit dem Präfix entfernt festgelegt. 
    
 **Hinweis** Wenn **PR_SUBJECT_PREFIX** eine leere Zeichenfolge ist, sind **PR_SUBJECT** und diese Eigenschaft identisch. 
  
Schließlich sollte diese Eigenschaft den Teil des **PR_SUBJECT** hinter dem Präfix sein. Wenn kein Präfix vorhanden ist, wird diese Eigenschaft **PR_SUBJECT**identisch.
  
 **PR_SUBJECT_PREFIX** und diese Eigenschaft sollte als Teil der Implementierung des [IMAPIProp::SaveChanges](imapiprop-savechanges.md) berechnet werden. Eine Clientanwendung sollte nicht die [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode für ihre Werte aufgefordert, bis sie gespeichert wurden durch einen Aufruf von **IMAPIProp::SaveChanges** . 
  
Die Subject-Eigenschaften in der Regel kleine Zeichenfolgen von weniger als 256 Zeichen sind, und eine Nachricht Speicheranbieter ist nicht verpflichtet, klicken sie auf die Object Linking and Embedding (OLE) **IStream** -Schnittstelle unterstützt. Der Client sollte immer Zugriff über die Schnittstelle **IMAPIProp** zuerst versuchen, und greifen auf **IStream** nur, wenn MAPI_E_NOT_ENOUGH_MEMORY zurückgegeben wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

