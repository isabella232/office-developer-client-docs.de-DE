---
title: PidTagProfileServerFullVersion (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 66c6b8d50947baafb726c41c28e3bb4d675eab4f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616418"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a>PidTagProfileServerFullVersion (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt vollständige Versions- und Buildinformationen über die Microsoft Exchange Server an, mit der Konten in einem Profil verbunden sind.
  
## 

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PROFILE_SERVER_FULL_VERSION  <br/> |
|Kennung:  <br/> |0x663B  <br/> |
|Eigenschaftentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Profilkonfiguration  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ein Profil kann ein oder mehrere Konten angeben, die eine Verbindung mit einem Exchange Server herstellen, müssen jedoch mit demselben Exchange Server verbunden sein.
  
Versionen von Outlook vor Microsoft Office Outlook 2007 unterstützen diese Eigenschaft nicht. Überprüfen Sie für diese Versionen von Outlook, **[ob PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** im Profil vorhanden sind. 
  
Wenn das aktive Postfach mit einem Exchange Server verbunden ist, speichert Outlook 2007 im allgemeinen vollständige Exchange Server Versionsinformationen in der **eigenschaft PR_PROFILE_SERVER_FULL_VERSION** im aktiven Profil. Outlook speichert die Informationen in einer **EXCHANGE_STORE_VERSION_NUM** Struktur, die die Haupt- und Nebenversionsnummern sowie die Haupt- und Nebenversionsnummern enthält. Um beispielsweise den Exchange Server Versionsbezeichner **8.0.685.24** zu speichern, ist die Hauptversionsnummer 8 und die Nebenversionsnummer 0 und die Hauptbuildnummer 685 und die Nebenbuildnummer 24.
  
In einem Profil ist wahrscheinlich nur eine **PR_PROFILE_SERVER_VERSION** oder **PR_PROFILE_SERVER_FULL_VERSION** vorhanden, es gibt jedoch keine Garantie, dass beide immer in einem Profil vorhanden sind. Outlook schreibt erst dann in eine der Eigenschaften, wenn eine erfolgreiche Verbindung mit dem Exchange Server hergestellt wurde. 
  
Im Outlook-Objektmodell können Sie die **ExchangeMailboxServerVersion-Eigenschaft** des **NameSpace-Objekts** verwenden, um die Version der Exchange Server zu suchen, auf der das aktive Postfach gehostet wird. 
  
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

