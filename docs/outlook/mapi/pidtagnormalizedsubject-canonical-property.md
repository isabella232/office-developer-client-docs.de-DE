---
title: PidTagNormalizedSubject (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagNormalizedSubject
api_type:
- HeaderDef
ms.assetid: 2000e6e8-d908-4814-8093-28f8011250c8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0f7765fb7898ed76dd7b537bc0eeefc21e626fb4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555279"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a>PidTagNormalizedSubject (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Nachrichtenbetreff mit entfernten Präfixen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W  <br/> |
|Kennung:  <br/> |0x0E1D  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |E-Mails  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaften werden von Nachrichtenspeicher- oder Transportanbietern aus den **Eigenschaften PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) und **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) auf folgende Weise berechnet.
  
- Wenn die **PR_SUBJECT_PREFIX** vorhanden ist und eine anfängliche Teilzeichenfolge von **PR_SUBJECT** ist, werden **PR_NORMALIZED_SUBJECT** und die zugehörigen Eigenschaften auf den Inhalt von **PR_SUBJECT** mit dem entfernten Präfix festgelegt. 
    
- Wenn **PR_SUBJECT_PREFIX** vorhanden ist, es sich jedoch nicht um eine anfängliche Teilzeichenfolge **von PR_SUBJECT** handelt, wird **PR_SUBJECT_PREFIX** aus **PR_SUBJECT** mithilfe der folgenden Regel gelöscht und neu berechnet: Wenn die in **PR_SUBJECT** enthaltene Zeichenfolge mit einem bis drei nicht numerischen Zeichen beginnt, gefolgt von einem Doppelpunkt und einem Leerzeichen, wird die Zeichenfolge zusammen mit dem Doppelpunkt und dem Leeren zum Präfix. Zahlen, Leerzeichen und Interpunktionszeichen sind keine gültigen Präfixzeichen. 
    
- Wenn **PR_SUBJECT_PREFIX** nicht vorhanden ist, wird sie anhand **PR_SUBJECT** mithilfe der im vorherigen Schritt beschriebenen Regel berechnet. Diese Eigenschaft wird dann auf den Inhalt von **PR_SUBJECT** festgelegt, wobei das Präfix entfernt wird. 
    
 **Hinweis** Wenn **PR_SUBJECT_PREFIX** eine leere Zeichenfolge ist, sind **PR_SUBJECT** und diese Eigenschaft identisch. 
  
Letztendlich sollte diese Eigenschaft Teil der **PR_SUBJECT** sein, die auf das Präfix folgen. Wenn kein Präfix vorhanden ist, wird diese Eigenschaft mit **PR_SUBJECT** identisch.
  
 **PR_SUBJECT_PREFIX** und diese Eigenschaft sollten als Teil der [IMAPIProp::SaveChanges-Implementierung](imapiprop-savechanges.md) berechnet werden. Eine Clientanwendung sollte die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) erst dann zur Eingabe ihrer Werte auffordern, wenn ein Commit durch einen **IMAPIProp::SaveChanges-Aufruf** ausgeführt wurde. 
  
Die Betreffeigenschaften sind in der Regel kleine Zeichenfolgen mit weniger als 256 Zeichen, und ein Nachrichtenspeicheranbieter ist nicht verpflichtet, die **Ole-IStream-Schnittstelle** (Object Linking and Embedding) für sie zu unterstützen. Der Client sollte immer zuerst versuchen, über die **IMAPIProp-Schnittstelle** auf **IStream** zuzugreifen, wenn MAPI_E_NOT_ENOUGH_MEMORY zurückgegeben wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

