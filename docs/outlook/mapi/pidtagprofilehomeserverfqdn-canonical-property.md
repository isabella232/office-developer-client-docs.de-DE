---
title: PidTagProfileHomeServerFQDN (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: aef4a932da35f3c4955bc2f4b265b146775c6d87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341594"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a>PidTagProfileHomeServerFQDN (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Aktiviert die Kerberos-Authentifizierung einer Profilkonfiguration.
  
****

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PROFILE_HOME_SERVER_FQDN  <br/> |
|Kennung:  <br/> |0x662A001F  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Profilkonfiguration  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie diese Eigenschaft auf den Domänennamen des Verzeichnisservers des Benutzers festlegen, wird eine direkte Verbindung mit dem Domänencontroller (Dc) ermöglicht. Dies ist für ein Profil erforderlich, das für die Verwendung der Kerberos-Authentifizierung für Microsoft Exchange Server 2007 und frühere Versionen konfiguriert wurde, indem **RPC_C_AUTHN_GSS_KERBEROS** in **PR_PROFILE_AUTH_PACKAGE PR_PROFILE_AUTH_PACKAGE .**
  
> [!NOTE]
> Microsoft Exchange Server 2010 und Exchange Server 2013 behandeln Adressbuchanrufe an den Clientzugriffsserver anders als in Exchange Server 2007 und früheren Versionen. Der DSProxy-Prozess wird nicht mehr verwendet, sodass die Kerberos-Authentifizierung möglicherweise erfolgreich ist. Der Client würde jedoch weiterhin mit dem Exchange-Server kommunizieren, anstatt direkt mit dem Domänencontroller zu kommunizieren, was möglicherweise **nicht gewünscht** ist: Durch festlegen PR_PROFILE_HOME_SERVER_FQDN wird dies vermieden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Gibt zulässige Vorgänge für die Zentralen Nachrichtenspeicherobjekte an.
    
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

