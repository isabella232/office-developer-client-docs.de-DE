---
title: Kanonische PidLidCustomFlag-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidCustomFlag
api_type:
- COM
ms.assetid: bfb7fd1e-774f-9a2f-fbbe-ba7f68ed8663
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3e2f25cba725c5ce47ba62e9ea9ca69475c56122
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595518"
---
# <a name="pidlidcustomflag-canonical-property"></a>Kanonische PidLidCustomFlag-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Bitmaske, die angibt, wie eine Nachricht angepasst wird, z. B. mit benutzerdefinierten Eigenschaften gespeichert.
  
## 

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidCustomFlag  <br/> |
|Long ID (LID):  <br/> |0x00008251  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um den Wert dieser Eigenschaft abzurufen, verwenden Sie zuerst **[IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md)** um das Eigenschaftstag abzurufen, und geben Sie dann dieses Eigenschaftstag in **[IMAPIProp::GetProps](imapiprop-getprops.md)** an, um den Wert abzurufen. 
  
Mögliche Flags sind:
  
****

|**Konstante**|**Wert**|
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0x0D000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x02000000  <br/> |
   
Geben Sie beim Aufrufen von **IMAPIProp::GetIDsFromNames** die folgenden Werte für die **[MAPINAMEID-Struktur](mapinameid.md)** an, auf die durch den Eingabeparameter  *lppPropNames*  verwiesen wird. 
  
****

|**Member**|**Value**|
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_ID  <br/> |
|Kind.lID:  <br/> |dispidCustomFlag  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen bereit.
    
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

