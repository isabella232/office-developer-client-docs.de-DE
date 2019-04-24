---
title: Kanonische Pidtagprofileserverfullversion (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9456178e9426d7a5fe17382d876f507daa0251f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341601"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a>Kanonische Pidtagprofileserverfullversion (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die vollständige Version und die Erstellung von Informationen zu Microsoft Exchange Server an, mit denen Konten in einem Profil verbunden sind.
  
## 

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PROFILE_SERVER_FULL_VERSION  <br/> |
|Kennung:  <br/> |0x663B  <br/> |
|Eigenschafts:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Profilkonfiguration  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ein Profil kann ein oder mehrere Konten angeben, die eine Verbindung mit einem Exchange-Server herstellen, aber Sie müssen mit demselben Exchange-Server verbunden sein.
  
Versionen von Outlook vor Microsoft Office Outlook 2007 unterstützen diese Eigenschaft nicht. Überprüfen Sie für diese Versionen von Outlook, ob **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** im Profil vorhanden ist. 
  
Wenn das aktive Postfach mit einem Exchange-Server verbunden ist, speichert Outlook 2007 vollständige Exchange Server-Versionsinformationen in der **PR_PROFILE_SERVER_FULL_VERSION** -Eigenschaft im aktiven Profil. Outlook speichert die Informationen in einer **EXCHANGE_STORE_VERSION_NUM** -Struktur, die die Haupt-und Nebenversionsnummern sowie die Haupt-und Nebenversionen enthält. Um beispielsweise die Exchange Server-Versionskennung von **8.0.685.24**zu speichern, ist die Hauptversionsnummer 8, und die Versionsnummer der Nebenversion ist 0, und die Haupt buildnummer lautet 685 und die Minor Build number ist 24.
  
Nur eines von **PR_PROFILE_SERVER_VERSION** oder **PR_PROFILE_SERVER_FULL_VERSION** ist wahrscheinlich in einem Profil vorhanden, aber es gibt keine Garantie, dass es in einem Profil immer vorhanden ist. Outlook schreibt in keiner der Eigenschaften, bis eine erfolgreiche Verbindung mit dem Exchange-Server hergestellt wurde. 
  
Im Outlook-Objektmodell können Sie die **ExchangeMailboxServerVersion** -Eigenschaft des **Namespace** -Objekts verwenden, um die Version von Exchange Server zu suchen, auf der das aktive Postfach gehostet wird. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Definitionen für Eigenschaftensätze bereit.
    
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

