---
title: Kanonische Pidtagprofileserverversion (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d41a536-81ff-733c-2fd7-460798e057c8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 84ff229e9914ec9074d61023873279b110fb606a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286566"
---
# <a name="pidtagprofileserverversion-canonical-property"></a>Kanonische Pidtagprofileserverversion (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt Informationen zu der Version von Microsoft Exchange Server an, mit der Konten in einem Microsoft Outlook-Profil verbunden sind.
  
## 

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PROFILE_SERVER_VERSION  <br/> |
|Kennung:  <br/> |0x661B  <br/> |
|Eigenschafts:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Profilkonfiguration  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ein Profil kann ein oder mehrere Konten angeben, die eine Verbindung mit einem Exchange-Server herstellen, aber Sie müssen mit demselben Exchange-Server verbunden sein.
  
Versionen von Outlook vor Microsoft Office Outlook 2007 können in diese Eigenschaft schreiben, um Informationen über die Exchange Server-Version zu speichern, mit der das aktive Profil verbunden ist. Das Format der Versionsinformationen variiert jedoch für verschiedene Versionen von Exchange Server. Beispielsweise speichert Outlook in **PR_PROFILE_SERVER_VERSION** den dezimalwert 6944, um nur die Haupt-Buildnummer in der Versions-ID von **6.5.6944.3** für Microsoft Exchange Server 2003 darzustellen. Bei einer Exchange 2007-Verbindung speichert Outlook die Hauptversionsnummer und die Haupt-Buildnummer in einer verketteten Hexadezimaldarstellung dieser Zahlen in der-Eigenschaft. Ein Exchange 2007-Versionsbezeichner von **8.0.685.24** hat eine Hauptversion 8 und eine Haupt-buildnummer 685 als Dezimalzahl. Wenn beide Zahlen in Hexadezimalwerte konvertiert werden, erhalten Sie 0x8 und 0x2AD. Bei der Verkettung dieser beiden Zahlen speichert Outlook den Wert 0x82AD in **PR_PROFILE_SERVER_VERSION** in der Hexadezimaldarstellung. 
  
Outlook 2007 liest oder schreibt diese Eigenschaft nicht. Es unterstützt **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**. 
  
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

