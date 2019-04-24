---
title: Kanonische Pidtagprofilehomeserverfqdn (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: aef4a932da35f3c4955bc2f4b265b146775c6d87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341594"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a>Kanonische Pidtagprofilehomeserverfqdn (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Aktiviert die Kerberos-Authentifizierung einer Profilkonfiguration.
  
****

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PROFILE_HOME_SERVER_FQDN  <br/> |
|Kennung:  <br/> |0x662A001F  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Profilkonfiguration  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie diese Eigenschaft auf den Domänennamen des Verzeichnisservers des Benutzers festlegen, ist eine direkte Verbindung mit dem Domänen Controller (DC) möglich, der für ein Profil erforderlich ist, das für die Verwendung der Kerberos-Authentifizierung für Microsoft Exchange Server 2007 konfiguriert wurde und frühere Versionen, durch Festlegen von **RPC_C_AUTHN_GSS_KERBEROS** in **PR_PROFILE_AUTH_PACKAGE**.
  
> [!NOTE]
> Microsoft Exchange Server 2010 und Exchange Server 2013 behandeln Adressbuch Aufrufe, die auf dem Client Zugriffs Server vorgenommen wurden, anders als die Art und Weise, in der Sie von Exchange Server 2007 und früheren Versionen verarbeitet wurden. Der DSProxy-Prozess wird nicht mehr verwendet, sodass die Kerberos-Authentifizierung möglicherweise erfolgreich ausgeführt wird. Der Client würde jedoch weiterhin mit dem Exchange-Server und nicht direkt mit dem DC kommunizieren, was möglicherweise nicht erwünscht ist: die Einstellung **PR_PROFILE_HOME_SERVER_FQDN** vermeidet dies. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Gibt zulässige Vorgänge für die wichtigsten Nachrichtenspeicher Objekte an.
    
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

