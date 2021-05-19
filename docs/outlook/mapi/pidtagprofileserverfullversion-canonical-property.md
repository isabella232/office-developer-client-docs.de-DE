---
title: PidTagProfileServerFullVersion (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9456178e9426d7a5fe17382d876f507daa0251f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341601"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a>PidTagProfileServerFullVersion (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt vollständige Versions- und Buildinformationen zu Microsoft Exchange Server, mit denen Konten in einem Profil verbunden sind.
  
## 

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PROFILE_SERVER_FULL_VERSION  <br/> |
|Kennung:  <br/> |0x663B  <br/> |
|Eigenschaftstyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Profilkonfiguration  <br/> |
   
## <a name="remarks"></a>Hinweise

Ein Profil kann ein oder mehrere Konten angeben, die eine Verbindung mit Exchange Server herstellen, sie müssen jedoch mit demselben Exchange Server.
  
Versionen von Outlook vor Microsoft Office Outlook 2007 unterstützen diese Eigenschaft nicht. Überprüfen Sie für diese Outlook, ob eine PR_PROFILE_SERVER_VERSION **[im](pidtagprofileserverversion-canonical-property.md)** Profil angezeigt wird. 
  
Wenn das aktive Postfach mit einer Exchange Server verbunden ist, speichert Outlook 2007 im allgemeinen vollständige Exchange Server Versionsinformationen in der **PR_PROFILE_SERVER_FULL_VERSION-Eigenschaft** im aktiven Profil. Outlook speichert die Informationen in einer **EXCHANGE_STORE_VERSION_NUM,** die die Haupt- und Nebenversionsnummern sowie die Haupt- und Nebenversionsnummern enthält. Wenn Sie z. B. die Exchange Server-Versions-ID **von 8.0.685.24** speichern möchten, ist die Hauptversionsnummer 8 und die Nebenversionsnummer 0, und die Hauptversionsnummer ist 685 und die Nebenversionsnummer 24.
  
Es ist **wahrscheinlich PR_PROFILE_SERVER_VERSION** oder **PR_PROFILE_SERVER_FULL_VERSION** in einem Profil vorhanden ist, aber es gibt keine Garantie, dass in einem Profil immer vorhanden ist. Outlook schreibt erst in eine eigenschaft, wenn sie erfolgreich mit dem Objekt verbunden Exchange Server. 
  
Im Outlook-Objektmodell können Sie die **ExchangeMailboxServerVersion-Eigenschaft** des **NameSpace-Objekts** verwenden, um die Version von Exchange Server zu finden, in der das aktive Postfach gehostet wird. 
  
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

