---
title: Kanonische Pidtaguserx509certificate (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUserX509Certificate
api_type:
- COM
ms.assetid: 278bb9e4-3ff6-4bef-b208-7924f7a5e9b1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4e6446283116c39080271e5c2fb3ec128b25d32e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360718"
---
# <a name="pidtaguserx509certificate-canonical-property"></a>Kanonische Pidtaguserx509certificate (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die X. 509 Version 3-Sicherheitszertifikate für einen Messagingbenutzer. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_USER_X509_CERTIFICATE  <br/> |
|Kennung:  <br/> |0x3A70  <br/> |
|Datentyp:  <br/> |PT_MV_BINARY  <br/> |
|Bereich:  <br/> |MAPI-e-Mail-Benutzer  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird von Anwendungen verwendet, die Public-Key-Sicherheit verwenden. Es enthält eine binäre Darstellung eines oder mehrerer Sicherheitszertifikate der X. 509-Version 3. 
  
Verschiedene Anwendungen und Clients können diese Eigenschaft für eigene Sicherheitszertifikate verwenden. Das Binärformat der X. 509-Daten kann je nach Anbieter variieren. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
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

