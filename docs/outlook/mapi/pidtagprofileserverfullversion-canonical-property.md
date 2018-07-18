---
title: PidTagProfileServerFullVersion (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 284b4b451a31a9478caf31fe855d38bfeab2caf3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794819"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a>PidTagProfileServerFullVersion (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Gibt die vollständige Angaben zu Version und Build über die Microsoft Exchange Server-Konten in einem Profil verbunden sind.
  
## 

|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_PROFILE_SERVER_FULL_VERSION  <br/> |
|Bezeichner:  <br/> |0x663B  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Profil-Konfiguration  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ein Profil kann eine oder mehrere Konten, die mit einem Exchange-Server verbunden angeben, jedoch müssen die gleichen Exchange-Server hergestellt werden.
  
Diese Eigenschaft wird von Outlook-Versionen vor Microsoft Office Outlook 2007 nicht unterstützt. Überprüfen Sie für diese Versionen von Outlook das Vorhandensein des **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** im Profil. 
  
Wenn das aktive Postfach mit einem Exchange-Server verbunden ist, speichert Outlook 2007 umfassende Informationen zur Version von Exchange Server in der Regel in der **PR_PROFILE_SERVER_FULL_VERSION** -Eigenschaft in das aktive Profil. Outlook speichert die Informationen in eine **EXCHANGE_STORE_VERSION_NUM** -Struktur, die Haupt- und Hilfsintervalle Versionsnummern und die Haupt- und Hilfsintervalle Buildnummern enthält. Beispielsweise, um die Exchange Server-Version-Bezeichner des **8.0.685.24**gespeichert werden sollen, ist die Nummer der Hauptversion 8 und Nebenversionsnummer ist 0, und die wichtigsten Buildnummer wird 685 und minor Buildnummer 24 ist.
  
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

