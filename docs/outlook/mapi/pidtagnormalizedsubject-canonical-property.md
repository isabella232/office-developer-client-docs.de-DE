---
title: Kanonische PidTagNormalizedSubject-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 54a0f438dacc8a1c7838eb538ec05c5c263f1b0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329274"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a>Kanonische PidTagNormalizedSubject-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Betreff der Nachricht mit einem beliebigen Präfix entfernt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W  <br/> |
|Kennung:  <br/> |0x0E1D  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |E-Mail  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften werden von den Nachrichtenspeicher-oder Transportanbietern aus den Eigenschaften **PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md)) und **PR_SUBJECT_PREFIX** ([pidtagsubjectprefix (](pidtagsubjectprefix-canonical-property.md)) auf folgende Weise berechnet.
  
- Wenn **PR_SUBJECT_PREFIX** vorhanden ist und eine anfängliche Teilzeichenfolge von **PR_Subject**ist, werden **PR_NORMALIZED_SUBJECT** und zugehörige Eigenschaften auf den Inhalt von **PR_Subject** festgelegt, wobei das Präfix entfernt wird. 
    
- Wenn **PR_SUBJECT_PREFIX** vorhanden ist, aber keine anfängliche Teilzeichenfolge von **PR_Subject**ist, wird **PR_SUBJECT_PREFIX** gelöscht und von **PR_Subject** mithilfe der folgenden Regel neu berechnet: Wenn die in **PR_Subject** enthaltene Zeichenfolge beginnt mit einem bis drei nicht-numerischen Zeichen, gefolgt von einem Doppelpunkt und einem Raum, dann wird die Zeichenfolge zusammen mit dem Doppelpunkt und dem leeren das Präfix. Zahlen, Leerzeichen und Interpunktionen sind keine gültigen Präfixzeichen. 
    
- Wenn **PR_SUBJECT_PREFIX** nicht vorhanden ist, wird es aus **PR_Subject** mithilfe der im vorherigen Schritt beschriebenen Regel berechnet. Diese Eigenschaft wird dann auf den Inhalt von **PR_Subject** festgelegt, wobei das Präfix entfernt wurde. 
    
 **Hinweis** Wenn **PR_SUBJECT_PREFIX** eine leere Zeichenfolge ist, sind **PR_Subject** und diese Eigenschaft identisch. 
  
Schließlich sollte diese Eigenschaft der Teil von **PR_Subject** sein, der dem Präfix folgt. Wenn kein Präfix vorliegt, wird diese Eigenschaft mit **PR_Subject**identisch.
  
 **PR_SUBJECT_PREFIX** und diese Eigenschaft sollten als Teil der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Implementierung berechnet werden. Eine Clientanwendung sollte die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode für ihre Werte erst auffordern, nachdem Sie von einem **IMAPIProp:: SaveChanges** -Aufruf übergeben wurden. 
  
Die Subject-Eigenschaften sind in der Regel kleine Zeichenfolgen mit weniger als 256 Zeichen, und ein Nachrichtenspeicher Anbieter ist nicht zur Unterstützung der OLE- **IStream** -Schnittstelle (Object Linking and Embedding) für Sie verpflichtet. Der Client sollte immer versuchen, zuerst über die **IMAPIProp** -Schnittstelle zuzugreifen, und nur dann auf **IStream** zurückgreifen, wenn MAPI_E_NOT_ENOUGH_MEMORY wird. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

