---
title: PidTagContainerClass (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerClass
api_type:
- HeaderDef
ms.assetid: db249e9e-f1f0-4b95-8cd9-daa7c53ddb32
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c5b80831607f473208ce987a720c7e80e44b6d80
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400257"
---
# <a name="pidtagcontainerclass-canonical-property"></a>PidTagContainerClass (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Textzeichenfolge, die den Typ eines Ordners. Obwohl diese Eigenschaft im Allgemeinen ignoriert wird, erwarten Versionen von Microsoft® Exchange Server vor Exchange Server 2003-Postfach-Manager diese Eigenschaft vorhanden sein.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W  <br/> |
|Kennung:  <br/> |0x3613  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften werden normalerweise nicht vom Exchange-Server verwendet. Allerdings fügt Microsoft Office Outlook® sie an den Postfachordner. Darüber hinaus-Versionen von Exchange Server vor Exchange Server 2003-Postfach-Manager möglicherweise nicht ordnungsgemäß Ordner verarbeitet, die nicht über diese Eigenschaften verfügen.
  
Diese Eigenschaften können die Zeichenfolgenwerte in der folgenden Tabelle zugewiesen werden.
  
|**Wert**|**Inhalt des Ordners**|
|:-----|:-----|
|IPF.Appointment  <br/> |Termine  <br/> |
|IPF.Contact  <br/> |Kontakte  <br/> |
|IPF. Journal  <br/> |Outlook-Journaleinträge  <br/> |
|IPF.Note  <br/> |E-Mail-Nachrichten und Notizen  <br/> |
|IPF. StickyNote  <br/> |Outlook-Kurznotizen  <br/> |
|IPF.Task  <br/> |Outlook-Aufgaben  <br/> |
   
Für Ordner, die e-Mail-Nachrichten enthalten, sollten diese Eigenschaften auf IPF festgelegt werden. Beachten Sie.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für das Erstellen und Ordner mit Sonderfunktion in einem Postfach suchen.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für Kontakt- und Objekte in der persönlichen Verteilerliste Liste zulässig sind.
    
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

