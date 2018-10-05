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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386418"
---
# <a name="pidtagdisplayname-canonical-property"></a>PidTagDisplayName (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Anzeigenamen für ein bestimmtes MAPI-Objekt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W  <br/> |
|Kennung:  <br/> |0x3001  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Allgemeine MAPI  <br/> |
   
## <a name="remarks"></a>Hinweise

Ordner erfordern gleichgeordneten Knoten Unterordner eindeutigen Anzeigenamen haben. Beispielsweise wenn ein Ordner zwei Unterordner enthält, können nicht zwei Unterordner den gleichen Wert für diese Eigenschaft verwenden. Diese Beschränkung gilt nicht für andere Container, z. B. Adressbücher und Verteilerlisten. 
  
Dienstanbieter sollte den Wert dieser Eigenschaft festgelegt, sodass sie die Anbieter Typ und die Konfiguration der Informationen enthält. Weitere Informationen hilft zum unterscheiden zwischen Instanzen von Anbietern des gleichen Typs. Nicht konfigurierte Anbieter sollte eine Zeichenfolge verwenden, die den Namen des Anbieters. Konfigurierte Anbieter sollten Sie dieselbe Zeichenfolge gefolgt von einer charakteristische Zeichenfolge in Klammern verwenden. Beispielsweise kann ein Anbieter nicht konfigurierte Nachricht diese Eigenschaften auf festgelegt: 
  
Persönlicher Informationsspeicher
  
Die konfigurierte Version kann anschließend diese Eigenschaften festgelegt werden auf: 
  
Persönlicher Informationsspeicher (6 Februar 1998)
  
Für Status-Objekte enthalten diese Eigenschaften den Namen der Komponente, die von der Benutzeroberfläche angezeigt werden kann. 
  
> [!NOTE]
> Semikolons können nicht innerhalb von Empfängernamen in MAPI messaging verwendet werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Ordner Vorgänge behandelt.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.
    
[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)
  
> Erweitert das Protokoll WebDAV, das angibt, wie angefordert, und legen Sie die Exchange-Sicherheits-ID über WebDAV-Methoden.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[PidTagTransmittableDisplayName (kanonische Eigenschaft)](pidtagtransmittabledisplayname-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

