---
title: PidTagProfileHomeServerFQDN (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f0050c89d69c8dd42a17b7eba1adbc1b6ff18cbe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583275"
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
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Festlegen dieser Eigenschaft auf den Domänennamen des Verzeichnisservers des Benutzers ermöglicht eine direkte Verbindung mit dem Domänencontroller (DC), der für ein Profil erforderlich ist, das für die Verwendung der Kerberos-Authentifizierung für Microsoft Exchange Server 2007 und frühere Versionen konfiguriert wurde, indem **RPC_C_AUTHN_GSS_KERBEROS** in **PR_PROFILE_AUTH_PACKAGE** festgelegt wird.
  
> [!NOTE]
> in Microsoft Exchange Server 2010 und Exchange Server 2013 werden Adressbuchaufrufe an den Clientzugriffsserver anders behandelt als in Exchange Server 2007 und früheren Versionen. Der DSProxy-Prozess wird nicht mehr verwendet, sodass die Kerberos-Authentifizierung möglicherweise erfolgreich ist. Der Client kommuniziert jedoch weiterhin mit dem Exchange-Server und nicht direkt mit dem DC, was möglicherweise nicht gewünscht ist: Das Festlegen **PR_PROFILE_HOME_SERVER_FQDN** verhindert dies. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Gibt zulässige Vorgänge für die zentralen Nachrichtenspeicherobjekte an.
    
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

