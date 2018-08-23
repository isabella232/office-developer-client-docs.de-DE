---
title: PidLidSharingInitiatorSmtp (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorSmtp
api_type:
- COM
ms.assetid: 4fb7d91d-4c51-41c1-9cb6-7b837dd12f11
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: be033af220135175003a6304c5429a5bdee6658e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566523"
---
# <a name="pidlidsharinginitiatorsmtp-canonical-property"></a>PidLidSharingInitiatorSmtp (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt die SMTP-Adresse des Benutzers, der die Freigabenachricht initiiert hat. Dies ist eine Eigenschaft eines eine Freigabenachricht. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidSharingInitiatorSmtp  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Sharing  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008A08  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Freigabe  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft muss auf den Wert der Eigenschaft **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) aus dem Adressbuch identifiziert durch die **DispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md))-Eigenschaft festgelegt und werden sollten ignoriert.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Teilt Postfachordner zwischen Clients.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

