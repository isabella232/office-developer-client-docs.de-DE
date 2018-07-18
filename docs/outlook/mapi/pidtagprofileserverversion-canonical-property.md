---
title: PidTagProfileServerVersion (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d41a536-81ff-733c-2fd7-460798e057c8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 571ac25d6bc738f8289e3019c342820682d08c28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794816"
---
# <a name="pidtagprofileserverversion-canonical-property"></a>PidTagProfileServerVersion (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Gibt Informationen über die Version von Microsoft Exchange Server-Konten in einem Microsoft Outlook-Profil verbunden sind.
  
## 

|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_PROFILE_SERVER_VERSION  <br/> |
|Bezeichner:  <br/> |0x661B  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Profil-Konfiguration  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ein Profil kann eine oder mehrere Konten, die mit einem Exchange-Server verbunden angeben, jedoch müssen die gleichen Exchange-Server hergestellt werden.
  
Outlook-Versionen vor Microsoft Office Outlook 2007 können Schreiben auf diese Eigenschaft zum Speichern von Informationen zur Version von Exchange Server mit dem das aktive Profil verbunden ist. Das Format der die Versionsinformationen ändert sich jedoch für die verschiedenen Versionen von Exchange Server. Beispielsweise Buildnummer Outlook-Speicher in **PR_PROFILE_SERVER_VERSION** den Dezimalwert 6944 nur die wichtigsten dargestellt in der Versionsbezeichner des **6.5.6944.3** für Microsoft Exchange Server 2003. Für eine Exchange 2007-Verbindung Outlook speichert die Nummer der Hauptversion und die Major-Buildnummer in einer verketteten hexadezimale Darstellung dieser Zahlen in der Eigenschaft. Ein Exchange 2007-Version-Bezeichner des **8.0.685.24** hat Hauptversionsnummer 8 und eine Haupt-Buildnummer 685 Dezimal. Konvertieren von beiden Zahlen in eine Hexadezimalzahl, erhalten Sie 0 x 8 und 0x2AD. Diese beiden Zahlen verketten, speichert Outlook den Wert 0x82AD in **PR_PROFILE_SERVER_VERSION** , im Hexadezimal-Darstellung. 
  
Outlook 2007 nicht lesen oder Schreiben in diese Eigenschaft. **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** unterstützt. 
  
Nur eine der **PR_PROFILE_SERVER_VERSION** oder **PR_PROFILE_SERVER_FULL_VERSION** wahrscheinlich in einem Profil vorhanden ist, aber es ist nicht gewährleistet, dass entweder immer in einem Profil vorhanden ist. Outlook wird nicht auf eine der Eigenschaften geschrieben, bis er erfolgreich mit dem Exchange-Server verbunden hat. 
  
Im Outlook-Objektmodell können Sie die **ExchangeMailboxServerVersion** -Eigenschaft des **NameSpace** -Objekts verwenden, um die Version von Exchange Server zu erhalten, auf dem das aktuelle Postfach gehostet wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen an.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

