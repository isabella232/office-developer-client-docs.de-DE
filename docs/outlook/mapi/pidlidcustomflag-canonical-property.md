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
ms.openlocfilehash: 9a131c633b8dcf9b0e5070f01de8fcab90a18ade
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357617"
---
# <a name="pidlidcustomflag-canonical-property"></a>PidLidCustomFlag (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Bitmaske, die angibt, wie eine Nachricht angepasst wird, z. B. mit benutzerdefinierten Eigenschaften gespeichert wird.
  
## 

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidCustomFlag  <br/> |
|Lange ID (LID):  <br/> |0x00008251  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
   
## <a name="remarks"></a>Hinweise

Um den Wert dieser Eigenschaft abzurufen, verwenden Sie zunächst **[IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md)** um das Eigenschaftstag abzurufen, und geben Sie dann dieses Eigenschaftstag in **[IMAPIProp::GetProps](imapiprop-getprops.md)** an, um den Wert abzurufen. 
  
Mögliche Flags sind wie folgt:
  
****

|**Konstante**|**Wert**|
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0x0D000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x02000000  <br/> |
   
Geben Sie beim Aufrufen von **IMAPIProp::GetIDsFromNames** die folgenden Werte für die **[MAPINAMEID-Struktur](mapinameid.md)** an, auf die der Eingabeparameter *lppPropNames verweist.* 
  
****

|**Member**|**Value**|
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_ID  <br/> |
|Kind.lID:  <br/> |dispidCustomFlag  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen zur Verfügung.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

