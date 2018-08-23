---
title: PidLidCustomFlag (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCustomFlag
api_type:
- COM
ms.assetid: bfb7fd1e-774f-9a2f-fbbe-ba7f68ed8663
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cba4989ec3b1afcadb0caddd4af444cc9c96ebda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565956"
---
# <a name="pidlidcustomflag-canonical-property"></a>PidLidCustomFlag (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Eine Bitmaske, die angibt, wie eine Nachricht angepasst ist, beispielsweise mit benutzerdefinierten Eigenschaften gespeichert.
  
## 

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidCustomFlag  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008251  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um den Wert dieser Eigenschaft abzurufen, zunächst mit dem **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** um das Eigenschafts-Tag zu erhalten, und geben Sie in **[IMAPIProp::GetProps](imapiprop-getprops.md)** zum Abrufen des Werts dieser Eigenschaftentag. 
  
Mögliche Flags lauten wie folgt:
  
****

|**Konstante**|**Wert**|
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0x0D000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x02000000  <br/> |
   
Beim Aufruf von **IMAPIProp::GetIDsFromNames**, geben Sie die folgenden Werte für die **[MAPINAMEID](mapinameid.md)** -Struktur, die auf den Eingabeparameter *LppPropNames* zeigt. 
  
****

|**Member**|**Value**|
|:-----|:-----|
|x LpGuid:  <br/> |PSETID_Common  <br/> |
|UlKind:  <br/> |MNID_ID  <br/> |
|Kind.lID:  <br/> |dispidCustomFlag  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen an.
    
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

