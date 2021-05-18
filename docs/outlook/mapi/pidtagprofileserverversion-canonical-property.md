---
title: PidTagProfileServerVersion (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d41a536-81ff-733c-2fd7-460798e057c8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 84ff229e9914ec9074d61023873279b110fb606a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286566"
---
# <a name="pidtagprofileserverversion-canonical-property"></a>PidTagProfileServerVersion (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt Informationen zur Version von Microsoft Exchange Server an, mit denen Konten in einem Microsoft Outlook verbunden sind.
  
## 

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PROFILE_SERVER_VERSION  <br/> |
|Kennung:  <br/> |0x661B  <br/> |
|Eigenschaftstyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Profilkonfiguration  <br/> |
   
## <a name="remarks"></a>Hinweise

Ein Profil kann ein oder mehrere Konten angeben, die eine Verbindung mit Exchange Server herstellen, sie müssen jedoch mit demselben Exchange Server.
  
Versionen von Outlook vor Microsoft Office Outlook 2007 können in diese Eigenschaft schreiben, um Informationen zur Version von Exchange Server zu speichern, mit der das aktive Profil verbunden ist. Das Format der Versionsinformationen variiert jedoch für unterschiedliche Versionen Exchange Server. Beispielsweise speichert Outlook in **PR_PROFILE_SERVER_VERSION** den Dezimalwert 6944, um nur die Haupt buildnummer im Versionsbezeichner **6.5.6944.3** für Microsoft Exchange Server 2003 zu repräsentieren. Für eine Exchange 2007 speichert Outlook die Hauptversionsnummer und die Hauptbaunummer in einer verkettten hexadezimalen Darstellung dieser Zahlen in der Eigenschaft. Eine Exchange Version 2007 von **8.0.685.24** hat die Hauptversionsnummer 8 und die Hauptbaunummer 685 im Dezimalformat. Wenn Sie beide Zahlen in Hexadezimal konvertieren, erhalten 0x8 und 0x2AD. Wenn Sie diese beiden Zahlen verketten, Outlook der Wert 0x82AD **in** PR_PROFILE_SERVER_VERSION in hexadezimaler Darstellung. 
  
Outlook 2007 liest oder schreibt nicht in diese Eigenschaft. Es unterstützt **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**. 
  
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

