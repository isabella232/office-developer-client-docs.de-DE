---
title: Kanonische PidTagProfileServerVersion-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5d41a536-81ff-733c-2fd7-460798e057c8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 61e7e9071bf943320fcd41cbb933e00cd123907c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616425"
---
# <a name="pidtagprofileserverversion-canonical-property"></a>Kanonische PidTagProfileServerVersion-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt Informationen zur Version von Microsoft Exchange Server an, mit denen Konten in einem Microsoft Outlook-Profil verbunden sind.
  
## 

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PROFILE_SERVER_VERSION  <br/> |
|Kennung:  <br/> |0x661B  <br/> |
|Eigenschaftentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Profilkonfiguration  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ein Profil kann ein oder mehrere Konten angeben, die eine Verbindung mit einem Exchange Server herstellen, müssen jedoch mit demselben Exchange Server verbunden sein.
  
Versionen von Outlook vor Microsoft Office Outlook 2007 können in diese Eigenschaft schreiben, um Informationen über die Version von Exchange Server zu speichern, mit der das aktive Profil verbunden ist. Das Format der Versionsinformationen variiert jedoch für unterschiedliche Versionen von Exchange Server. Beispielsweise speichert Outlook in **PR_PROFILE_SERVER_VERSION** den Dezimalwert 6944, um nur die Hauptbuildnummer im Versionsbezeichner **6.5.6944.3** für Microsoft Exchange Server 2003 darzustellen. Bei einer Exchange 2007-Verbindung speichert Outlook die Hauptversionsnummer und die Hauptbuildnummer in einer verketteten hexadezimalen Darstellung dieser Zahlen in der Eigenschaft. Ein Exchange 2007-Versionsbezeichner **8.0.685.24** hat die Hauptversionsnummer 8 und die Hauptbuildnummer 685 im Dezimaltrennzeichen. Wenn Sie beide Zahlen in hexadezimale Zahlen konvertieren, erhalten Sie 0x8 und 0x2AD. Beim Verketten dieser beiden Zahlen speichert Outlook den Wert 0x82AD in **PR_PROFILE_SERVER_VERSION** in hexadezimaler Darstellung. 
  
Outlook 2007 liest oder schreibt nicht in diese Eigenschaft. Es unterstützt **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**. 
  
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

