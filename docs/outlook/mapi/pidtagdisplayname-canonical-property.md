---
title: PidTagDisplayName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayName
api_type:
- HeaderDef
ms.assetid: bd094e00-5c60-4bb3-9a45-b943fab52876
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 834141fe3e57fde5e6404776e0ad5ce3b438450e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360802"
---
# <a name="pidtagdisplayname-canonical-property"></a>PidTagDisplayName (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Anzeigenamen für ein bestimmtes MAPI-Objekt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W  <br/> |
|Kennung:  <br/> |0x3001  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI allgemein  <br/> |
   
## <a name="remarks"></a>Hinweise

Ordner erfordern gleichgeordnete Unterordner, um eindeutige Anzeigenamen zu haben. Wenn ein Ordner beispielsweise zwei Unterordner enthält, können die beiden Unterordner nicht denselben Wert für diese Eigenschaft verwenden. Diese Einschränkung gilt nicht für andere Container, z. B. Adressbücher und Verteilerlisten. 
  
Dienstanbieter sollten den Wert dieser Eigenschaft so festlegen, dass sie sowohl den Anbietertyp als auch Konfigurationsinformationen enthält. Die zusätzlichen Informationen helfen, zwischen Instanzen von Anbietern desselben Typs zu unterscheiden. Nicht konfigurierte Anbieter sollten eine Zeichenfolge verwenden, die den Anbieter benennt. Konfigurierte Anbieter sollten dieselbe Zeichenfolge gefolgt von einer unterscheidenden Zeichenfolge in Klammern verwenden. Ein nicht konfigurierter Nachrichtenspeicheranbieter kann beispielsweise folgende Eigenschaften festlegen: 
  
Personenbezogene Store
  
Die konfigurierte Version kann dann die folgenden Eigenschaften festlegen: 
  
Personal Information Store (6. Februar 1998)
  
Für Statusobjekte enthalten diese Eigenschaften den Namen der Komponente, die von der Benutzeroberfläche angezeigt werden kann. 
  
> [!NOTE]
> Semikolons können nicht innerhalb von Empfängernamen in MAPI-Nachrichten verwendet werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Verarbeitet Ordnervorgänge.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.
    
[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)
  
> Erweitert das WebDAV-Protokoll, das angibt, wie der Sicherheitsdeskriptor Exchange WebDAV-Methoden an- und festgelegt wird.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagTransmittableDisplayName (kanonische Eigenschaft)](pidtagtransmittabledisplayname-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

